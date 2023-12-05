- Die Anwendungsschicht regelt die Kommunikation 
	- verschiedener Anwendungsprogramme innerhalb eines Netzwerks. 
- Die OSI-Anwendungsschicht kann 
	- allgemeine und 
	- benutzerorientiere Dienste ausführen und 
	- wird von zahlreichen Protokollen genutzt.

## Funktionen

- Die Anwendungsschicht ermöglicht eine 
	- effiziente und 
	- sichere Kommunikation zwischen 
	- verschiedenen Anwendungsprogrammen 
		- innerhalb eines Netzwerks. 
- Dabei fungiert sie selbst nicht als Anwendung, 
	- sondern bietet nur unterschiedliche Funktionen an. 
- Dazu gehören:
	- **Identifikation**: 
		- Hierbei stellt die OSI-Anwendungsschicht sicher, dass 
			- die Seite, die erreicht werden soll, 
				- einerseits erreicht werden kann und sich 
				- andererseits klar und ohne Einschränkungen identifizieren lässt.
	- **Authentifizierung**: 
		- Die Anwendungsschicht bestimmt 
			- zum Beispiel im Falle einer Kommunikation per E-Mail 
				- den Absender und 
				- den Empfänger einer Nachricht 
				- oder auch nur einen von beiden.
	- **Analyse**: 
		- Über die Anwendungsschicht wird sichergestellt, 
			- dass die nötigen Voraussetzungen gegeben sind, 
			- damit zwei Systeme miteinander kommunizieren können. 
		- Dazu gehört zum Beispiel die Überprüfung, 
			- ob eine aktive Netzwerkverbindung vorhanden ist.
	- **Sicherheit**: 
		- Der Application Layer überprüft auf beiden Seiten 
			- der Kommunikationssysteme, 
				- dass Protokolle und Prozeduren 
					- im Bereich der Privatsphäre, 
					- des Zustands der Daten und 
					- möglicher Fehlerlösungen eingehalten und 
					- in Einklang gebracht werden.
	- **Überwachung**: 
		- Die Anwendungsebene überwacht 
			- die Datensyntaxregeln und stellt sicher, dass 
			- das Netzwerkprotokoll während der Interaktion eingehalten wird.

## Dienste

- Die Anwendungsschicht führt verschiedene Dienste aus, 
	- wobei die Grunddienste ursprünglich in zwei große Kategorien unterteilt wurden: 
		- CASE (Common Application Service Elements) und 
		- SASE (Specific Application Service Elements).

### CASE in der Anwendungsschicht

- CASE bezeichnet dabei allgemeine Funktionen, die 
	- die Koordination anderer Protokolle regeln und 
	- somit auch den Unterbau für SASE bilden. 
- Zu den Standardanwendungen gehören unter anderem 
	- Auftragstransfer, 
	- Datentransfer und 
	- E-Mail-Funktionen. 
- Ein Beispiel für CASE 
	- im Bereich der Anwendungsschicht 
	- wären Verzeichnisdienste. 
- Diese können eine Verteilerliste erstellen, 
	- einen Server für eine bestimmte Dienstleistung oder 
	- Aktion bestimmen oder 
	- Namen und Adressen zuordnen.

### SASE in der Anwendungsschicht

- Im Gegensatz dazu handelt es sich bei SASE um benutzerorientierte Funktionen, die anwendungsspezifisch sind und in vielen Fällen auf CASE aufbauen. 
- Hierzu können unter anderem **benutzerorientierte Verzeichnisse, virtuelle Terminals, Datentransfer, E-Mail oder die Übertragung von Grafiken und Medien** gehören.

- Während die beiden Dienste zunächst in der Planung strikt getrennt waren, 
	- gibt es in der Praxis durch das Zusammenspiel von SASE und CASE und die Abhängigkeit des einen vom anderen große Überschneidungen. 
- Daher definiert man häufig auch beide zusammen als 
	- Anwendungssteuerungs-Dienstelemente (ACSE).

## Protokolle

Es gibt zahlreiche Protokolle, die die OSI-Anwendungsschicht verwenden. Die bekanntesten davon dürften die TCP/IP-Protokolle sein, die die Grundlage für das Internet und die Kommunikation in Netzwerken bilden. Unter anderem nutzen folgende Programme den Application Layer:

- HTTP (80)
	- Hypertext Transfer Protocol: 
		- Wird zur Übertragung von HTML-Seiten genutzt.
- HTTPS (443)
	- Hypertext Transfer Protocol: 
		- Die verschlüsselte Version eines Übertragungsprotokolls.
- FTP (21)
	- File Transfer Protocol: 
		- FTP ermöglicht den Datenaustausch zwischen zwei Rechnern, 
		- auch wenn sich diese hinsichtlich 
			- ihrer Bauweise und 
			- ihres Betriebssystems unterscheiden.
- TFTP (69)
	- Trivial File Transfer Protocol: 
		- Ähnelt FTP, setzt allerdings auf UDP auf.
- SMTP (25)
	- Simple Mail Transfer Protocol): 
		- Ermöglicht den Austausch von E-Mails zwischen zwei Rechnern.
- IMAP (143)
	- Internet Message Access Protokoll
- POP3 (110)
	- Post Office Protocol: 
		- Ruft E-Mails von einem Server ab und kann diese bei Bedarf löschen.
- BOOTP (V4-Client=68, V4-Server=67)
	- Bootstrap Protocol
		- dient dazu, einem Computer in einem TCP/IP-Netzwerk eine IP-Adresse und eine Reihe von weiteren Parametern zuzuweisen, Ports werden auch von DHCP benutzt.
- DHCP (V6-Client=546, V6-Server=547)
	- Dynamic Host Configuration Protocol
		- Zuweisung der Netzwerkkonfiguration an Clients durch einen Server.
- DNS (53)
	- Domain Name System: 
		- Löst Domains in IP-Adressen auf.
- NFS (111, 2049)
	- Network File System: 
		- Ermöglicht den Zugriff auf entfernte Daten über ein Netzwerk.
- NTP (123)
	- Network Time Protocol: 
		- Der Standard zur Synchronisierung mehrerer Netzwerkuhren, 
			- ermöglicht auch die Erstellung eines Zeitstempels.
- NNTP (119)
	- Network News Transfer Protocol: 
	- Ein Übertragungsprotokoll zur Verwaltung von Nachrichten und Newsgroups.
- SSH (22 auch für scp,sftp)
	- Secure Shell: 
		- Ermöglicht die sichere Verbindung 
			- zwischen zwei Rechnern in einem Netzwerk.
- Telnet (23)
	- Telecommunication Network: 
		- Ermöglicht den Zugriff 
			- eines virtuellen Terminals 
			- auf einen entfernten Rechner.
- SNMP (161)
	- Simple Network Management Protocol: 
		- Für 
			- die Verwaltung und 
			- Überwachung von 
		- Netzwerken sowie 
			- die Kommunikation mit diesen von 
			- einer zentralen Station aus.