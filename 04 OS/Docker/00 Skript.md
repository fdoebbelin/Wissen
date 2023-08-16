# Statische Webseiten mit Nginx #

Get an Image
$ docker pull nginx
Expose the Port
$ docker run --name docker-nginx -p 80:80 nginx
CTRL-C
$ docker rm docker-nginx
Run in Detached Mode
$ docker run --name docker-nginx -p 80:80 -d nginx
$ docker stop docker-nginx
$ docker rm docker-nginx
Building a Web Page to Serve on Nginx
$ mkdir -p ~/Code/test-docker-nginx/html
$ cd ~/Code/test-docker-nginx/html
$ mate index.html
<html>
  <head>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet" integrity="sha256-MfvZlkHCEqatNoGiOXveE8FIwMzZg4W85qfrfIFBfYc= sha512-dTfge/zgoMYpP7QbHy4gWMEGsbsdZeCXz7irItjcC3sPUFtf0kuFbDz/ixG7ArTxmDjLXDmezHubeNikyKGVyQ==" crossorigin="anonymous">
    <title>Docker nginx Tutorial</title>
  </head>
  <body>
    <div class="container">
      <h1>Hello Digital Ocean</h1>
      <p>This nginx page is brought to you by Docker and Digital Ocean</p>
    </div>
  </body>
</html>
Linking the Container to the Local Filesystem
$ docker run --name docker-nginx -p 80:80 -d -v ~/Code/test-docker-nginx/html:/usr/share/nginx/html nginx


----

# Local docker development with virtual hosts #

1) Setup dnsmasq: We are going to configure dnsmasq with a local dns resolver to route every request to *.dev to your local docker instance.
$ brew install dnsmasq
and follow the post-install instructions (or use something else if you prefer)
Find your docker IP, with docker-machine as 'docker-machine ip', or with docker private beta it is just 127.0.0.1

$ echo 'address=/dev/127.0.0.1' >> /usr/local/etc/dnsmasq.conf
$ sudo mkdir -p /etc/resolver
$ echo 'nameserver 127.0.0.1' | sudo tee /etc/resolver/dev
$ brew services restart dnsmasq

restart your computer for the local dns resolver to be recognized

2) Add our automated nginx reverse proxy for docker

$ docker run -d --name nginx -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock:ro jwilder/nginx-proxy
3) Set the VIRTUAL_HOST environment variable on any containers that you want to be accessible via virtual hosts
$ docker run --name docker-nginx -d -e VIRTUAL_HOST=myapp.dev nginx

or in docker-compose...

web:
    expose:
        - "8080"
    environment:
      - VIRTUAL_HOST=myapp.dev

As you add more services or start and stop containers, it can be fun to inspect the nginx configuration on the nginx container, as it changes automagically updates based on events in the internal docker api.
$ docker run -v ~/Code/test-docker-nginx/html:/usr/share/nginx/html -e VIRTUAL_HOST=test.dev nginx


----

# Install Docker on Ubuntu #

Update your apt sources
Update package information, ensure that APT works with the https method, and that CA certificates are installed.
$ apt-get update
$ apt-get install apt-transport-https ca-certificates
Add the new GPG key.
$ apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
$ echo "deb https://apt.dockerproject.org/repo ubuntu-xenial main" | tee /etc/apt/sources.list.d/docker.list
Update the APT package index.
$ apt-get update
Verify that APT is pulling from the right repository.
$ apt-cache policy docker-engine

Prerequisites by Ubuntu Version
Install the recommended packages.
$ apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual

Install Docker.
$ apt-get install docker-engine
Start the docker daemon.
$ service docker start
Verify docker is installed correctly.
$ docker run hello-world

Optional configurations
Enable UFW forwarding
$ apt-get install ufw
$ ufw status
$ vi /etc/default/ufw
DEFAULT_FORWARD_POLICY="ACCEPT"

$ ufw allow ssh
$ ufw allow 80
$ ufw allow 2375/tcp
$ ufw allow 2376/tcp
$ ufw allow 2377/tcp
$ ufw enable

Configure Docker to start on boot¶
$ systemctl enable docker


----

# Install Docker Compose #

