---
source: https://www.ionos.de/digitalguide/server/knowhow/transportschicht/
---
- Die Hauptaufgabe der Transportschicht ist 
	- die Bereitstellung 
		- einer funktionalen und 
		- sicheren End-to-End-Datenübertragung 
	- innerhalb eines Netzwerks. 
- Dafür übernimmt die OSI-Transportschicht 
	- die Daten von der Sitzungsschicht (Layer 5) und 
	- gibt sie dann an die Vermittlungsschicht (Layer 3) weiter. 
- Die Transportschicht kann bei Bedarf 
	- die Daten auch in kleinere Einheiten unterteilen 
	- oder sie in größeren Paketen zusammenfassen, 
	- um sie so einfacher zu transportieren.
- Die maximale Paketgröße (MTU) ist vom physikalischen Medium abhängig:
| Medium               | MTU in Bytes           |
|----------------------|------------------------|
| Hyperchannel         | 65535                  |
| Token Ring(4)(802.5) | 4464                   |
| Token Ring(16)       | 17914                  |
| FDDI                 | 4352                   |
| Ethernet             | 1500                   |
| Gigabit Ethernet     |
| mit Jumboframes      | 9000                   |
| PPPoE (z. B. DSL)    | ≤ 1492                 |
| SLIP/PPP (low delay) | 296                    |
| X.25                 | 576                    |
| FibreChannel         | theoretisch unbegrenzt |
| ISDN                 | 576                    |
| DQDB                 |                        |
| HIPPI                |                        |
| ATM                  | 4500, s. u.            |
| ARCNET               |                        |
| 802.11               | 2312 (WiFi)            |


- Die Übertragungen können dabei 
	- im verbundenen oder 
	- im unverbundenen Modus stattfinden. 
- Die Transportschicht kann 
	- eine Netzwerkverbindung nutzen,
	- eine Verbindung für mehrere Verbindungen verwenden oder 
	- eine Transportverbindung auf verschiedene Netzverbindungen verteilen. 
- Sie agiert dabei aber immer transparent.

- Zu den weiteren Funktionen der Transportschicht gehören auch 
	- der Auf- und Abbau sowie die Überwachung der Verbindung. 
- Erfolgt die Übertragung im Verbindungsmodus, 
	- wird der erfolgreiche Datentransfer durch eine Bestätigung abgesichert. 
- So weiß die Maschine, die die Daten gesendet hat, 
	- dass sämtliche Einheiten wie vorgeschrieben übertragen wurden. 
- Erfolgt die Bestätigung nicht, startet automatisch ein neuer Übertragungsversuch. 
- Dabei nimmt die Transportschicht keine Rücksicht auf die Medien, 
	- die in den ersten drei Schichten verwendet werden.

## Dienste

