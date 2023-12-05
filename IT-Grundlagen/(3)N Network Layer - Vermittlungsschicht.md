---
source: https://www.ionos.de/digitalguide/server/knowhow/vermittlungsschicht/
---
- Die Vermittlungsschicht ist zuständig für 
	- die korrekte Adressierung, 
	- die für den Verbindungsaufbau innerhalb eines Netzwerk wichtig ist. 
- So ermöglicht sie zwei Teilnehmern 
	- die sichere Verknüpfung miteinander, 
	- wobei die Kommunikation auch über 
		- verschiedene Netze verlaufen kann.

## Funktionen

- Die Voraussetzung dafür, 
	- dass zwei unterschiedliche Systeme in einem Netzwerk 
		- miteinander kommunizieren und 
		- Daten austauschen können,
	- ist die **korrekte Adressierung**. 
- Die Vermittlungsschicht 
	- bietet zu diesem Zweck unterschiedliche 
		- Dienste und 
		- Funktionen an, 
	- die sie insbesondere der Transportschicht (Layer 4) zur Verfügung stellt.

- Die Hauptaufgabe des Network Layers besteht somit 
	- sowohl in der namensgebenden Vermittlung, 
	- als auch im Auf- und Abbau einer Verbindung.
- Dafür werden gesicherte Systemverbindungen miteinander verknüpft, 
	- selbst wenn diese dafür über mehrere Netze geführt werden müssen. 
- Die Vermittlungsschicht 
	- trifft in diesem Fall eine Wegwahl und 
	- stellt den höheren Ebenen 
		- dann eine transparente Verbindung 
		- zwischen Quelle und Zielsystem zur Verfügung.

- Zu den weiteren Funktionen der Vermittlungsschicht gehören 
	- Flusskontrolle, 
	- die Fehleranalyse und -behebung 
	- sowie die Überwachung der physikalischen Verbindung. 
- Die Flusskontrolle erlaubt unter anderem 
	- die Pufferung der übertragenen Daten, 
	- falls der Datenfluss von Empfängerseite unterbrochen wird. 
- Dazu passt die OSI-Vermittlungsschicht 
	- die Größe der Datenpakete 
		- an die Gegebenheiten des jeweiligen Netzes an, 
	- um so eine möglichst reibungslose Übertragung 
		- zu ermöglichen.

- Bei paketorientierten Diensten 
	- ist die Vermittlungsschicht außerdem 
	- für die Stauvermeidung mitverantwortlich. 
- Der Network Layer kann 
	- sowohl verbindungslose 
	- als auch verbindungsorientierte Netzwerke unterstützen, 
		- dabei allerdings immer nur einen Typ gleichzeitig bedienen.

## Dienste

- Die Vermittlungsschicht bietet 
	- zahlreiche unterschiedliche Dienste an. 
- Ist keine direkte Kommunikation 
	- zwischen Sender und Empfänger möglich, 
	- sorgt die OSI-Vermittlungsschicht dafür, 
		- dass die einzelnen Pakete 
			- zunächst an Knotenpunkte weitergeleitet werden, 
		- nicht aber in die höheren Ebenen gelangen.

- Neben den Netzverbindungen 
	- stellt die Vermittlungsschicht auch 
	- die passenden Netzadressen zur Verfügung. 
- Diese Adressen sind 
	- einzigartig und 
	- hierarchisch strukturiert. 
- Zu den weiteren Diensten gehören 
	- die eigentliche Übertragung von Dateneinheiten und 
	- die Identifizierung 
		- der relevanten Verbindungspunkte 
		- zwischen Sender und Empfänger. 
- Im Gegensatz zur Sicherungsschicht (Layer 2) 
	- können sich die Informationen der Vermittlungsschicht 
	- über die Grenzen des lokalen Netzwerks bewegen.
## Komponenten

- Router
- Layer-3-Switch

## Protokolle

- Zahlreiche Protokolle nutzen oder nutzten die Vermittlungsschicht. 
- Dazu gehören unter anderem:
	- CLNS (Connectionless-mode Network Service): 
		- Ein Netzwerkprotokoll für den Einsatz in administrierten Telekommunikationsnetzen.
	- DDP (Datagram Delivery Protocol): 
		- Ein Datenübertragungsprotokoll von AppleTalk.
	- EGP (Exterior Gateway Protocol): 
		- Ein Protokoll, welches die Erreichbarkeit von Netzen aus zwei verschiedenen autonomen Systemen überprüft.
	- EIGRP (Enhanced Interior Gateway Routing Protocol): 
		- Ein Protokoll, welches Router und Routen zwischen zwei Netzwerken speichert.
	- [ICMP](https://www.ionos.de/digitalguide/server/knowhow/igmp-internet-group-management-protocol/) (Internet Control Message Protocol): 
		- Ein Protokoll zum Austausch von Informationen und Fehlermeldungen in Netzwerken. Gehört zu IPv4.
	- [IGMP](https://www.ionos.de/digitalguide/server/knowhow/igmp-internet-group-management-protocol/) (Internet Group Management Protocol): 
		- Ein Netzwerkprotokoll zur Organisation von Gruppenkommunikation.
	- [IPsec](https://www.ionos.de/digitalguide/server/knowhow/ipsec-sicherheitsarchitektur-fuer-ipv4-und-ipv6/) (Internet Protocol Security): 
		- Ein Protokollstapel, der eine sichere Verbindung in potenziell unsicheren Netzen ermöglichen soll.
	- IPv4: 
		- Das [Internet Protocol](https://www.ionos.de/digitalguide/server/knowhow/was-ist-das-internet-protocol-definition-von-ip-co/) (IP) der Version 4 und der ehemalige Standard.
	- [IPv6](https://www.ionos.de/digitalguide/server/knowhow/welche-vorteile-bietet-ipv6/): 
		- Der neuere Internetstandard, der den Adressraum von 32 auf 128 Bit ausweitet.
	- IPX (Internetwork Packet Exchance): 
		- Ein Netzwerkprotokoll, welches vor allem für das Betriebssystem NetWare eingesetzt wird.
	- OSPF (Open Shortest Path First): 
		- Ein Routing-Protokoll von IETF für den Einsatz in großen Unternehmensnetzen.
	- NetBEUI (NetBIOS Extended User Interface): 
		- Ein Netzwerkprotokoll, welches durch TCP/IP mittlerweile allerdings überholt ist.
	- PIM (Protocol Independent Multicast): 
		- Ein Verfahren für dynamisches Routing in der Gruppenkommunikation.
	- RIP (Routing Information Protocol): 
		- Ein Routing-Protokoll für den Einsatz innerhalb eines autonomen Systems.
	- X.25: 
		- Eine Protokollfamilie für Wide Area Networks, 
		- die ebenfalls die Vermittlungsschicht verwendet.