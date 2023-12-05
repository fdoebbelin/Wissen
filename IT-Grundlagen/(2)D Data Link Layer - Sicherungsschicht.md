---
source: https://www.ionos.de/digitalguide/server/knowhow/sicherungsschicht/
---
- Die Sicherungsschicht ist für 
	- die fehlerfreie Übertragung von Bits 
		- in Datenpaketen zuständig. 
- Sie kümmert sich dabei nicht nur um 
	- die Portionierung und 
	- die Überwachung während des Transfers, sondern 
		- trägt auch aktiv zur Fehlerbehebung bei.

- Sie fungiert als Protokollschicht und 
	- sorgt für eine fehlerfreie Übertragung von Frames 
	- innerhalb einer physikalischen Verbindung. 
- Damit übernimmt diese Schicht 
	- eine wichtige Funktion innerhalb des OSI-Modells. 

## Funktionen

- Die Sicherungsschicht 
	- kodiert, 
	- dekodiert und 
	- organisiert die einzelnen Bits und 
	- bereitet sie als Data Frames auf. 
- Sie erstellt so also Datenpakete oder 
	- löst große Datenpakete in kleinere Einheiten auf.
- Der Data Link Layer sorgt dafür, dass 
	- die Frames fehlerfrei übertragen und so 
		- ungesicherte Systemverbindungen zu 
		- gesicherten Systemverbindungen werden können.

- Die Kommunikation, 
	- die auf der Sicherungsschicht stattfindet, kann 
		- verbindungslos oder 
		- verbindungsorientiert durchgeführt werden. 
- Im ersten Fall werden dazu sämtliche Daten, 
	- die übertragen werden sollen, 
	- mit Quell- und Zieladressen ausgestattet. 
- Im zweiten Fall werden 
	- zunächst logische Verbindungen 
		- zwischen Sender und Empfänger etabliert.

## Fehlererkennung und -behebung

- Neben dem Auf- und Abbau 
	- der unterschiedlichen Vermittlungsabschnitte und 
	- der Strukturierung der einzelnen Bits in Frames 
	- gehören auch 
		- die Kontrolle während und nach der Übertragung sowie 
		- die **Fehlererkennung und -behebung** 
	- zu den Aufgaben der Sicherungsschicht. 
- Dafür analysiert sie zunächst 
	- einzelne Bitmuster innerhalb der Frames und 
	- kann so frühzeitig Probleme und Fehler erkennen.

- Tritt eine Unregelmäßigkeit auf, 
	- informiert die Sicherungsschicht die übergeordneten Ebenen. 
- Der Empfänger kann dann Frames, 
	- die nicht in der richtigen Reihenfolge geliefert werden, 
		- neu sortieren, 
- während die Sicherungsschicht kontrolliert, 
		- ob die einzelnen Pakete unversehrt geblieben sind.

- Dafür überprüft die OSI-Sicherungsschicht den Datenfluss und 
	- kann erkennen und eingreifen, 
	- wenn eine **physische Verbindung überlastet** ist. 
- Kommt es zu Einschränkungen, 
	- so werden diese Informationen über 
		- die umliegenden Geräte verbreitet und 
	- es wird – falls möglich – eine Umleitung initiiert.

### Dienste

- Die Sicherungsschicht wird unterteilt in zwei Unterschichten: 
	- Die logische Medienzugriffskontrolle MAC ([Medium Access Control](https://www.ionos.de/digitalguide/server/knowhow/mac-adresse/ "Mac-Adresse"))  
		- grenzt an die Bitübertragungsschicht (Layer 1) an 
	- und 
		- die Verbindungssteuerung LLC (Logical Link Control) 
			- dockt an die Netzwerkschicht (Layer 3) an. 
- Die Dienste, die die Sicherungsschicht anbietet, 
	- lassen sich in drei Kategorien unterteilen:

### Verbindungslose Dienste ohne Bestätigung

- Werden auf diese Weise Frames an einen Empfänger versendet, 
	- bestätigt dieser nicht den ordnungsgemäßen Erhalt. 
- Werden Datenpakete also beschädigt oder gehen sie verloren, 
	- erfolgt **keine Wiederherstellung**. 
- Diese Art der Übertragung eignet sich daher 
	- nur bei besonders sicheren Verbindungen oder wenn 
	- eine höhere Ebene die Fehlerkorrektur übernimmt. 
- Auch wenn ein 
	- umgehender Datentransfer nötig und 
	- wichtiger als eine vollständige Übertragung ist, 
	- kann diese Methode in Frage kommen.

### Verbindungslose Dienste mit Bestätigung

- In den meisten Fällen ist diese Methode allerdings besser, 
	- da der **Erfolg jeder Übertragung bestätigt** wird. 
- Erreicht eine Übertragung 
	- nicht ihr Ziel oder 
	- gehen einzelne Bestandteile unterwegs verloren, 
	- bleibt die Bestätigung aus und 
	- der Datentransfer kann erneut versucht werden. 
- Das sorgt dafür, 
	- dass alle Frames beim Empfänger ankommen.

### Verbindungsorientierte Dienste

- Die sicherste Methode ist 
	- der verbindungsorientierte Dienst der Sicherungsschicht. 
- Dabei erhält jedes Datenpaket eine spezifische Nummer, 
	- die beim Sender und 
	- beim Empfänger hinterlegt wird. 
- Diese bauen vor jedem Austausch eine Verbindung auf. 
- Beide Seiten haben dadurch die Garantie, 
	- dass jedes Paket genau einmal und 
	- mit Sicherheit fehlerfrei übertragen wird und 
	- sein Ziel erreicht.

## Komponenten

- Bridge
- Wireless Access Point
- Layer-2-Switch
- Modem

## Protokolle

- Zahlreiche Protokolle können der OSI-Sicherungsschicht zugeordnet werden. 
- Dazu gehören unter anderem:
	-   1-Wire
	-   ARCnet
	-   [ARP](https://www.ionos.de/digitalguide/server/knowhow/was-ist-arp-adressaufloesung-im-netzwerk/)
	-   ATM
	-   [Ethernet](https://www.ionos.de/digitalguide/server/knowhow/ethernet-ieee-8023/)
	-   HDLC
	-   LLC/MAC
	-   MIL-STD-1553
	-   PPP
		- Point-to-Point Protocol = Netzwerkprotokoll zum Verbindungsaufbau über Wählleitungen)
	-   SpaceWire
	-   [Token Ring](https://www.ionos.de/digitalguide/server/knowhow/token-ring/)
	-   UNI/O
	-   V.120
	-   X.75