Follow the instructions from the release page and run the curl command, which the release page specifies, in your terminal.
$ export dockerComposeVersion=1.13.0
$ curl -L "https://github.com/docker/compose/releases/download/$dockerComposeVersion/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
Apply executable permissions to the binary:
$ chmod +x /usr/local/bin/docker-compose
Installing Command Completion
Bash
Make sure bash completion is installed. If you use a current Linux in a non-minimal installation, bash completion should be available. On a Mac, install with brew install bash-completion
Place the completion script in /etc/bash_completion.d/ (/usr/local/etc/bash_completion.d/ on a Mac), using e.g.
$ curl -L https://raw.githubusercontent.com/docker/compose/$(docker-compose version --short)/contrib/completion/bash/docker-compose > /etc/bash_completion.d/docker-compose
Completion will be available upon next login.
Zsh
Place the completion script in your /path/to/zsh/completion, using e.g. ~/.zsh/completion/
$ mkdir -p ~/.zsh/completion
$ curl -L https://raw.githubusercontent.com/docker/compose/$(docker-compose version --short)/contrib/completion/zsh/_docker-compose > ~/.zsh/completion/_docker-compose
Include the directory in your $fpath, e.g. by adding in ~/.zshrc
fpath=(~/.zsh/completion $fpath)
Make sure compinit is loaded or do it by adding in ~/.zshrc
autoload -Uz compinit && compinit -i
Then reload your shell
$ exec $SHELL -l
Available completions
Depending on what you typed on the command line so far, it will complete
	•	available docker-compose commands
	•	options that are available for a particular command
	•	service names that make sense in a given context (e.g. services with running or stopped instances or services based on images vs. services based on Dockerfiles). For docker-compose scale, completed service names will automatically have “=” appended.
	•	arguments for selected options, e.g. docker-compose kill -s will complete some signals like SIGHUP and SIGUSR1.
Enjoy working with Compose faster and with less typos!



----

# Deployment Container #

