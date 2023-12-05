- Die Sitzungsschicht wird auch als 
	- Kommunikationssteuerungsschicht oder 
	- Session Layer bezeichnet.

## Kommunikationssteuerung

- Die Hauptaufgabe der Sitzungsschicht besteht darin, 
	- eine **logische Verbindung zwischen zwei Systemen aufzubauen**. 
- Diese Verbindung wird als Sitzung bezeichnet. 
- Sie ist jeweils einzigartig und eindeutig. 
- Auch die Kontrolle 
	- dieser Sitzungen oder 
	- Sessions obliegt der Sitzungsschicht. 
- So kann die Ebene zum Beispiel 
	- den temporären Zugriff auf ein anderes System erlauben und 
	- dabei die Kommunikation steuern.

- Diese findet 
	- beidseitig, 
	- parallel oder 
	- richtungsabhängig statt. 
- Man spricht von einer **Dialogkontrolle** (Dialog Control), 
	- die von der OSI-Sitzungsschicht übernommen wird. 
- Für eine einseitige Kommunikation 
	- kann der Session Layer Token vergeben, 
	- um die Reihenfolge zu regeln und 
	- so einen ungestörten Dialog zu ermöglichen.

Diese Tokens werden für die OSI-Sitzungsschicht in vier Kategorien unterteilt:

- **Datenmarken** (Data Token): 
	- Diese geben während 
		- einer einseitigen Kommunikation 
			- im Halb-Duplex-Betrieb an, 
		- welche Seite wann senden darf.
- **Aktivitätsmarken** (Activity Major Token): 
	- Aktivitätsmarken unterteilen eine Verbindung 
		- in unterschiedliche Aktivitäten. 
	- Wird eine Aktivität unterbrochen oder abgebrochen, 
		- kann sie später 
			- in dieser oder 
			- einer anderen Sitzung 
		- wiederaufgenommen werden.
- **Synchronisationsmarken** (Synchronize Minor Token): 
	- Diese Tokens sind von 0 bis 999.999 durchnummeriert und 
	- werden verwendet, um eine Kommunikation zu unterteilen. 
- **Beendigungsmarken** (Release Token): 
	- Diese markieren das Ende einer Session.

## Synchronisation auf der Sitzungsschicht

- Neben der Organisation und Steuerung der Kommunikation ist 
	- die Synchronisation des Datenaustauschs 
	- ein zweiter sehr wichtiger Dienst, 
	- der von der Sitzungsschicht bereitgestellt wird. 
- Dieser rückt vor allem dann in den Fokus, 
	- wenn eine Datenübertragung 
		- auf der vierten oder einer darunterliegenden Ebene 
		- **unerwartet und ungewollt abgebrochen** wird.

- Die OSI-Sitzungsschicht erstellt 
	- speziell für solche Fälle Synchronisationspunkte. 
- Wird dann die Kommunikation unterbrochen, 
	- kann die Übertragung 
		- an einem solchen Punkt 
		- wieder aufgenommen werden und 
	- muss nicht komplett von vorne beginnen. 
- Insbesondere bei der Kommunikation über 
	- langsame oder instabile Verbindungen oder 
	- bei besonders umfangreichen Dateien 
	- ist dieser Dienst eine große Hilfe.

- Die Synchronisationspunkte, 
	- die von der Sitzungsschicht zur Verfügung gestellt werden, 
	- unterteilt man in zwei große Kategorien.
		- **Major-Synchronisationspunkte** 
			- unterteilen Daten, 
				- die ausgetauscht werden sollen, 
				- in einzelne Einheiten. 
			- Diese Synchronisationspunkte müssen 
				- ausdrücklich bestätigt werden.
		- **Minor-Synchronisationspunkte** 
			- sorgen innerhalb der Einheiten für eine 
				- logische und 
				- praktische Struktur. 
			- Ihre Bestätigung ist optional.

## Dienste

- Die Internationale Organisation für Standarisierung (ISO), 
	- schlägt folgende Klassifizierung für die Funktionseinheiten vor. 
- Die passende Kombination wird im 
	- Vorfeld der Sitzung von beiden Parteien festgelegt.
		- **Basic Combined Subset** (BCS): 
			- kompatibel mit Kernel, Halb-Duplex und Duplex
		- **Basic Synchronized Subset** (BSS): 
			- kompatibel mit Kernel, Halb-Duplex, Negotiated Release, Minor- und Major-Synchronisationspunkte sowie Resynchronisation
		- **Basic Activity Subset** (BAS): 
			- kompatibel mit Kernel, Halb-Duplex, Minor-Synchronisationspunkte, Ausnahmen, Aktivitätsmanagement

## Protokolle

- Es gibt zahlreiche Protokolle, 
	- die die OSI-Sitzungsschicht nutzen. 
- Dafür stellt die Sitzungsschicht 
	- ihre Protokolle und Dienste den höher liegenden Ebenen 
	- über Programmierschnittstellen zur Verfügung. 
- Die Parameter und Eigenschaften 
	- der darunter liegenden Schichten sind dabei 
	- für die belastbaren Kommunikationsverbindungen 
		- nicht relevant. 
- Zu den Protokollen, 
	- die die Sitzungsschicht nutzen, 
	- gehören unter anderem folgende:
		- ADSP
			- AppleTalk Data Stream Protocol
		- ASP
			- AppleTalk Session Protocol
		- H.245
			- Call Control Protocol for Multimedia Communications
		- iSNS
			- Internet Storage Name Service
		- NetBIOS
			- File Sharing and Name Resolution protocol - the basis of file sharing with Windows.
		- NetBEUI
			- NetBIOS Enhanced User Interface
		- NCP
			- NetWare Core Protocol
		- PAP
			- Printer Access Protocol
		- RPC
			- Remote Procedure Call
		- RTCP
			- RTP Control Protocol
		- SDP
			- Sockets Direct Protocol
		- SMB
			-  Server Message Block
		- SMPP
			- Short Message Peer-to-Peer
		- SOCKS
			-  "SOCKetS"
		- ZIP
			-  Zone Information Protocol (For AppleTalk)