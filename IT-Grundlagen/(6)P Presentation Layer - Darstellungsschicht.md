- Die Darstellungsschicht ist 
	- für die Übersetzung 
	- unterschiedlicher Dateiformate zuständig. 
- Dies ermöglicht eine Kommunikation zwischen zwei Systemen. 
- Zu den weiteren Aufgaben des Presentation Layers gehören 
	- die Kompression sowie die Verschlüsselung von Daten.

## Funktionen

- Die Darstellungsschicht 
	- interagiert besonders eng mit 
		- der ihr folgenden Anwendungsschicht. 
- Ihre Hauptaufgabe besteht darin, 
	- Daten so darzustellen, 
	- dass sie von beiden Seiten, also 
		- dem sendenden System und dem 
		- empfangenden System, 
	- **verstanden und interpretiert werden** können. 
- Dafür wird auf der Anwendungsschicht zunächst festgelegt, 
	- wie Daten strukturiert werden sollen und 
	- welche Typen und Werte zulässig sind.

- Aus diesen Angaben wird automatisch 
	- ein Befehlssatz beziehungsweise 
	- eine **abstrakte Transfersyntax** erstellt. 
- Der Darstellungsschicht 
	- kommt nun die Aufgabe zu, 
	- die Daten so zu übertragen, 
		- dass sie zwar lesbar sind, 
		- ihre enthaltenen Informationen 
			- aber auch nicht verändert werden.

- Eine zweite wichtige Aufgabe, 
	- die in den meisten Fällen auf 
		- der Ebene der Darstellungsschicht stattfindet, 
	- ist die 
		- Verschlüsselung und 
		- Entschlüsselung von Daten. 
- Hierfür werden die Informationen zunächst auf der Seite des Senders verschlüsselt und dann im verschlüsselten Zustand an den Empfänger gesendet. 
- Über die Darstellungsschicht werden dazu 
	- Schlüssel und 
	- Verschlüsselungsverfahren ausgetauscht. 
- Dadurch erhält die Seite 
	- des Empfängers die Möglichkeit, 
	- die unlesbaren Daten 
		- zu entschlüsseln und 
		- in ein Format zu bringen, 
	- das verständlich und auswertbar ist.

- Die dritte Funktion der OSI-Darstellungsschicht ist 
	- die sogenannte Serialisierung von Objekten, 
	- welche über den Presentation Layer verwaltet wird. 
- Dafür werden komplexe Anwendungsdatenobjekte so übersetzt, dass sie leichter zu transportieren sind und auf der Empfängerseite besser gespeichert werden können. 
- Dies erleichtert den Datentransfer auch bei anspruchsvollen Dateien und ermöglicht der empfangenden Seite den schnellen und fehlerlosen Wiederaufbau des Objektes. 
- Dieses wird zurück in ein Format gewandelt, 
	- welches von der Anwendung ausgeführt werden kann. 
- Das führt außerdem dazu, 
	- dass in der eigentlichen Anwendung keine Funktionen implementiert werden müssen, die zur Kompression benötigt werden.

## Formate

- Werden Daten während eines Transfers angezeigt, 
	- spricht man von einer Transfersyntax. 
- Diese wird unterteilt in die oben bereits erwähnte 
	- **abstrakte Transfersyntax**, 
		- in der die übertragenen Werte beschrieben werden, und 
	- die **konkrete Syntax**, 
		- die eine Beschreibung der Kodierung der Werte enthält.

- Nur wenn der Empfänger 
	- sämtliche Informationen über die Darstellungsschicht erhält, 
	- kann er die erhaltenen Daten verarbeiten und verstehen. 
- Die gängigste Beschreibungssprache ist 
	- die **Abstract Syntax Notation One** (ASN.1), 
	- welche auch von der ISO-Organisation vorgeschlagen wird. 

- Die Darstellungsschicht kennt viele verschiedene Formate, 
	- die je nach Empfänger am besten für die Aufbereitung geeignet sind. 
- Am häufigsten werden jedoch die Formate [ASCII](https://www.ionos.de/digitalguide/server/knowhow/ascii-american-standard-code-for-information-interchange/ "ASCII-American-Standard-Code-for-Information-Interchange") (American Standard Code for Information Interchance) und EBCDIC (Extended Binary-Coded Decimal Interchance Code) für Texte verwendet. 
- Die gängigsten 
	- Bildformate sind 
		- GIF, 
		- JPEG,
		- PNG und 
		- TIFF 
	- und die Formate für Videos 
		- MIDI, 
		- MPEG und 
		- QuickTime.

## Protokolle

- Viele verschiedene Protokolle, Übertragungs- und Vermittlungstechniken greifen auf die Darstellungsschicht zurück. 
- Dazu gehören unter anderem:
	- TLS
		- Transport Layer Security
	- SSL
		- Secure Socket Tunneling
	- AFP
		- Apple Filing Protocol
	- ICA
		- Independent Computing Architecture, the Citrix system core protocol
	- LPP
		- Lightweight Presentation Protocol
	- NCP
		- NetWare Core Protocol
	- NDR
		- Network Data Representation
	- Tox
		- The Tox protocol is sometimes regarded as part of both the presentation and application layer
	- XDR
		- eXternal Data Representation
	- X.25
		- Packet Assembler/Disassembler Protocol (PAD)

## Verzicht auf den Presentation Layer

- Die Aufgaben, die die Darstellungsschicht erledigt, 
	- werden nicht bei jeder Kommunikation 
	- zwischen zwei Systemen benötigt. 
- Nutzen beide Seiten 
	- dieselben Formate, 
	- so fällt die Übersetzung weg. 
- Auch die Verschlüsselung oder die Kompression 
	- sind längst nicht bei jeder Interaktion gefragt oder 
	- können bei Bedarf auch auf 
		- anderen Schichten des OSI-Modells durchgeführt werden. 
- In diesen Fällen kann es vorkommen, 
	- dass die Darstellungsschicht nicht zum Einsatz kommt und 
	- somit die Anwendungsschicht (Layer 7) 
	- stattdessen direkt mit der Sitzungsschicht (Layer 5) kommuniziert.