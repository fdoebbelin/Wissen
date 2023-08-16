### Einführung

[Docker](https://www.docker.com/) ist eine Anwendung, die die Verwaltung von Anwendungsprozessen in *Containern* vereinfacht. In Containern können Anwendungen in ressourcenisolierten Prozessen ausgeführt werden. Container ähneln virtuellen Computern, sind jedoch besser portierbar, ressourcenfreundlicher und stärker vom Host-Betriebssystem abhängig.

Eine ausführliche Einführung in die unterschiedlichen Komponenten eines Docker-Containers ist [The Docker Ecosystem: An Introduction to Common Components](https://www.digitalocean.com/community/tutorials/the-docker-ecosystem-an-introduction-to-common-components) (Das Docker Ökosystem: Eine Einführung in allgemeine Komponenten) zu entnehmen.

In diesem Tutorial installieren und verwenden Sie Docker Community Edition (CE) unter Ubuntu 20.04. Sie installieren Docker selbst, arbeiten mit Containern und Images und verschieben ein Image in ein Docker-Repository.

## Voraussetzungen

Um dieses Tutorial zu absolvieren, benötigen Sie Folgendes:

- Einen Ubuntu 20.04-Server, der gemäß des [Leitfadens zur Ersteinrichtung des Servers für Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20.04) eingerichtet wurde, einschließlich eines sudo Nicht-root-Benutzers und einer Firewall.
- Einen Account auf [Docker Hub](https://hub.docker.com/), wenn Sie eigene Images erstellen und sie nach Docker Hub verschieben möchten, wie in Schritt 7 und 8 gezeigt.

## Schritt 1 — Installieren von Docker

Das im offiziellen Ubuntu-Repository verfügbare Docker-Installationspaket ist möglicherweise nicht die neueste Version. Um die neueste Version zu erhalten, installieren wir Docker aus dem offiziellen Docker-Repository. Dazu fügen wir eine neue Paketquelle hinzu, fügen den GPG-Schlüssel von Docker hinzu, um sicherzustellen, dass die Downloads gültig sind, und installieren das Paket dann.

Aktualisieren Sie zuerst Ihre bestehende Liste der Pakete:

Installieren Sie als Nächstes einige vorausgesetzte Pakete, damit `apt` Pakete über HTTPS nutzen kann:

Fügen Sie Ihrem System dann den GPG-Schlüssel für das offizielle Docker-Repository hinzu:

Fügen Sie das Docker-Repository zu APT-Quellen hinzu:

Aktualisieren Sie als Nächstes die Paketdatenbank mit den Docker-Paketen aus dem neu hinzugefügten Repo:

Stellen Sie sicher, dass Sie aus dem Docker Repo und nicht aus dem Standard-Ubuntu-Repo installieren:

Sie sehen eine Ausgabe wie diese, wobei die Versionsnummer für Docker möglicherweise abweicht:

Output of apt-cache policy docker-ce

Beachten Sie, dass `docker-ce` nicht installiert ist, aber der Kandidat für die Installation aus dem Docker-Repository für Ubuntu 20.04 (`focal`) kommt.

Installieren Sie abschließend Docker:

Docker sollte jetzt installiert, der daemon gestartet und der Prozess zum Starten beim Booten aktiviert sein. Überprüfen Sie, ob er ausgeführt wird:

Die Ausgabe sollte in etwa wie folgt aussehen und anzeigen, dass der Dienst aktiv ist und ausgeführt wird:

```
Output● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Tue 2020-05-19 17:00:41 UTC; 17s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 24321 (dockerd)
      Tasks: 8
     Memory: 46.4M
     CGroup: /system.slice/docker.service
             └─24321 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

```

Durch Installieren von Docker erhalten Sie nicht nur den Docker-Dienst (daemon), sondern auch das `Docker`-Befehlszeilendienstprogramm oder den Docker-Client. Wir befassen uns im Laufe dieses Tutorials damit, wie Sie den Befehl `docker` verwenden.

## Schritt 2 — Ausführen des Befehls docker ohne Sudo (optional)

Der Befehl `docker` kann standardmäßig nur durch den **root**-Benutzer oder einen Benutzer in der **docker**-Gruppe ausgeführt werden, die beim Installationsprozess von Docker automatisch erstellt wird. Wenn Sie versuchen, den Befehl `docker` auszuführen, ohne ihm `sudo` voranzustellen oder ohne Teil der **docker** Gruppe zu sein, erhalten Sie eine Ausgabe ähnlich wie die Folgende:

```
Outputdocker: Cannot connect to the Docker daemon. Is the docker daemon running on this host?.
See 'docker run --help'.

```

Wenn Sie `sudo` immer bei Ausführen des Befehls `docker` eingeben möchten, fügen Sie der `docker` Gruppe Ihren Benutzernamen hinzu:

Um die neue Gruppenmitgliedschaft anzuwenden, melden Sie sich beim Server ab und wieder an oder geben Sie Folgendes ein:

Sie werden aufgefordert, das Benutzerpasswort einzugeben, um fortzufahren.

Bestätigen Sie, dass Ihr Benutzer der Gruppe **docker** jetzt hinzugefügt wird, indem Sie Folgendes eingeben:

```
Outputsammy sudo docker

```

Wenn Sie der `docker`-Gruppe einen Benutzer hinzufügen müssen, als der Sie nicht angemeldet sind, erklären Sie diesen Benutzernamen ausdrücklich wie folgt:

Im restlichen Artikel wird davon ausgegangen, dass Sie den Befehl `docker` als ein Benutzer in der **docker**-Gruppe ausführen. Sollten dies anders sein, setzen Sie bitte `sudo` vor die Befehle.

Wir behandeln als Nächstes den Befehl `docker`.

## Schritt 3 — Verwenden des Befehls docker

Die Verwendung von `docker` besteht darin, eine Kette von Optionen und Befehlen zu übergeben, gefolgt von Argumenten. Die Syntax übernimmt diese Form:

Um alle verfügbaren Unterbefehle zu sehen, geben Sie Folgendes ein:

Ab Docker 19 enthält die vollständige Liste der verfügbaren Unterbefehle:

```
Output  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes


```

Um die Optionen für einen bestimmten Befehl zu sehen, geben Sie Folgendes ein:

Um systemweite Informationen zu Docker zu sehen, verwenden Sie Folgendes:

Wir wollen uns einige dieser Befehle näher ansehen. Wir wollen zunächst mit Images arbeiten.

## Schritt 4 — Arbeiten mit Docker-Images

Docker-Container werden aus Docker-Images erstellt. Standardmäßig holt Docker diese Images aus [Docker Hub](https://hub.docker.com/), einer Docker-Registrierung, die durch Docker, verwaltet wird, jenem Unternehmen, das hinter dem Docker-Projekt steht. Jeder kann seine Docker-Images auf Docker Hub hosten, sodass die meisten Anwendungen und Linux-Distributionen, die Sie benötigen, dort Images gehostet haben.

Um zu prüfen, ob Sie Images von Docker Hub aufrufen und herunterladen können, geben Sie Folgendes ein:

Die Ausgabe gibt an, dass Docker korrekt funktioniert:

```
OutputUnable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
0e03bdcc26d7: Pull complete
Digest: sha256:6a65f928fb91fcfbc963f7aa6d57c8eeb426ad9a20c7ee045538ef34847f44f1
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

...


```

Docker konnte zunächst das Image `hello-world` lokal nicht finden. Daher hat es das Image aus Docker Hub, dem Standard-Repository, heruntergeladen. Sobald das Image heruntergeladen wurde, hat Docker einen Container aus dem Image und der Anwendung innerhalb des ausgeführten Containers erstellt und zeigt die Nachricht an.

Sie können auf Docker Hub nach verfügbaren Images suchen, indem Sie den Befehl `docker` mit dem Unterbefehl `search` verwenden. Um zum Beispiel nach Ubuntu zu suchen, geben Sie Folgendes ein:

Das Skript schleicht sich in Docker Hub ein und gibt eine Auflistung aller Images zurück, deren Name mit der Suchfolge übereinstimmt. In diesem Fall sieht die Ausgabe etwa wie folgt aus:

```
OutputNAME                                                      DESCRIPTION                                     STARS               OFFICIAL            AUTOMATED
ubuntu                                                    Ubuntu is a Debian-based Linux operating sys…   10908               [OK]
dorowu/ubuntu-desktop-lxde-vnc                            Docker image to provide HTML5 VNC interface …   428                                     [OK]
rastasheep/ubuntu-sshd                                    Dockerized SSH service, built on top of offi…   244                                     [OK]
consol/ubuntu-xfce-vnc                                    Ubuntu container with "headless" VNC session…   218                                     [OK]
ubuntu-upstart                                            Upstart is an event-based replacement for th…   108                 [OK]
ansible/ubuntu14.04-ansible                               Ubuntu 14.04 LTS with
...


```

In der Spalte **OFFICIAL** gibt **OK** ein Image an, das von dem Unternehmen, das hinter dem Projekt steht, erstellt wurde und durch das es unterstützt wird. Wenn Sie das Image identifiziert haben, das Sie verwenden möchten, können Sie es mithilfe des Unterbefehls `pull` auf Ihren Computer herunterladen.

Führen Sie den folgenden Befehl aus, um das offizielle `ubuntu`-Image auf Ihren Computer zu laden:

Sie sehen die folgende Ausgabe:

```
OutputUsing default tag: latest
latest: Pulling from library/ubuntu
d51af753c3d3: Pull complete
fc878cd0a91c: Pull complete
6154df8ff988: Pull complete
fee5db0ff82f: Pull complete
Digest: sha256:747d2dbbaaee995098c9792d99bd333c6783ce56150d1b11e333bbceed5c54d7
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest

```

Nachdem ein Image heruntergeladen wurde, können Sie einen Container mit dem heruntergeladenen Image mit dem Unterbefehl `run` ausführen. Wie am Beispiel `hello-world` gezeigt, lädt der Docker-Client das Image zunächst herunter, sofern noch kein Image heruntergeladen wurde, wenn `Docker` über den Unterbefehl `run` ausgeführt wird. Danach wird ein Container ausgeführt, der es nutzt.

Um die Images zu sehen, die auf Ihren Computer heruntergeladen wurden, geben Sie Folgendes ein:

Die Ausgabe sieht etwa wie folgt aus:

```
OutputREPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              1d622ef86b13        3 weeks ago         73.9MB
hello-world         latest              bf756fb1ae65        4 months ago        13.3kB

```

Wie Sie in diesem Tutorial noch sehen werden, können Images, die Sie zum Ausführen von Containern verwenden, geändert und zum Erstellen neuer Images genutzt werden, die dann in Docker Hub oder andere Docker-Registrierungen hochgeladen (*gepusht* ist der technische Begriff) werden.

Wir wollen uns näher ansehen, wie Container ausgeführt werden.

## Schritt 5 — Ausführen eines Docker-Containers

Der im vorherigen Schritt ausgeführte `hello-world` Container ist ein Beispiel für einen Container, der nach Ausgabe einer Testnachricht ausgeführt und geschlossen wird. Container können jedoch so viel sinnvoller sein und außerdem interaktiv. Sie ähneln virtuellen Maschinen, sind jedoch ressourcenfreundlicher.

Wir führen zum Beispiel einen Container mit dem neueste Image von Ubuntu aus. Die Kombination der **-i** und **-t**-Schalter gibt Ihnen interaktiven Shellzugriff in den Container:

Ihre Befehlsaufforderung sollte sich so ändern, dass sie wiedergibt, dass Sie jetzt innerhalb des Containers arbeiten, und sollte wie folgt aussehen:

```
Outputroot@d9b100f2f636:/#

```

Beachten Sie die Container-ID in der Befehlsaufforderung. In diesem Beispiel ist es `d9b100f2f636`. Sie brauchen diese Container-ID später, um den Container zu identifizieren, wenn Sie ihn entfernen möchten.

Sie können nun jeden beliebigen Befehl innerhalb des Containers ausführen. Wir wollen zum Beispiel die Paketdatenbank im Container aktualisieren. Sie brauchen keinem Befehl `sudo` voranstellen, da Sie innerhalb des Containers als **root**-Benutzer arbeiten:

Installieren Sie anschließend eine beliebige Anwendung darin. Wir wollen Node.js installieren:

Damit wird Node.js aus dem offiziellen Ubuntu Repository im Container installiert. Wenn die Installation beendet ist, überprüfen Sie, ob Node.js installiert ist:

Sie sehen dann, dass die Versionsnummer in Ihrem Terminal angezeigt wird:

```
Outputv10.19.0

```

Alle Änderungen, die Sie innerhalb des Containers vornehmen, gelten nur für diesen Container.

Um den Container zu beenden, geben Sie `exit` in die Eingabeaufforderung ein.

Wir wollen uns als Nächstes die Verwaltung der Container auf unserem System ansehen.

## Schritt 6 — Verwalten von Docker-Containern

Wenn Sie Docker eine zeitlang nutzen, gibt es viele aktive (ausgeführte) und inaktive Container auf Ihrem Computer. So können Sie die **aktiven** anzeigen:

Sie werden eine Ausgabe ähnlich der Folgenden sehen:

```
OutputCONTAINER ID        IMAGE               COMMAND             CREATED             


```

In diesem Tutorial haben Sie zwei Container gestartet: einen aus dem `hello-world` Image und einen anderen aus dem `ubuntu` Image Beide Container laufen nicht mehr, sind jedoch immer noch auf Ihrem System.

Um alle Container – aktive und inaktive –zu sehen, führen Sie `docker ps` mit dem Schalter `a` aus:

Sie sehen eine Ausgabe, die dieser ähnelt:

```
1c08a7a0d0e4        ubuntu              "/bin/bash"         2 minutes ago       Exited (0) 8 seconds ago                       quizzical_mcnulty
a707221a5f6c        hello-world         "/hello"            6 minutes ago       Exited (0) 6 minutes ago                       youthful_curie


```

Um den neuesten Container zu sehen, den Sie erstellt haben, übergeben Sie ihm den `l` Schalter:

Um einen gestoppten Container zu starten, verwenden Sie `docker start`, gefolgt von der Container-ID oder dem Namen des Containers. Wir starten den Ubuntu-basierten Container mit der ID `1c08a7a0d0e4`:

Der Container startet. Sie können mit `docker ps` seinen Status anzeigen:

```
OutputCONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
1c08a7a0d0e4        ubuntu              "/bin/bash"         3 minutes ago       Up 5 seconds                            quizzical_mcnulty


```

Mit `docker stop`, gefolgt von Container-ID oder Namen, können Sie einen laufenden Container stoppen. Diesmal nutzen wir den Namen, den Docker dem Container zugewiesen hat, nämlich `quizzical_mcnulty`:

Sobald Sie entschieden haben, dass Sie einen Container nicht mehr benötigen, löschen Sie ihn mit dem Befehl `docker rm`, auch hier wieder entweder mit der Container-ID oder dem Namen. Verwenden Sie den Befehl `docker ps -a`, um die Container-ID oder den Namen für den Container zu finden, der mit dem Image `hello world` verknüpft ist, und löschen Sie ihn.

Sie können einen neuen Container starten und ihm mit dem `--name` Schalter einen Namen geben. Sie können auch den `--rm` Schalter nutzen, um einen Container zu erstellen, der sich selbst löscht, wenn er gestoppt wird. Weitere Informationen zu diesen Optionen und anderen erhalten Sie mit dem Befehl `docker run help`.

Container können in Images verwandelt werden, die zur Erstellung neuer Container genutzt werden können. Wir wollen uns nun ansehen, wie das funktioniert.

## Schritt 7 — Committen von Änderungen in einem Container mit einem Docker-Image

Wenn Sie ein Docker-Image starten, können Sie Dateien so erstellen, ändern und löschen, wie mit einer virtuellen Maschine. Die Änderungen, die Sie vornehmen, werden nur auf diesen Container angewendet. Sie können ihn starten und stoppen. Sobald Sie ihn mit dem Befehl `docker rm` zerstören, gehen die Änderungen jedoch verloren.

Dieser Abschnitt zeigt Ihnen, wie der Status eines Containers als neues Docker-Image gespeichert wird.

Nach der Installation von Node.js im Ubuntu-Container haben Sie nun einen Container, der aus einem Image läuft. Der Container unterscheidet sich jedoch von dem Image, das Sie genutzt haben, um ihn zu erstellen. Sie haben die Möglichkeit, den Node.js-Container später als Basis für neue Images wiederzuverwenden.

Verknüpfen Sie die Änderungen mit einer neuen Docker-Image-Instanz über folgenden Befehl.

Der **-m**-Schalter dient der Commit-Nachricht, die Ihnen und anderen anzeigt, welche Änderungen Sie vorgenommen haben, während **-a** zur Angabe des Autors verwendet wird. Die `container_id` wurde bereits zuvor im Tutorial erwähnt, als Sie die interaktive Docker-Session gestartet haben. Sofern Sie weitere Repositorys auf Docker Hub erstellt haben, ist das `Repository` in der Regel Ihr Docker-Hub-Benutzername.

So lautet beispielsweise der Befehl für den Benutzer **sammy** mit der Container-ID `d9b100f2f636`:

Wenn Sie ein Image *verknüpfen*, wird das neue Image lokal auf Ihrem Computer gespeichert. Später erfahren Sie in diesem Tutorial, wie Sie ein Image in eine Docker-Registrierung wie Docker Hub verschieben, damit andere darauf zugreifen können.

Durch das erneute Auflisten der Docker-Images sieht man das neue Image sowie das alte, von dem es abgeleitet wurde:

Die Ausgabe sieht dann so aus:

```
OutputREPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
sammy/ubuntu-nodejs   latest              7c1f35226ca6        7 seconds ago       179MB
...


```

In diesem Beispiel ist `ubuntu-nodejs` das neue Image, das aus dem bestehenden `ubuntu`-Image von Docker Hub abgeleitet wurde. Der Größenunterschied spiegelt die vorgenommenen Änderungen wider. Und in diesem Beispiel war die Änderung die Installation von NodeJS. Wenn Sie nun beim nächsten Mal einen Container mit Ubuntu ausführen wollen, in dem NodeJS vorinstalliert ist, können Sie ganz einfach das neue Image nutzen.

Sie können außerdem Images aus einer `Dockerfile` erstellen. Damit lässt sich die Installation von Software in einem neuen Image automatisieren. Das würde jedoch über den Rahmens dieses Tutorials hinausgehen.

Wir wollen nun das neue Image mit anderen teilen, damit sie daraus Container erstellen können.

## Schritt 8 — Verschieben von Docker-Images in ein Docker-Repository

Der nächste logische Schritt nach dem Erstellen eines neuen Images aus einem bestehenden Image besteht darin, es mit einigen wenigen Auserwählten, mit der ganzen Welt oder einer anderen Docker-Registrierung zu teilen, zu der Sie Zugriff haben. Um ein Image auf Docker Hub oder in eine andere Docker-Registrierung zu verschieben, müssen Sie dort ein Konto haben.

Dieser Abschnitt zeigt Ihnen, wie ein Docker-Image in Docker Hub verschoben wird. Um zu erfahren, wie Sie Ihre private Docker-Registrierung erstellen, lesen Sie [Einrichten einer privaten Docker-Registrierung unter Ubuntu 14.04​​](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-private-docker-registry-on-ubuntu-14-04).

Um Ihr Image zu verschieben, melden Sie sich zuerst in Docker Hub an.

Sie werden aufgefordert, sich mit Ihrem Docker-Hub-Passwort zu authentifizieren. Wenn Sie das korrekte Passwort angegeben haben, sollte die Authentifizierung erfolgreich sein.

**Anmerkung:** Wenn der Benutzername Ihrer Docker-Registrierung sich von Ihrem lokalen Benutzernamen unterscheidet, den Sie zur Erstellung des Image verwendet haben, müssen Sie das Image mit Ihrem Registrierungsbenutzernamen kennzeichnen. Für das im letzten Schritt angegebene Beispiel geben Sie Folgendes ein:

Dann können Sie Ihr eigenes Image wie folgt verschieben:

Um das `ubuntu-nodejs` Image in das **sammy** Repository zu verschieben, brauchen Sie den Befehl:

Der Vorgang kann möglicherweise einige Zeit dauern, um die Images hochladen zu können. Wenn er abgeschlossen ist, sieht die Ausgabe wie folgt aus:

```
OutputThe push refers to a repository [docker.io/sammy/ubuntu-nodejs]
e3fbbfb44187: Pushed
5f70bf18a086: Pushed
a3b5c80a4eba: Pushed
7f18b442972b: Pushed
3ce512daaf78: Pushed
7aae4540b42d: Pushed

...



```

Nach dem Verschieben eines Image in eine Registrierung sollte es, wie unten dargestellt, wie im Dashboard Ihres Kontos aufgelistet sein.

<img width="741" height="265" src="../../_resources/ec2vX3Z_9a3904e45a714e41ad175fc415490216.png"/>

Wenn das Verschieben zu einem solchen Fehler führt, haben Sie sich wahrscheinlich nicht angemeldet:

```
OutputThe push refers to a repository [docker.io/sammy/ubuntu-nodejs]
e3fbbfb44187: Preparing
5f70bf18a086: Preparing
a3b5c80a4eba: Preparing
7f18b442972b: Preparing
3ce512daaf78: Preparing
7aae4540b42d: Waiting
unauthorized: authentication required

```

Melden Sie sich mit dem `docker login` an und wiederholen Sie den Versuch. Überprüfen Sie dann, ob es auf Ihrer Docker-Hub-Repository-Seite vorhanden ist.

Sie können nun mit `docker pull sammy/ubuntu-nodejs` das Image auf eine neuen Rechner ziehen und zum Ausführen eines neuen Containers verwenden.

## Zusammenfassung

In diesem Tutorial haben Sie Docker installiert, mit Images und Containern gearbeitet und ein modifiziertes Image auf Docker Hub verschoben. Nachdem Sie nun die Grundlagen kennen, empfehlen wir die [anderen Docker-Tutorials](https://www.digitalocean.com/community/tags/docker?type=tutorials) in der DigitalOcean Community.