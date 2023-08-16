# Protect the Docker daemon socket

Zertifikat generieren
Die unter macOS mit openssl generierten Certificate sind nicht mit Docker kompatibel, sie müssen auf einem Linux-System generiert werden.
```
$ ssh metarow
$ openssl genrsa -aes256 -out ca-key.pem 4096
StandardMitZahl
```

```
$ openssl req -new -x509 -days 365 -key ca-key.pem -sha256 -out ca.pem
StandartMitZahl
DE
.
Magdeburg
MetaRow UG
.
metarow.com
.
```

```
$ openssl genrsa -out server-key.pem 4096
```

```
$ openssl req -subj "/CN=metarow.com" -sha256 -new -key server-key.pem -out server.csr
$ echo subjectAltName = DNS:metarow.com,IP:176.9.24.187,IP:127.0.0.1 > extfile.cnf
$ openssl x509 -req -days 365 -sha256 -in server.csr -CA ca.pem -CAkey ca-key.pem \
-CAcreateserial -out server-cert.pem -extfile extfile.cnf
```

```
$ openssl genrsa -out key.pem 4096
$ openssl req -subj '/CN=client' -new -key key.pem -out client.csr
$ echo extendedKeyUsage = clientAuth > extfile.cnf
$ openssl x509 -req -days 365 -sha256 -in client.csr -CA ca.pem -CAkey ca-key.pem \
-CAcreateserial -out cert.pem -extfile extfile.cnf
StandardMitZahl
$ rm -v client.csr server.csr
$ chmod -v 0400 ca-key.pem key.pem server-key.pem
$ chmod -v 0444 ca.pem server-cert.pem cert.pem
```

```
$ mkdir -p /etc/docker/certs
$ cp {ca.pem,server-cert.pem,server-key.pem} /etc/docker/certs
Testen der Zertifikate
Start des Docker daemons von Hand, vorher Service abschalten:
$ service docker stop
$ dockerd --tlsverify \
--tlscacert=/etc/docker/certs/ca.pem \
--tlscert=/etc/docker/certs/server-cert.pem \
--tlskey=/etc/docker/certs/server-key.pem \
-H=0.0.0.0:2376
```

Testen der Verbindung vom lokalen Rechner.

```
$ docker --tlsverify \
--tlscacert=$HOME/.docker/macOS/certs/ca.pem \
--tlscert=$HOME/.docker/macOS/certs/cert.pem \
--tlskey=$HOME/.docker/macOS/certs/key.pem \
-H=176.9.24.187:2376 \
version
```

Dockerservice einrichten
Entfernen der Hostdefinition:

```
$ vi /lib/systemd/system/docker.service
...
ExecStart=/usr/bin/dockerd -H fd://
ExecStart=/usr/bin/dockerd
Anlegen einer Konfigurationsdatei für den Docker daemon:
$ vi /etc/docker/daemon.json
{
  "tlsverify": true,
  "tlscacert": "/etc/docker/certs/ca.pem",
  "tlscert": "/etc/docker/certs/server-cert.pem",
  "tlskey": "/etc/docker/certs/server-key.pem",
  "hosts": ["tcp://0.0.0.0:2376"]
}
```

Neustart des Docker daemons:

```
$ systemctl daemon-reload
$ service docker start
```

Secure by default
If you want to secure your Docker client connections by default, you can move the files to the .docker directory in your home directory – and set the DOCKER_HOST and DOCKER_TLS_VERIFY variables as well (instead of passing -H=tcp://$HOST:2376 and --tlsverify on every call).

```
$ mkdir -pv ~/.docker
$ cp -v {ca,cert,key}.pem ~/.docker
$ append .bashrc
export HOST=127.0.0.7
export DOCKER_HOST=tcp://$HOST:2376 DOCKER_TLS_VERIFY=1
```

Docker will now connect securely by default:

```
$ docker ps
```

Merke: Muss auch auf dem Docker-Host durchgeführt werden.
Portainer mit Docker verbinden
Der eingerichtete Docker daemon kann über einen lokalen Docker Container mit Portainer verwaltet werden

```
$ docker run -d -p 9000:9000 \
-v /Users/fritz/.docker/macOS/certs:/certs \
portainer/portainer \
-H tcp://176.9.24.187:2376 --tlsverify
```