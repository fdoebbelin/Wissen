- Um die Kompatibilität und Kommunikation von Netzen untereinander zu gewährleisten, 
	- hat die ISO das OSI-7-Schichtenmodell der Kommunikation in offenen Systemen entwickelt.

*OSI-7-Schichtenmodell und Protokolle (Beispiele)*
![](_resources/Pasted%20image%2020221213104905.png)

- Auf der Grundlage des 7-Schichten-Netzmodells können die verschiedenen Netze miteinander kommunizieren. 

![](_resources/Pasted%20image%2020221213105147.png)

- Jede Schicht (Layer) im OSI-7-Schichtenmodell 
	- nutzt Dienste der darunterliegenden Schichten und 
	- stellt den höheren Schichten Dienste zur Verfügung.

>**ISO** International Standardization Organization
>**OSI** Open Systems Interconnection
>OSI-Schichtenmodell beschrieben in ISO/IEC 7498-1
>IEC International Electrotechnical Commission

>Merksatz für die 7 Schichten:
>Von oben nach unten gelesen:
><u>a</u>ll <u>p</u>eople <u>s</u>eem <u>t</u>o <u>n</u>eed <u>d</u>ata <u>p</u>rocessing
>Alle deutschen Studenten trinken verschiedene Sorten Bier
>Oder von unten nach oben gelesen:
><u>p</u>lease <u>d</u>o <u>n</u>ot <u>t</u>hrow <u>s</u>alami <u>p</u>izza <u>a</u>way.


### Kapselung von Daten mit OSI-7-Schichtenmodell
- Bei der Datenkapselung (Encapsulation) werden 
	- die Daten mit den Protokollinformationen gepackt.

![](_resources/Pasted%20image%2020221213111914.png)

- Jede OSI-Schicht fügt hierbei Protokollinformationen 
	- an den Anfang (Header) und Protokollinformationen 
	- an das Ende (Trailer) eines Datenpaketes an und 
	- reicht anschließend die gesamten Informationen 
		- eine Schicht weiter nach unten. 
- Damit Datenpakete von der Quelle zum Ziel übertragen werden, 
	- muss jede Schicht des Senders 
	- mit der gleichrangigen Schicht des Zieles kommunizieren. 
- Jede Schicht tauscht hierbei 
	- Protokollinformationen (PDU = Protocol-Data-Unit) 
	- mit der gleichrangigen Schicht aus. 
- Im TCP/IP-Modell werden 
	- die OSI-Schichten zum Teil zusammengefasst.

![](_resources/Pasted%20image%2020221213112034.png)

### Schritte bei der Datenkapselung (Senden)

#### Schritt 1: Daten erzeugen
- Ein Benutzer, der z. B. eine E-Mail schreibt und versendet, 
	- verwendet alphanumerische Zeichen. 
- Diese werden in Daten, 
	- die auf dem Netzwerk transportiert werden können, 
	- gewandelt. 
- Die beteiligten Schichten sind meist 
	- die Sitzungsschicht, 
	- die Darstellungsschicht und 
	- die Anwendungsschicht.

#### Schritt 2: Daten für den Transport packen
- Die Daten werden für den Ende-zu-Ende-Transport 
	- in Segmente verpackt. 
- Durch die Segmentierung garantiert die Transportschicht, 
	- dass Sender und Empfänger 
		- zuverlässig miteinander kommunizieren können

#### Schritt 3: Netzwerkadressen hinzufügen
- Die Segmente werden in ein Paket, 
	- das die Netzwerkadressen 
		- der Quelle und 
		- des Senders enthält, 
	- eingepackt. 
- Die Pakete werden auch Datagramme genannt. 
- Durch die Netzwerkadressen 
	- können die Netzwerkkomponenten 
	- einen Pfad zum Versenden bestimmen.

#### Schritt 4: MAC-Adressen hinzufügen
- Jede Netzwerkkomponente 
	- packt die Pakete in einen Rahmen (Frame), 
	- welcher 
		- die Ziel-MAC-Adresse und 
		- die Sender-MAC-Adresse 
	- enthält. 
- Der Rahmen ermöglicht eine Verbindung 
	- zum nächsten direkt angeschlossenen Netzwerk.

#### Schritt 5: Konvertierung in Bits
- Die im Rahmen enthaltenen Daten werden in Bits konvertiert. 
- Die einzelnen Bits werden über das Medium versandt.

### Schritt 1 bis 5 bei Empfang:
- Beim Empfang 
	- werden die Schritte 
		- in umgekehrter Reihenfolge 
	- durchlaufen, 
	- die Daten werden hierbei 
		- schrittweise entkapselt (Decapsulation).