- Es gibt zahlreiche Dienste, die die OSI-Transportschicht den höheren Ebenen anbietet. 
- Diese sind für unterschiedliche Aspekte des Datentransfers relevant. 
- Zu den wichtigsten Diensten gehören unter anderem folgende:
	- **Verbindungsorientierte Übertragungen**: 
		- Die Transportschicht stellt verbindungsorientierte Übertragungen wie [TCP](https://www.ionos.de/digitalguide/server/knowhow/tcp-vorgestellt/) (Transmission Control Protocol) zur Verfügung. 
		- Dabei vergibt sie Portnummern zwischen 0 und 65.535 und greift auf das oben beschriebene Bestätigungsverfahren zurück.
	- **Verbindungslose Protokolle**: 
		- Im Gegensatz zu den verbindungsorientierten Protokollen verzichten verbindungslose Übertragungen auf die automatische Bestätigung. 
		- So fällt zwar dieser Sicherheitsmechanismus weg, 
			- gerade für Echtzeitübertragungen wie Videokonferenzen/Telefonie ist diese Methode allerdings gut geeignet. 
		- Auch Protokolle wie [UDP](https://www.ionos.de/digitalguide/server/knowhow/udp-user-datagram-protocol/) (User Datagram Protocol) nutzen dabei Ports zwischen 0 und 65.535.
	- **Same Order Delivery**: 
		- Dieser Dienst der Transportschicht stellt sicher, 
			- dass Datenpakete in einer festgelegten Reihenfolge verschickt und 
			- erhalten werden. 
		- Die einzelnen Pakete werden 
			- zu diesem Zweck nummeriert und können 
			- so entsprechend korrekt angeordnet werden.
	- **Integrität der Daten**: 
		- Bei der Übertragung zwischen zwei Systemen können Daten 
			- beschädigt werden, 
			- verloren gehen oder 
			- in einer falschen Reihenfolge beim Empfänger ankommen. 
		- Die Transportschicht nutzt Fehlererkennungscodes und 
			- stellt so sicher, dass die Daten im geplanten Zustand zugestellt werden. 
		- Zu diesem Zweck sendet der Transport Layer 
			- eine Bestätigungsnachricht an den Sender.
	- **Flusskontrolle**: 
		- Die Flusskontrolle reguliert und optimiert den Datenverkehr. 
		- Hierbei kann die Geschwindigkeit 
			- der Übertragung 
				- gedrosselt oder 
				- erhöht werden, 
			- um den Datenaustausch anzupassen. 
		- Dies verhindert, dass der Empfänger überlastet wird.
	- **Stauvermeidung**: 
		- Kommt es dennoch zu Engpässen an Knotenpunkten und Verbindungen, kann die Transportschicht Maßnahmen ergreifen, um eine längerfristige Behinderung zu vermeiden. 
		- Dazu gehört zum Beispiel die Verminderung der Übertragungsrate.
	- **Multiplexing**: 
		- Pakete, die von einem System zum anderen System transferiert werden, können aus vielen unterschiedlichen Quellen stammen. 
		- Durch Multiplexing erlaubt es die Transportschicht 
			- Nutzerinnen und Nutzern, 
			- Anwendungen und 
			- Dienste aus verschiedenen Quellen 
			- innerhalb eines Netzwerks zu öffnen.

## Komponenten
- Firewall
- ?

## Protokolle

- Es gibt zahlreiche Protokolle, die die OSI-Transportschicht nutzen oder früher nutzten. 
- Dazu gehören unter anderem folgende:
	-   DCCP (Datagram Congestion Control Protocol): 
		- Ein Netzwerkprotokoll zur Übertragung 
			- von Medien in IP-Netzen in Echtzeit, 
				- das ohne obligatorische Bestätigungen auskommt.
	-   FCP (Fibre Channel Protocol): 
		- Ein SCSI Interface Protocol 
			- für eine Standardschnittstelle in einem Speichernetzwerk.
	-   IL Protocol: 
		- Eine vereinfachte Form von TCP.
	-   MPTCP (Multipath TCP): 
		- Ein vorgeschlagener Standard, 
			- der mehrere Pfade zusammenschließen soll.
	-   NORM (NACK-Oriented Reliable Multicast): 
		- Für den verlässlichen Transport 
			- in Multicast-Gruppen innerhalb von Netzwerken.
	-   RDP (Reliable Data Protocol): 
		- Ein Transportprotokoll für den Transfer von Bildern und Daten.
	-   RUDP (Reliable User Datagram Protocol): 
		- Ein Protokoll für das Betriebssystem Plan 9.
	-   [SCTP](https://www.ionos.de/digitalguide/server/knowhow/sctp-stream-control-transmission-protocol/) (Stream Control Transmission Protocol): 
		- Ein Netzwerkprotokoll, das auf einem potenziell 
			- unzuverlässigen Paketdienst aufsetzt.
	-   TCP (Transmission Control Protocol): 
		- Ein verbreitetes Netzwerkprotokoll, 
			- das die Art des Datentransfers zwischen Netzwerkkomponenten definiert.
	-   UDP (User Datagram Protocol): 
		- Ein minimalistisches Netzwerkprotokoll, 
			- das den Versand von Datagrammen in IP-basierten Netzen ermöglicht.