In einem Docker Data Volume Container werden die die Quelltexte einer Webapplikation auf dem Server für alle anderen laufenden Container verfügbar gemacht.
	•	Ein PHP-cli-Image wird mit compose Deployer (https://deployer.org) verfügbar gemacht
	•	Mit einem zentralen Git-Repository werden die Quelltexte für das Deployment bereitgestellt.
	•	Die neue Version wird über ein docker exec eingespielt.
	•	Das ganze wird in einem docker-compose Netzwerk zusammengefasst.


----

# Docker Images übertragen #

Transferring a Docker image via SSH, bzipping the content on the fly:
$ docker save <image> | bzip2 | \
     ssh user@host 'bunzip2 | docker load'
It's also a good idea to put pv in the middle of the pipe to see how the transfer is going:
$ docker save <image> | bzip2 | pv | \
     ssh user@host 'bunzip2 | docker load'
First save the docker image to a zip file
$ docker save <docker image name> | gzip > <docker image name>.tar.gz
Then load the exported image to docker using the below command
$ zcat <docker image name>.tar.gz | docker load


----

# Create a swarm #

$ docker swarm init
Swarm initialized: current node (6fwj814xtostgp3cyyy281wbx) is now a manager.

To add a worker to this swarm, run the following command:

    docker swarm join \
    --token SWMTKN-1-1kzb5eaknlfcpk5h1skxor0ct25av4mrh41z0zo8ge8iwbol7u-c7lupgre6qcekuj8ezblw72qs \
    176.9.24.187:2377

To add a manager to this swarm, run 'docker swarm join-token manager' and follow the instructions.
Damit auf den Swarm-Master zugriffen werden kann:
$ ufw allow 2377/tcp


----

# Run portainer #

$ docker run \
-d -p 9000:9000 \
--name=portainer \
-v "/var/run/docker.sock:/var/run/docker.sock" \
portainer/portainer


----

# Run Rancher #

$ docker run -d --restart=unless-stopped -p 8080:8080 rancher/server
$ ufw allow 500/udp
$ ufw allow 4500/udp
$ ufw allow 8080
$ ufw reload
$ open 176.9.24.187:8080
$ docker run --rm --privileged -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/rancher:/var/lib/rancher rancher/agent:v1.2.2 http://176.9.24.187:8080/v1/scripts/CA5E3ABD4DCFCBC1B8F6:1483142400000:HLssjYJpQdwhy6VeW5ba2gCaL0



----

# Protect the Docker daemon socket #

Zertifikat generieren
Die unter macOS mit openssl generierten Certificate sind nicht mit Docker kompatibel, sie müssen auf einem Linux-System generiert werden.
$ ssh metarow
$ openssl genrsa -aes256 -out ca-key.pem 4096
StandardMitZahl

$ openssl req -new -x509 -days 365 -key ca-key.pem -sha256 -out ca.pem
StandartMitZahl
DE
.
Magdeburg
MetaRow UG
.
metarow.com
.

$ openssl genrsa -out server-key.pem 4096

$ openssl req -subj "/CN=metarow.com" -sha256 -new -key server-key.pem -out server.csr
$ echo subjectAltName = DNS:metarow.com,IP:176.9.24.187,IP:127.0.0.1 > extfile.cnf
$ openssl x509 -req -days 365 -sha256 -in server.csr -CA ca.pem -CAkey ca-key.pem \
-CAcreateserial -out server-cert.pem -extfile extfile.cnf

$ openssl genrsa -out key.pem 4096
$ openssl req -subj '/CN=client' -new -key key.pem -out client.csr
$ echo extendedKeyUsage = clientAuth > extfile.cnf
$ openssl x509 -req -days 365 -sha256 -in client.csr -CA ca.pem -CAkey ca-key.pem \
-CAcreateserial -out cert.pem -extfile extfile.cnf
StandardMitZahl
$ rm -v client.csr server.csr
$ chmod -v 0400 ca-key.pem key.pem server-key.pem
$ chmod -v 0444 ca.pem server-cert.pem cert.pem

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

Testen der Verbindung vom lokalen Rechner.
$ docker --tlsverify \
--tlscacert=$HOME/.docker/macOS/certs/ca.pem \
--tlscert=$HOME/.docker/macOS/certs/cert.pem \
--tlskey=$HOME/.docker/macOS/certs/key.pem \
-H=176.9.24.187:2376 \
version
Dockerservice einrichten
Entfernen der Hostdefinition:
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
Neustart des Docker daemons:
$ systemctl daemon-reload
$ service docker start
Secure by default
If you want to secure your Docker client connections by default, you can move the files to the .docker directory in your home directory – and set the DOCKER_HOST and DOCKER_TLS_VERIFY variables as well (instead of passing -H=tcp://$HOST:2376 and --tlsverify on every call).
$ mkdir -pv ~/.docker
$ cp -v {ca,cert,key}.pem ~/.docker
$ append .bashrc
export HOST=127.0.0.7
export DOCKER_HOST=tcp://$HOST:2376 DOCKER_TLS_VERIFY=1
Docker will now connect securely by default:
$ docker ps
Merke: Muss auch auf dem Docker-Host durchgeführt werden.
Portainer mit Docker verbinden
Der eingerichtete Docker daemon kann über einen lokalen Docker Container mit Portainer verwaltet werden
$ docker run -d -p 9000:9000 \
-v /Users/fritz/.docker/macOS/certs:/certs \
portainer/portainer \
-H tcp://176.9.24.187:2376 --tlsverify

----

# A monitoring solution for Docker hosts, containers and containerized services #

I’ve been looking for an open source self-hosted monitoring solution that can provide metrics storage, visualization and alerting for physical servers, virtual machines, containers and services that are running inside containers. After trying out Elastic Beats, Graphite and Prometheus I’ve settled-on Prometheus. The main reason for choosing Prometheus was the support for multi-dimensional metrics and the query language that’s easy to grasp. The fact that you can use the same language for graphing and alerting makes the monitoring task a whole lot easier. Prometheus handles blackbox probing as well as whitebox metrics meaning you can probe your infrastructure and also monitor the internal state of your applications.
Why choose Prometheus:
	•	The whole stack can be deployed using containers
	•	It’s built for distributed systems and infrastructure
	•	Scalable data collection that doesn’t rely on distributed storage
	•	Flexible service discovery (built in support for Kubernetes, Consul, EC2, Azure)
	•	Special-purpose exporters for services like HAProxy, MySQL, PostgreSQL, Memcached, Redis and many more
The Prometheus ecosystem is huge meaning you can find metrics exporters for a wide range of systems: from databases, MQ, HTTP servers to hardware related systems like IoT or IPMI. Whitebox monitoring also has great coverage. There are Prometheus client libraries for Go, Java, Python, Ruby, .NET, PHP and many more programming languages.
Getting started with Prometheus and Docker
If you want to try out the Prometheus stack, take a look at the dockprom repository on GitHub. You can use dockprom as a starting point in developing your own monitoring solution. With dockprom you can, run with one command, the whole stack: Prometheus, Grafana, cAdvisor, NodeExporter and AlertManager.
![][prometheus-on-docker]
Install
Clone dockprom repository on your Docker host, cd into dockprom directory and run compose up:
$ git clone https://github.com/stefanprodan/dockprom
$ cd dockprom
$ docker-compose up -d
Containers:
	•	Prometheus (metrics database) http://<host-ip>:9090
	•	AlertManager (alerts management) http://<host-ip>:9093
	•	Grafana (visualize metrics) http://<host-ip>:3000
	•	NodeExporter (host metrics collector)
	•	cAdvisor (containers metrics collector)
While Grafana supports authentication, the Prometheus and AlertManager services have no such feature. You can remove the ports mapping from the docker-compose file and use NGINX as a reverse proxy providing basic authentication for Prometheus and AlertManager.
Setup Grafana
Navigate to http://<host-ip>:3000 and login with user admin password changeme. You can change the password from Grafana UI or by modifying the user.config file.
From the Grafana menu, choose Data Sources and click on Add Data Source. Use the following values to add the Prometheus container as data source:
	•	Name: Prometheus
	•	Type: Prometheus
	•	Url: http://prometheus:9090
	•	Access: proxy
Now you can import the dashboard temples from the grafana directory.
From the Grafana menu, choose Dashboards and click on Import.
Docker Host Dashboard
![][Grafana_Docker_Host]
The Docker Host Dashboard shows key metrics for monitoring the resource usage of your server:
	•	Server uptime, CPU idle percent, number of CPU cores, available memory, swap and storage
	•	System load average graph, running and blocked by IO processes graph, interrupts graph
	•	CPU usage graph by mode (guest, idle, iowait, irq, nice, softirq, steal, system, user)
	•	Memory usage graph by distribution (used, free, buffers, cached)
	•	IO usage graph (read Bps, read Bps and IO time)
	•	Network usage graph by device (inbound Bps, Outbound Bps)
	•	Swap usage and activity graphs
Docker Containers Dashboard
![][Grafana_Docker_Containers]
The Docker Containers Dashboard shows key metrics for monitoring running containers:
	•	Total containers CPU load, memory and storage usage
	•	Running containers graph, system load graph, IO usage graph
	•	Container CPU usage graph
	•	Container memory usage graph
	•	Container cached memory usage graph
	•	Container network inbound usage graph
	•	Container network outbound usage graph
Note that this dashboard doesn’t show the containers that are part of the monitoring stack.
Monitor Services Dashboard
![][Grafana_Prometheus]
The Monitor Services Dashboard shows key metrics for monitoring the containers that make up the monitoring stack:
	•	Prometheus container uptime, monitoring stack total memory usage, Prometheus local storage memory chunks and series
	•	Container CPU usage graph
	•	Container memory usage graph
	•	Prometheus chunks to persist and persistence urgency graphs
	•	Prometheus chunks ops and checkpoint duration graphs
	•	Prometheus samples ingested rate, target scrapes and scrape duration graphs
	•	Prometheus HTTP requests graph
	•	Prometheus alerts graph
Prometheus memory usage can be controlled by adjusting the local storage memory chunks. You can modify the max chunks value in docker-compose.yml. I’ve set the storage.local.memory-chunks value to 100000, if you monitor 10 containers, then Prometheus will use around 2GB of RAM.
Define alerts
I’ve setup three alerts configuration files:
	•	Monitoring services alerts targets.rules
	•	Docker Host alerts hosts.rules
	•	Docker Containers alerts containers.rules
You can modify the alert rules and reload them by making a HTTP POST call to Prometheus:
curl -X POST http://<host-ip>:9090/-/reload
Monitoring services alerts
Trigger an alert if any of the monitoring targets (node-exporter and cAdvisor) are down for more than 30 seconds:
ALERT monitor_service_down
  IF up == 0
  FOR 30s
  LABELS { severity = "critical" }
  ANNOTATIONS {
      summary = "Monitor service non-operational",
      description = "{{ $labels.instance }} service is down.",
  }
Docker Host alerts
Trigger an alert if the Docker host CPU is under hight load for more than 30 seconds:
ALERT high_cpu_load
  IF node_load1 > 1.5
  FOR 30s
  LABELS { severity = "warning" }
  ANNOTATIONS {
      summary = "Server under high load",
      description = "Docker host is under high load, the avg load 1m is at {{ $value}}. Reported by instance {{ $labels.instance }} of job {{ $labels.job }}.",
  }
Modify the load threshold based on your CPU cores.
Trigger an alert if the Docker host memory is almost full:
ALERT high_memory_load
  IF (sum(node_memory_MemTotal) - sum(node_memory_MemFree + node_memory_Buffers + node_memory_Cached) ) / sum(node_memory_MemTotal) * 100 > 85
  FOR 30s
  LABELS { severity = "warning" }
  ANNOTATIONS {
      summary = "Server memory is almost full",
      description = "Docker host memory usage is {{ humanize $value}}%. Reported by instance {{ $labels.instance }} of job {{ $labels.job }}.",
  }
Trigger an alert if the Docker host storage is almost full:
ALERT hight_storage_load
  IF (node_filesystem_size{fstype="aufs"} - node_filesystem_free{fstype="aufs"}) / node_filesystem_size{fstype="aufs"}  * 100 > 85
  FOR 30s
  LABELS { severity = "warning" }
  ANNOTATIONS {
      summary = "Server storage is almost full",
      description = "Docker host storage usage is {{ humanize $value}}%. Reported by instance {{ $labels.instance }} of job {{ $labels.job }}.",
  }
Docker Containers alerts
Trigger an alert if a container is down for more than 30 seconds:
ALERT jenkins_down
  IF absent(container_memory_usage_bytes{name="jenkins"})
  FOR 30s
  LABELS { severity = "critical" }
  ANNOTATIONS {
    summary= "Jenkins down",
    description= "Jenkins container is down for more than 30 seconds."
  }
Trigger an alert if a container is using more than 10% of total CPU cores for more than 30 seconds:
 ALERT jenkins_high_cpu
  IF sum(rate(container_cpu_usage_seconds_total{name="jenkins"}[1m])) / count(node_cpu{mode="system"}) * 100 > 10
  FOR 30s
  LABELS { severity = "warning" }
  ANNOTATIONS {
    summary= "Jenkins high CPU usage",
    description= "Jenkins CPU usage is {{ humanize $value}}%."
  }
Trigger an alert if a container is using more than 1,2GB of RAM for more than 30 seconds:
ALERT jenkins_high_memory
  IF sum(container_memory_usage_bytes{name="jenkins"}) > 1200000000
  FOR 30s
  LABELS { severity = "warning" }
  ANNOTATIONS {
      summary = "Jenkins high memory usage",
      description = "Jenkins memory consumption is at {{ humanize $value}}.",
  }
Setup alerting
The AlertManager service is responsible for handling alerts sent by Prometheus server. AlertManager can send notifications via email, Pushover, Slack, HipChat or any other system that exposes a webhook interface. A complete list of integrations can be found here.
You can view and silence notifications by accessing http://<host-ip>:9093.
The notification receivers can be configured in alertmanager/config.yml file.
To receive alerts via Slack you need to make a custom integration by choose incoming web hooks in your Slack team app page. You can find more details on setting up Slack integration here.
Copy the Slack Webhook URL into the api_url field and specify a Slack channel.
route:
    receiver: 'slack'

receivers:
    - name: 'slack'
      slack_configs:
          - send_resolved: true
            text: "{{ .CommonAnnotations.description }}"
            username: 'Prometheus'
            channel: '#<channel>'
            api_url: 'https://hooks.slack.com/services/<webhook-id>'
Extending the monitoring system
Dockprom Grafana dashboards can be easily extended to cover more then one Docker host. In order to monitor more hosts, all you need to do is to deploy a node-exporter and a cAdvisor container on each host and point the Prometheus server to scrape those.
You should run a Prometheus stack per data center/zone and use the federation feature to aggregate all metrics in a dedicated Prometheus instance that will serve as an overview of your whole infrastructure. This way, if a zone goes down or the Prometheus instance that does the zones aggregation goes down, your monitoring system present on the remaining zones can still be accessed.
You can also make Prometheus highly available by running two identical Prometheus servers in each zone. Having multiple servers pushing alerts to the same Alertmanager will not result in duplicate alerts, since Alertmanager does deduplication.
If you have any suggestion on improving dockprom please submit an issue or PR on GitHub. Contributions are more than welcome!

----

# meine Docker Kommandos #

Ein Image umbenennen
$ docker tag my-php fdoebbelin/php5
$ docker rmi my-php
Ein neues Image erzeugen
$ docker build -t fdoebbelin/php5 .
$ docker run --name test-php -p 80:80 -d -v /Users/fritz/Desktop/my_php/api/:/var/www -e APACHE_DOCROOT=/var/www/public fdoebbelin/php5
Kommando in einem laufen Container ausführen, interaktive Shell
$ docker exec -it test-php /bin/bash


----

# wichtige Links #

Docker Compose UI
http://francescou.github.io/docker-compose-ui/


Portainer | Simple management UI for Docker
https://www.portainer.io/

[prometheus-on-docker]: prometheus-on-docker.png width=600px height=336px

[Grafana_Docker_Host]: Grafana_Docker_Host.png width=679px height=912px

[Grafana_Docker_Containers]: Grafana_Docker_Containers.png width=741px height=1024px

[Grafana_Prometheus]: Grafana_Prometheus.png