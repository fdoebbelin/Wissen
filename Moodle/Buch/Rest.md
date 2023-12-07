
12 Ergänzende Lernhilfen für Moodle

Die vom Moodle-System von Haus aus gelieferten oder als Plugin nachträglich installier-baren Kurselemente sind meist funktional ausreichend, jedoch in ihren didaktischen Eigenschaften oft begrenzt. Moodle sieht deswegen offene Schnittstellen für externe Lernpakete vor, wie zum Beispiel _SCORM_ (Sharable Content Object Reference Model) oder den _IMS/_

_LTI-Standard_. Zu den bekanntesten Tools gehört _Hot Potatoes_, ein Tool zur unterhaltsamen Gestaltung von Übungsspielen und Hilfen der individuellen Lernzielkontrolle. Die an sich gute Idee externer Lernpakete ist allerdings auch mit berechtigter Kritik behaftet, denn beim SCORM-Standard sind Funktionen des Datenaustausches zwischen den externen Paketen und Moodle nicht mehr zeitgemäß, sodass erbrachte Leistungen nicht im Detail direkt berücksichtigt werden können.

Mit _H5P_ gibt es seit einiger Zeit eine immer beliebtere Möglichkeit, interaktive Lehrinhalte zu gestalten. Der Vorteil dieses Frameworks ist die einfache Integration direkt in Moodle und die ausschließliche Nutzung von Internet-Standard-Technologien (HTML5, CSS3 und JavaScript). Bei den Nutzerinnen und Nutzern wird also auf deren Computer für die Darstellung multimedialer Inhalte keine zusätzliche Software – z. B. FlashPlayer – benötigt.

Allerdings bietet auch die Moodle-Community selbst sehr einfache und dennoch gute Plugins an. Sie eignen sich hervorragend zur Wiederholung des Gelernten, unabhängig davon, ob der Stoff in der Lernplattform oder im Präsenzunterricht vermittelt wurde. Auch wird der

„Spieltrieb“ der Lernenden angesprochen und das Belohnungssystem herausgefordert. Es besteht also eine gewisse Motivation, sich mit den Herausforderungen der Übungen auseinander zu setzen.

**■**

**■ 12.1■Installation eines Lernspiel-Plugins**

Lernspiele sind meist nicht grundsätzlich im Moodle-System installiert. Die Moodle-Administration muss also entsprechende Plugins nachträglich installieren oder aktivieren. Bei der Installation eines Plugins muss unbedingt darauf geachtet werden, dass dieses tatsächlich auch zur aktuell verwendeten Moodle-Version kompatibel ist. Das Moodle Plugin Directory ist eine umfassende Sammlung von Moodle-Erweiterungen und bietet auch die erforderlichen Informationen.

![Image 494](index-487_1.png)

**464** 12 Ergänzende Lernhilfen für Moodle

Die Installation eines Plugins ist aus guten Gründen ausschließlich der Moodle-Administration vorbehalten. Teacher und Kursgestalter müssen also direkt mit der Systemverwaltung in Kontakt treten, wenn sie ein bestimmtes Lernspiel nutzen möchten. Dies gilt für alle in diesem Kapitel vorgestellten Tools.

Nach der Wahl des gewünschten Plugins im Moodle Plugin Directory wird dieses als ZIP-Datei heruntergeladen. Die ZIP-Datei kann direkt per _Drag and Drop_ 1 mit der Maus in das Feld des _Plugin Installers_ verschoben werden. Dort wird der Installationsprozess gestartet.

**Bild 12.1** Das Moodle Plugin Directory bietet unterschiedliche Erweiterungen für die meisten im Einsatz befindlichen Moodle-Versionen. Vor dem Download und der Installation ist jedoch grundsätzlich zu prüfen, ob das Plugin für die aktuelle Moodle-Version auch geeignet ist.

1 Drag and Drop steht für „greifen und fallen lassen“. Ein Objekt wird mit der Maus gegriffen und mit gedrückter linker Maustaste über das Ziel geschoben. Mit dem Loslassen der Maustaste wird das Objekt im Ziel abgelegt.

![Image 495](index-488_1.jpg)

12.1 Installation eines Lernspiel-Plugins

**465**

**Bild 12.2** Das Plugin kommt in einem ZIP-Archiv daher. Zur Installation in Moodle wird es – von der Moodle-Administration! – in das Datei-Upload-Formular des Plugin-Installers geschoben.

Moodle überprüft das angebotene Programmpaket. Das Ergebnis sollte unbedingt berücksichtigt werden. Unter Umständen wird eine _Warnung_ ausgegeben wie es beispielsweise Bild 12.3 zeigt. Trotzdem wird mit der Schaltfläche _Weiter_ die Fortsetzung der Installation angeboten. Es obliegt nun der Kenntnis (und der Verantwortung) der Moodle-Administration über die weitere Vorgehensweise zu entscheiden. Im gezeigten Beispiel von Bild 12.3

wurde tatsächlich versucht, eine Version des Plugins für eine veraltete Moodle-Version zu installieren. Die Meldung war hier durchaus eindeutig:

[Warnung] Entwicklungsstand [MATURITY_RC]

_Maturity_ kann mit Reife und Alter, aber auch mit dem Verfallsdatum übersetzt werden. In diesem Fall wurde zunächst die Installation fortgesetzt, worauf es zu gravierenden Problemen für den Benutzeraccount des Moodle-Administrators kam. Dies konnte nur mithilfe der täglichen Sicherheitskopien behoben werden.

Neben der Anfertigung regelmäßiger Sicherheitskopien des Systems und der Moodle-Datenbank sollten neue Plugins grundsätzlich zunächst in einem Experimentalsystem getestet werden.

![Image 496](index-489_1.png)

**466** 12 Ergänzende Lernhilfen für Moodle

**Eine „Goldene Regel“: Backup anlegen!**

Auch Autoren machen gelegentlich Fehler. So wurde auf dem hier verwendeten Testsystem versehentlich das Plugin „Flash Card Set“ für die Moodle-Version 2.8 installiert. Tatsächlich kommt für die Illustration jedoch die derzeit aktuelle Version Moodle _**3**_.8 zum Einsatz. Die Warnung nach dem „Entwicklungsstand“

wurde im Eifer des Gefechts mit _Weiter_ übergangen. Das hatte Konsequenzen, denn plötzlich war kein Login mehr mit dem Account der Moodle-Administration möglich.

Da glücklicherweise sowohl die Moodle-Datenbank als auch das gesamte

Moodle- und das Moodledata-Verzeichnis regelmäßig extern gesichert werden, war das System schnell wiederhergestellt. Ansonsten wäre durch den Ausfall der Moodle-Administration der reguläre Systembetrieb dauerhaft nicht mehr zu gewährleisten gewesen.

Stellen Sie bitte vor der Installation von Moodle-Erweiterungen sicher, dass sowohl die Moodle-Datenbank als auch die Moodle- und Moodledata-Verzeichnisse auf dem Webserver gesichert werden. Näheres dazu ist im Technik-Teil dieses Buchs zu lesen.

■

**Bild 12.3** Die Warnung ist ernst zu nehmen! Die Installation veralteter Versionen eines Plugins kann zu gravierenden Systemschäden führen.

![Image 497](index-490_1.jpg)

![Image 498](index-490_2.jpg)

12.2 Flash Cards

**467**

**Bild 12.4** Sind tatsächlich alle Voraussetzungen erfüllt? Mit der Aktualisierung der Datenbank wird die Installation des Plugins vollendet.

**Bild 12.5** Das Plugin kann nun genutzt werden. In diesem Fall handelt es sich um eine Aktivität, die in einem Kurs eingesetzt wird. Dort kann sie nun als Lernaktivität in die gewünschten Kursabschnitte eingebaut werden.

**■**

**■ 12.2■Flash Cards**

Flash Cards oder Lernkarten gehören zu den klassischen Lernhilfen, die vor allem in Sprachkursen erfolgreich zum Einsatz kommen. Ursprünglich wurde diese Methode auch im _Präsenzunterricht_ oder als Hausaufgabe eingesetzt. Bevor es elektronische Lernsysteme gab, nutzte man Karteikarten auf Papier.

![Image 499](index-491_1.png)

![Image 500](index-491_2.png)

**468** 12 Ergänzende Lernhilfen für Moodle

**Zum Spielablauf**

Die Lernenden nehmen die oberste Karte des vorderen Stapels und lesen die Frage. Beispielsweise wird die passende Vokabel für einen bestimmten Begriff gesucht. Bevor die Lernenden einen Blick auf die Rückseite der Karte werfen, auf welcher sie die richtige Lösung finden, versuchen sie selbst durch Überlegung auf die Lösung zu kommen. Ist die Lösung richtig, wird die Karte an das Ende des folgenden Stapels gesetzt. Ist die Lösung falsch, kommt die Karte zurück in den gleichen Stapel oder, wenn man bereits im folgenden Stapel arbeitet, wird sie wieder um einen Stack vorgelagert.

So lassen sich beispielsweise sehr effektiv und ohne Überlastung der Lernenden Vokabeln üben. Die Lernstrategie basiert dabei auf kleinen und zeitlich sehr kurzen Einheiten. Lernkarten eignen sich deswegen für die vielen kleinen Pausen des Tages wie zum Beispiel das Warten auf Bahn oder Bus.

Die elektronische Version der Lernkarten in Moodle bietet zudem verschiedene Automatis-men:

Karten können automatisch nach einer gewissen Zeit wieder in einem vorderen Stapel verschoben werden, was interessant ist, wenn mehrere Stapel in diesem Spiel vorgesehen werden. Lässt sich eine lernende Person zu viel Zeit mit der Bearbeitung, füllt sich somit automatisch der Einsteigerstapel. Fleiß wird hingegen damit belohnt, eine gute Chance zu haben, wirklich alle Karten in den letzten Stapel zu verschieben. In diesem Stapel befinden sich die Karten, deren Fragen offensichtlich sicher beantwortet werden können.

**Bild 12.6** 

Nur wenn das Flash-Card-Plugin installiert und aktiviert ist,

kann die Aktivität in den Kurs eingebunden werden.

**Bild 12.7** Das Lernkartenspiel kann durchaus zeitlich befristet werden. Schaffen alle Lernenden es, die Stapel durchzuarbeiten?

![Image 501](index-492_1.png)

![Image 502](index-492_2.jpg)

12.2 Flash Cards

**469**

**Bild 12.8** Anders als klassische Karteikarten können die Moodle-Flash-Cards durchaus auch multimediale Inhalte haben.

**Bild 12.9** 

Prinzip des Leitner-Spiels: Richtig beantwortete Karten rücken

einen Stapel weiter in Richtung Ziel. Falsch beantwortete Karten

rücken wieder um einen Stapel zurück zum Startpunkt.

(Quelle: Wikipedia/Zirguezi, Nutzung nach CC0, Public Domain)

**12.2.1■Konfiguration der Aktivität**

Mit der Konfiguration der Aktivität _Flash Card Set_ werden die Spielregeln von der Teacher-Rolle festgelegt. Das Gameplay – hier wird zwischen dem Leitner- und dem freien Training unterschieden – legt das Erscheinungsbild der Karten und das Spielschema fest.

Beim Leitner-Spiel – es bietet sich bei größeren Kartenstapeln an – werden mehrere Kartenstapel definiert. Zu Beginn liegen alle Karten auf dem ersten Stapel. Eine richtige Lösung lässt die Karten in den nächsten Stapel wandern. Optisch werden die verschiedenen Kartenstapel mit farbigen Kartenrücken dargestellt.

**470** 12 Ergänzende Lernhilfen für Moodle

Das freie Training sieht nur einen Kartenstapel vor. Ist eine Aufgabe korrekt gelöst, kann die Karte aus dem Stapel entfernt werden. Dies bedeutet selbstverständlich, dass die Karte lediglich aus dem Stack dieser einen lernenden Person entfernt wird. Die Stapel aller anderen Lernenden bleiben davon unberührt. Das freie Training endet, wenn der Kartenstapel erfolgreich durchgearbeitet wurde.

In beiden Spielvarianten ist es möglich, sowohl Fragen als auch Antworten – genau genommen „Vorder- und Rückseite“ der Lernkarten – mit reinem Text zu formulieren. Es können aber auch Bilder oder Audio-Dateien (zudem kombiniert) eingesetzt werden. Zunächst in der hier gezeigten Version als „experimentell“ eingestuft, sind auch kleine Video-Sequenzen denkbar.

Eine Quasi-Verdoppelung der Fragen lässt sich erreichen, wenn Vorder- und Rückseite vertauscht werden können. In der Tat verlieren die Fragestellungen die Routine, wenn sie ge -

legentlich aus einer anderen Perspektive gestellt werden.

**Video-Flash-Cards**

Video-Clips sind heute von den meisten modernen Webbrowsern ohne Zusatz-

software darstellbar. Zu prüfen ist, ob diese Sequenzen auch auf Smartphones der Lernenden problemlos konsumierbar sind. Hier sollte nicht zuletzt berücksichtigt werden, dass viele Mobilfunk-Verträge noch mit Volumentarifen für die Datenübertragung gestaltet werden. Videos transportieren in der Regel recht große Datenmengen!

■

Interessant sind die zeitlichen Einflüsse auf die Leitner-Kartenstapel. Hier wird ein gewisser Druck auf die Spieler, also auf die Lernenden aufgebaut. Zusätzlich zur zeitlichen Gesamtbegrenzung der Spielzeit lassen sich Fristen für die Bearbeitung der Kartenstapel festlegen. Verstreichen diese Fristen, werden die Karten wieder zurückgelegt.

Die Gestalt der Karten lässt sich individuell beeinflussen, wenn Grafiken zum Beispiel für den Vorder- und Hintergrund der Karten hochgeladen werden. Akzeptiert werden die gängigen Dateiformate für im Internet darstellbare Bilder wie JPG/JPEG, GIF und PNG.

Wer Erfahrungen mit CSS hat, kann die Gestalt der Karten zusätzlich beeinflussen. Das folgende Listing zeigt in den fett hervor gehobenen Zeilen eine Ergänzung des CSS-Codes aus Bild 12.11. Die Umrahmungen und die Schriften der Fragekarten werden damit rot, die der Antwortkarte grün dargestellt. Wer die Formate von CSS voll ausreizt, kann hier sehr ansprechende Designs entwickeln

/* panel div for question */

.flashcard-question{

**color: red;**

}

/* panel div for answer */

.flashcard-answer{

**color: green;**

}

![Image 503](index-494_1.png)

12.2 Flash Cards

**471**

**Bild 12.10** Mithilfe hochladbarer Bilddateien können die Lernkarten ein individuelles Design zugewiesen bekommen – zum Beispiel ein Logo der Schule oder des Bildungsinstituts.

![Image 504](index-495_1.png)

**472** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.11** Mithilfe von CSS können die Karten direkt in ihrem Layout bearbeitet werden.

**12.2.2■Erstellung von Fragen und Antworten**

Nach der Grundkonfiguration der Flash-Card-Aktivität benötigen die Karten natürlich auch Inhalte. Wie bereits angedeutet, ist die klassische Verwendung der Lernkarten das Vokabel-training. So kann auf die Vorderseite der Begriff in der eigenen Sprache und auf der Rückseite die Übersetzung in die zu lernende Fremdsprache geschrieben werden. Die einfachste Form der Lernkarten sieht also auf der Vorder- und Rückseite jeweils ein Wort vor. Allerdings lassen sich auch Fachbegriffe und komplexere Fragestellungen formulieren. Das Beispiel zeigt die Formulierung reiner Textfragen. Wie angedeutet, können die „Frage _karten_“

auch mit anderen Medien besetzt werden.

Für die Eingabe neuer Fragen können wahlweise Formulare für eine oder drei Frage-Antwort-Kombinationen aufgerufen werden. Weil jeder erneute Aufruf der Seite zur Übertragung der Fragen und für die erneute Eingabe eine gewisse Zeit erfordert, kann mit der gleichzeitigen Formulierung von drei Fragen und Antworten in einem Durchgang die Be -

arbeitungszeit deutlich verkürzt werden.

Die eingetragenen Fragen werden in einer übersichtlichen Liste dargestellt. Personen mit der Teacher-Rolle können hier gezielt Fragen bearbeiten und gegebenenfalls Fehler korrigieren oder Fragen aus der Sammlung entfernen.

![Image 505](index-496_1.jpg)

![Image 506](index-496_2.jpg)

12.2 Flash Cards

**473**

**Bild 12.12** Die Trainer-Rolle hat die Möglichkeit, die Karten zu bearbeiten. Hier können Fragen und Antworten angelegt und geändert werden.

**Bild 12.13** Sollen mehr als eine Frage erstellt werden, so ist es ratsam, gleich drei Fragen auf einmal hinzuzufügen. Das verkürzt die Bearbeitungszeit, weil die Übertragungs- und Seitenaufbauzeiten einer Webseite in der Summe sehr lang sein können.

![Image 507](index-497_1.png)

**474** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.14** Beispiel für die Eingabe nur einer Frage und der zugehörigen Antwort.

**12.2.3■Das Spiel**

Wie Lernende das Spiel nutzen, hängt von den Vorgaben der Lehrenden ab. Werden sowohl freies Training als auch das Leitner-Spiel angeboten, können die Lehrenden frei wählen. Die Karten werden mit einem Mausklick geöffnet und die Fragen nach dem Zufallsprinzip angezeigt. Wenn die Lehrenden das so vorgesehen haben, können durchaus auch die Vorder- und Rückseiten bei der Fragestellung vertauscht werden.

Beim Leitner-Spiel werden die Fragekarten mehrmals durchgearbeitet und bei richtiger Lösung auf den nächsten Stapel gelegt. Beim freien Training werden die Karten mit den richtigen Antworten aus dem Stapel entfernt.

Entscheidend ist beim Flash-Card-Spiel, dass es keine automatische Bewertung gibt. Es werden keine Antworten direkt in das System eingetragen. Die „Bewertung“ erfolgt ausschließlich durch die Lernenden selbst. Sie werden damit neben der Übung des fachlichen Stoffs zu einer Selbstreflexion motiviert und lernen, ihre eigenen Kenntnisse selbst und kritisch einzuschätzen.

**Selbstreflexion als wichtiges Lernziel**

Die Fähigkeit zur Selbsteinschätzung des eigenen Leistungs- und Wissens-

stands ist (nicht nur) für Lernende von allergrößter Bedeutung. Damit wird

![Image 508](index-498_1.jpg)

![Image 509](index-498_2.jpg)

12.2 Flash Cards

**475**

einerseits der Trend zur Selbstüberschätzung verringert. Die Lernenden

gewinnen aber auch die Fähigkeit, gezielt ihre Schwächen zu erkennen und selbstmotiviert vertiefend zu lernen.

■

**Bild 12.15** Das Lernkartenspiel nach dem Leitner-Verfahren: Hier ist das Spiel noch ganz am Anfang. Alle Fragenkarten befinden sich noch im ersten Stapel (ganz links).

**Bild 12.16** Klickt man im Leitner-Spiel auf einen Stapel, wird die Frage einer Karte geöffnet.

![Image 510](index-499_1.png)

![Image 511](index-499_2.png)

**476** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.17** Ein weiterer Klick auf die Karte zeigt die Antwort.

**Bild 12.18** Zwei richtige Antworten! Beim Leitner-Spiel werden die Karten um einen Stapel verschoben. Sie sind aber insgesamt noch im Spiel.

![Image 512](index-500_1.png)

12.2 Flash Cards

**477**

**Bild 12.19** Beim freien Training wird auf die Darstellung verschiedener Kartenstapel verzichtet.

Es wird nur entschieden, ob die Karte im Stapel verbleiben oder entfernt werden soll.

**12.2.4■Auswertung**

Lehrende sollten grundsätzlich im Blickfeld behalten, welche Fortschritte ihre Lernenden machen. Zwar können die Ergebnisse des Flash-Card-Spiels nicht als belastbare Lernzielkontrolle eingestuft werden, denn schließlich basiert die Darstellung in der Zusammenfassung der Lehrenden-Ansicht auf der eigene Einschätzung der Lernenden, jedoch kann beobachtet werden, ob die Lernkarten überhaupt von den Lernenden angenommen werden.

Einen zusätzlichen, sehr wertvollen Informationsgehalt hat die Auswertung der durchschnittlichen Bearbeitungszeit pro Lernkarte. Klicken Lernende die Karten nur durch die Stapel hindurch und suggerieren damit einen vermeintlichen Lernerfolg, so wird dies durch verblüffend kurze Bearbeitungszeiten schnell ersichtlich.

![Image 513](index-501_1.png)

**478** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.20** Lehrende können in einem begrenzten Maß beobachten, ob die Lernkarten bearbeitet werden, und aus den Daten schlussfolgern, wie ernsthaft dies geschieht.

**■**

**■ 12.3■Das Plugin „Game“**

Eine ganze Reihe interessanter Spiele fasst die Sammlung _Game_ von Vasilis Daoukas zusammen:

Hangman – Galgenmännchen

Crossword – Kreuzworträtsel

Cryptex – Suchrätsel

Millionaire – Wer wird Millionär?

Sudoku – Zahlenkreuzworträtsel

Snakes and Ladders – Schlangen und Leitern

The hidden Picture – Verstecktes Bild

Book with Questions – Buch mit Fragen

All diese Lernspiele werden mit einem einzigen Plugin installiert. Jedes Spiel kann allerdings als eigene Aktivität in einen Kursabschnitt eingefügt werden.

![Image 514](index-502_1.jpg)

![Image 515](index-502_2.jpg)

12.3 Das Plugin „Game“

**479**

**Bild 12.21** Das Plugin _Game_ bietet eine ganze Reihe sehr interessanter Lernspiele. Neben einem einfachen Hangman-Spiel ist unter anderem ein Kreuzworträtsel und eine Variante des TV-Quizes

„Wer wird Millionär“ in diesem Paket enthalten.

**Bild 12.22** Die Moodle-Administration bestimmt, welche Spiele tatsächlich in den Kursen eingesetzt werden dürfen.

![Image 516](index-503_1.png)

**480** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.23** 

Die Auswahl der Materialien und

Aktivitäten in den Kursen nimmt nach

der Installation des Game-Plugins

deutlich an Umfang zu.

**12.3.1■Hangman – Galgenmännchen**

Der Begriff „Galgenmännchen“ mag heute in Stil und Betitelung nicht gerade als „political correct“ gelten, jedoch fand dieses Spiel zum Erraten von Begriffen in Kindertagen immer einen gewissen Zuspruch. Mit jeder falschen Antwort bildete sich am Galgen ein Strich-männchen heraus. Hing das Männchen komplett am Galgen, war das Spiel verloren. Sinn war es also, mithilfe einer richtigen Antwort quasi „Leben“ zu retten.

Die Spielregeln lassen sich in Moodle ein wenig verändern. So kann die maximale Anzahl der falschen Antworten reduziert und das Spiel damit schwieriger gestaltet werden. Auch können mehrere Durchgänge vereinbart werden.

**Wichtige Voraussetzung**

Hangman braucht unbedingt ein gewisses Volumen an Fragen. Sehr gut eignet sich hier ein Glossar,2 was allerdings zum Kursthema passen sollte. Ob dieses Glossar von den Lernenden im Laufe des Kurses erstellt oder von Lehrenden beigesteuert wird, ist dabei unerheblich. Ohne eine Fragenquelle kann jedoch dieses Spiel nicht umgesetzt werden.

■

Wurde Hangman in einem echten Klassenraum gespielt – einige mögen sich noch an Tafel und quietschende Kreide erinnern –, zeichnete man einen Galgen und eine Reihe von Strichen, die als Platzhalter jeweils einen Buchstaben symbolisierten. Zum gesuchten Begriff wurde eine Frage gestellt. Es konnte nun mit dem Raten begonnen werden.

Beim Moodle-Hangman werden natürlich auch Fragen benötigt und idealerweise werden diese Fragen aus dem Kreis der Lernenden formuliert. Dazu eignet sich die in einem vor-2 Es gibt weitere Quellen für die Fragen in den Spielen: Fragenkataloge und Tests. Beides wird in einem späteren Kapitel beschrieben.

![Image 517](index-504_1.jpg)

12.3 Das Plugin „Game“

**481**

herigen Kapitel beschriebene Aktivität _Glossar_ sehr gut. Es wird somit ein doppelter Übungs- und Motivationserfolg erreicht, bei dem sich gewissermaßen Lernende untereinander messen können. Die Trainer-Rolle gibt also lediglich die Rahmenbedingungen vor.

Eine dieser Rahmenbedingungen ist die Begrenzung der Versuche. Die Standardeinstellung sieht sechs falsche Antworten vor. Dann ist das Männchen komplett und das Spiel verloren.

Es ist aber auch durchaus möglich, die Anzahl der tolerierten falschen Antworten zu reduzieren. Wird diese Zahl mit Fehlern erreicht, ist das Spiel zu Ende, wenngleich das Männchen am Galgen noch unvollständig ist. Erleichterungen für die Teilnehmerinnen und Teilnehmer bietet auch die Möglichkeit, den Anfangs- und/oder Endbuchstaben des Lösungsworts vorzugeben.

**Bild 12.24** Als Quelle der Fragen für das Hangman-Spiel kann ein durch Lernende selbst entwickeltes Glossar verwendet werden.

![Image 518](index-505_1.jpg)

![Image 519](index-505_2.png)

**482** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.25** Mit den Einstellungen für das Hangman-Spiel kann die Trainer-Rolle unabhängig von den eigentlichen Fragen einen Einfluss auf den Schwierigkeitsgrad nehmen.

**Bild 12.26** Eine interne Bewertung des Spiels bringt zusätzlichen sportlichen Anreiz.

![Image 520](index-506_1.png)

12.3 Das Plugin „Game“

**483**

**Bild 12.27** Die Standardvorgabe sind sechs mögliche Fehlversuche. Das Spiel kann aber auch mit weniger Versuchen durchgeführt werden.

**12.3.2■Kreuzworträtsel**

Ganz ähnlich wie beim zuvor erläuterten Hangman-Spiel benötigt auch das Kreuzworträtsel eine Quelle für Fragen und Begriffe. Auch hier eignet sich ein _Glossar_ hervorragend, denn es formuliert in den Begriffserklärungen Fragen, deren Lösungsworte die Suchbegriffe des Glossars darstellen.

Der Schwierigkeitsgrad wird von der Trainer-Rolle durch Vorgabe der Höchstzahl von Spalten und Zeilen sowie einer unteren und oberen Grenze der gesuchten Wortzahlen festgelegt.

Je nachdem, wie groß das Rätselfeld letztlich sein soll, können die Fragen unterhalb oder seitlich vom Raster platziert werden.

Wenn das Spiel gestartet wird, sehen die Lernenden ein Raster in waagrechter und senkrechter Anordnung. In den Feldern sind teilweise Zahlen zu finden, die als Referenz zu den Fragen stehen und für die waagrechten und die senkrechten Suchfelder getrennt formuliert werden. Man klickt in das Feld mit der Zahl und es öffnet sich neben der Frage eine Eingabezeile. Dort gibt man das Lösungswort ein. Es wird grundsätzlich Großschreibung verwendet.

![Image 521](index-507_1.jpg)

![Image 522](index-507_2.jpg)

**484** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.28** Die gesuchten Begriffe werden auch hier wieder einem Glossar entnommen, welches von den Lernenden auch selbst in einer Teamarbeit erstellt werden kann.

**Bild 12.29** Es können nur in einem Wort zusammenhängende Begriffe im Rätsel verwendet werden.

Begriffe, die Leerzeichen enthalten, werden nicht verwendet.

![Image 523](index-508_1.jpg)

12.3 Das Plugin „Game“

**485**

**Bild 12.30** Die Eingabe des Lösungsworts erfolgt im Fenster der Fragestellung.

**12.3.3■Cryptex**

Ein dem Kreuzworträtsel ähnliches Spiel ist Cryptex. Hier sind bereits alle Lösungsworte in das Raster eingetragen worden, doch die übrigen Felder sind mit zufällig gewählten Buchstaben belegt. Es ist möglich, dieses Spiel auch im Präsenzunterricht einzusetzen, indem das Raster ausgedruckt wird. Die Lernenden umrahmen dann die Lösungen im Raster mit einem Stift.

Grundlage für dieses Spiel ist wie bereits bei Hangman und beim Kreuzworträtsel (Crossword) ein Glossar. Ebenso wie beim Kreuzworträtsel werden bei Cryptex, also beim Suchrätsel, nur Begriffe verwendet, die kein Leerzeichen enthalten.3 Das Suchrätsel kann als eine sehr anspruchsvolle Aufgabe betrachtet werden und es eignet sich gut als unterhaltsame Ergänzung (auch) des Präsenzunterrichts. Am Ende einer Lehreinheit kann ein solches Suchrätsel aktiviert werden. Die Aufgabe kann zeitlich durch ein Datum und eine Uhrzeit, an der das Spiel geöffnet und geschlossen wird, begrenzt werden. Auch ist die Anzahl der Versuche einstellbar.

3 Dies ist eine sinnvolle Standard-Einstellung, die jedoch durch die Trainer-Rolle ausgeschaltet werden kann.

![Image 524](index-509_1.jpg)

![Image 525](index-509_2.jpg)

**486** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.31** Ein gesuchter Begriff wurde gefunden und wird in die Lösungszeile eingetragen.

**Bild 12.32** Ist der Begriff richtig, wird dieser im Raster hervorgehoben und die Frage aus der Liste entfernt.

![Image 526](index-510_1.jpg)

![Image 527](index-510_2.jpg)

12.3 Das Plugin „Game“

**487**

**Bild 12.33** Alle Fragen wurden richtig beantwortet. Die Fragen sind entfernt. Die Frage an die Trainer-Rolle wird sein: Wer war am schnellsten?

**Bild 12.34** Jeder Versuch wird mit der erreichten Zeit dokumentiert. Hier lassen sich zur Förderung des sportlichen Ehrgeizes auch Ranglisten im Klassenverband aufstellen.

![Image 528](index-511_1.jpg)

**488** 12 Ergänzende Lernhilfen für Moodle

**12.3.4■Sudoku**

Sudoku ist ein Zahlenkreuzworträtsel. Dieses – allgemein sehr beliebte – Rätselspiel ist nicht ohne Weiteres auf fachliche Fragen zu übertragen. Es ist also bei einem Zahlenrätsel nicht möglich, die Antwort „Beschleunigung“ auf eine Frage wie „Was ist die Änderung des Bewegungszustands eines Körpers?“ in ein Zahlenrätsel zu übertragen.

Die Designer dieses Moodle-Spiels haben eine andere Lösung gefunden: Das Sudoku-Spiel sucht in einem Raster von 9 mal 9 (3x3) mal (3x3) Ziffernfeldern eine korrekte Anordnung der Ziffern 1 bis 9. Dabei müssen in jeder Zeile _und_ in jeder Spalte jeweils alle Ziffern erscheinen. Es darf nirgendwo eine Ziffer doppelt erscheinen.

Wie bisher auch können die Fragen idealerweise aus einem Glossar entnommen werden.

Das Glossar eignet sich auch deswegen vorzüglich, weil es in Teamarbeit der Lernenden entwickelt werden kann. Dies motiviert und trainiert.

Beim Aufruf des Sudoku-Rasters werden leere Zellen und ein paar gesetzte Ziffern angezeigt. Die Teilnehmerinnen und Teilnehmer können also sofort versuchen, das Rätsel zu lösen. Allerdings können durch Beantwortung der gestellten Fragen zusätzliche Ziffern freigeschaltet und das Rätsel damit vereinfacht werden. Durch die Beantwortung der Fragen wird das Rätsel also leichter (oder überhaupt erst) lösbar.

**Bild 12.35** Als Quelle der Fragen dient hier wieder ein Glossar.

![Image 529](index-512_1.jpg)

12.3 Das Plugin „Game“

**489**

**Bild 12.36** Beim Spiel gibt es wie üblich einige gesetzte Ziffern. Damit kann man bereits eine Lösung versuchen. Weitere Ziffern werden nach der Beantwortung der Fragen freigeschaltet.

**12.3.5■„Wer wird Millionär“-ähnliches Spiel**

Eine Lernplattform bietet natürlich nicht den frechen Charme und Witz der Moderatoren Günter Jauch (Deutschland) und Armin Assinger (Österreich), die seit vielen Jahren sehr erfolgreich dieses Quiz mit hohen Einschaltquoten im TV moderieren. Beliebt und lehrreich ist es aber trotzdem auch „online“, sodass dieses Quiz auch als Handy- und Computerspiel adaptiert wurde. Das allgemeine Konzept des Millionenspiels ist auch in Moodle einsetzbar.

Anders als in den zuvor beschriebenen Lernspielen dieses Pakets werden die Fragen für dieses Quiz nicht von einem Glossar bereitgestellt. Das Glossar eignet sich nicht, weil es nur einen Begriff als Antwort liefern kann. Das Millionenquiz bietet jedoch pro Frage vier Alternativen an. Aus diesem Grund kann nur eine Frage vom Typ Multiple Choice4 verwendet werden, die direkt aus einer Fragensammlung oder aus einem Test entnommen werden muss.

Für dieses Quiz bedarf es also einer gewissen Vorbereitung. Es können nur Multiple Choice-Fragen mit einer eindeutigen Lösung verwendet werden. Der Fragenpool muss darüber hinaus so umfangreich sein, dass nicht nur die zehn Fragen für dieses eine Spiel vorhanden sind, sondern auch die Chance besteht, verschiedene neue Fragen bei einem erneuten Versuch zu finden.

4 Der Fragentyp heißt _Multiple_ Choice – Mehrfache Auswahl. Dieser Fragentyp kann, muss aber nicht, mit mehreren möglichen richtigen Antworten belegt werden. Für das Millionenquiz eignen sich nur Fragen mit einer eindeutigen Lösung.

![Image 530](index-513_1.jpg)

**490** 12 Ergänzende Lernhilfen für Moodle

Wie beim TV-Quiz ist auch hier nur eine Antwort möglich. Das Spiel wird fortgesetzt bis eine falsche Antwort gegeben wird oder (hier) die 150 000 Punkte gewonnen wurden. Es gibt auch drei Joker: „Fifty-Fifty“, „Telefonjoker“ und den „Publikumsjoker“. Natürlich kann man nicht wirklich jemanden anrufen. Auch ist kein „Chatkandidat“ vorgesehen. Der Publikums- und Telefonjoker werden deswegen von Moodle simuliert. Wer wirklich nicht weiter weiß, kann das Spiel auch direkt beenden.

**Bild 12.37** Für das Millionenquiz kommen nur der Fragenkatalog und Tests als Fragenquelle in Betracht. Das Glossar ist hier nicht einsetzbar, weil mehrere Antwortalternativen benötigt werden.

![Image 531](index-514_1.jpg)

12.4 Standards für externe Lernpakete

**491**

**Bild 12.38** Ähnlich wie in der TV-Show können Joker genutzt werden. Diese werden natürlich vom System simuliert.

**■**

**■ 12.4■Standards für externe Lernpakete**

Wenn hier von Standards für externe Lernpakete geschrieben wird, sind eigentlich die Standards gemeint, mit denen externe Lernpakete die in ihnen erzielten Ergebnisse an ein Lernmanagement-System weitergeben, von dem ausgehend sie aufgerufen wurden.

Das sind die beiden wesentlichen Aufgaben der Standards:

Aufruf des externen Lernpakets aus einem Lernmanagement-System (z. B. Moodle) heraus,

Übergabe der Kursergebnisse, die im externen Lernpaket erzielt wurden.

Zwei der bekanntesten Standards sind SCORM – dieser Standard ist relativ alt, aber häufig genutzt – und Learning Tools Interoperability (LTI).

**Keine Entwickler-Details**

Sowohl SCORM als auch LTI sind sehr umfangreiche Standards mit eigenen

Philosophien. Sie bieten Stoff für jeweils eigene Bücher und können in diesem Werk – das Thema ist Moodle – nicht erschöpfend behandelt werden.

■

**492** 12 Ergänzende Lernhilfen für Moodle

**12.4.1■Learning Tools Interoperability® (LTI)**

Ein zunehmend wichtiger werdender Standard kommt vom IMS Global Learning Consortium: Learning Tools Interoperability® oder kurz LTI. Die Abkürzung IMS steht hier für Instructional Management System. Ziel der Aktivität des Konsortiums war und ist es, einen offenen Standard für E-Learning-Tools zu entwickeln, um digitale Lehrmittel austauschbar und wiederverwendbar in unterschiedlichen Plattformen gestalten zu können.

**Offizielle Webseite des IMS Global Learning Consortiums**

Der Standard Learning Tools Interoperability® (LTI) wurde vom IMS Global Learning Consortium entwickelt und gepflegt:

[_https://www.imsglobal.org/activity/learning-tools-interoperability_](https://www.imsglobal.org/activity/learning-tools-interoperability)

Spezifikation von LTI v. 1.3 vom 16. 04. 2019:

[_https://www.imsglobal.org/spec/lti/v1p3/_](https://www.imsglobal.org/spec/lti/v1p3/)

■

**12.4.2■Shareable Content Object Reference Model (SCORM)**

Auch ein von der Firma Rustici Software LLC entworfener (Quasi)-Standard verfolgt das Ziel der Austausch- und Wiederverwendbarkeit elektronischer Lehrmittel. Es gibt eine aktuellere Version, allerdings ist nach wie vor die Version SCORM 1.2 in vielen Systemen der Standard. Auch in Moodle wird die Kompatibilität erwartet. Hier ist auf jedem Fall Bedarf für weitere Entwicklungen gegeben.

**SCORM – offizielle Webseite**

Entwickler des SCORM-Standards ist ein kommerzielles Unternehmen, die

Rustici Software LLC:

[_https://scorm.com_](https://scorm.com)

Eine Übersicht zu den SCORM-XML-Tags ist unter der folgenden Seite zu finden:

[_https://scorm.com/scorm-explained/technical-scorm/content-packaging/_](https://scorm.com/scorm-explained/technical-scorm/content-packaging/metadata-structure/)

[_metadata-structure/_](https://scorm.com/scorm-explained/technical-scorm/content-packaging/metadata-structure/)

■

12.5 Externe Tools (Auswahl)

**493**

**■**

**■ 12.5■Externe Tools (Auswahl)**

In diesem Abschnitt sollen nun zwei externe Lern-Tools vorgestellt werden:

Hot Potatoes kann über den SCORM-Standard in Moodle integriert werden. Hot Potatoes gehört zu den etablierten Tools, bietet allerdings nur eine begrenzte Zahl von Lernspielen an.

H5P ist eine noch sehr junge Technologie, die viel Potenzial für die Gestaltung multimedialer und interaktiver Lerninhalte bietet.

Beide externe Tools sind von großer Bedeutung in der Gestaltung didaktisch guter Lehrkonzepte. Sie dienen der Auflockerung elektronischer Kurse und fördern die Motivation beim Lernen. Zudem bieten diese Tools die Möglichkeit, den Stoff auf verschiedene Weise zu präsentieren. Man erreicht damit Lernende mit unterschiedlichen Talenten und Interessen.

**12.5.1■Hot Potatoes**

Hot Potatoes ist eine Art bildungstechnischer Kreativbaukasten, der aus sechs Komponenten besteht. Zunächst einmal sind die fünf Programmmodule für die Gestaltung der interaktiven Lehreinheiten zu nennen. Darüber hinaus gibt es den sogenannten _Masher_. Diese Programmkomponente ist für die Kombination der Lehreinheiten und deren Export zu -

ständig.

Die fünf Programmodule sind:

JQuiz – Multiple Choice-Quizfragen

JCloze – Lückentext

JCross – Kreuzworträtsel

JMatch – Zuordnung

JMix – der „Schüttelsatz“

**Download Hot Potatoes**

Hot Potatoes ist kostenlos auf der deutschsprachigen Seite zu bekommen.

Es empfiehlt sich, stets die aktuellste Version zu verwenden. Beta-Versionen sind grundsätzlich noch in einer fortgeschrittenen Testphase und sollten für den Live-Einsatz nur nach einer ausführlichen Prüfung verwendet werden.

[_https://www.hotpotatoes.de_](https://www.hotpotatoes.de)

■

![Image 532](index-517_1.jpg)

![Image 533](index-517_2.jpg)

**494** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.39** Wer Programme aus dem Internet herunterlädt, sollte grundsätzlich die originalen Quellen verwenden.

**12.5.1.1■Hot Potatoes – externes Programm**

Hot Potatoes ist ein eigenständiges Programm. Es werden also keinerlei administrative Rechte im Moodle-System benötigt, um Lehrinhalte mit Hot Potatoes zu erstellen. Um diese später in einen Kurs einzugliedern, benötigt es allerdings Teacher-Rechte. Diese sind nötig, um ein externes Lernpaket zu verwenden.

Die Kurseinheiten werden einzeln in jeweils einem Lernspiel erstellt. Mithilfe des _Mashers_ werden die Lektionen kombiniert und in das richtige Format exportiert. Die Bedienung erfolgt über ein grafisches Menü des Programmfensters.

**Bild 12.40** 

Hot Potatoes ist ein Paket aus fünf

verschiedenen Lernspielen.

![Image 534](index-518_1.png)

12.5 Externe Tools (Auswahl)

**495**

**12.5.1.2■JCloze – der Lückentext**

In Moodle gibt es den Fragentyp5 _Lückentext_. Dieser Aufgabentyp ist jedoch mit einer recht unkomfortablen Syntax verbunden, um die Fragen zu entwickeln. Hot Potatoes bietet hier mit JCloze eine Alternative. Dabei ist es nicht notwendig, besondere Regeln zu beachten. Es wird einfach der Textblock in das Editorfenster hineinkopiert und in diesem Text werden bei Bedarf die entsprechenden Lücken eingebaut. Das passiert mit einem Mausklick.

Lücken können gezielt gesetzt werden (empfohlen), wobei hier konkret die interessanten Fachbegriffe ausgewählt werden. Alternativ dazu kann man automatisch Lücken setzen lassen, indem der Abstand der Lücken mit der Zahl der Wörter festgelegt wird. Diese Variante eignet sich für Sprachtrainings, bei denen die Lernenden die Sätze vollenden müssen. Zu kurze Intervalle sind jedoch schwierig, weil dann die Sätze nicht mehr mit eindeutigen Worten rekonstruiert werden können.

Grundsätzlich können alle Lücken in der Aufgabenstellung direkt nachbearbeitet oder –

wenn sie ohne Sinn wären – aus dem Text gelöscht werden. In diesem Fall wird der Text mit dem ursprünglich an dieser Position befindlichen Begriff wiederhergestellt. Mit der Bearbeitung der Lücken ist es möglich, wahrscheinlich verwendete Alternativbegriffe festzulegen, die ebenfalls als richtig angesehen werden. Wenn rein fachliche Begriffe geprüft werden sollen, dann können auch mögliche Schreibfehler und Varianten verwendet werden.

Das sind zum Beispiel Groß- und Kleinschreibung, Schreibweisen mit „ss“ oder „ß“ etc.

**Bild 12.41** Sollen einfache Schreibfehler toleriert werden? In diesem Fall kann zum Beispiel ein kleingeschriebenes Lösungswort alternativ als richtig anerkannt werden.

5 Die Fragentypen des Moodle-Systems werden im Kapitel zu Fragenkatalogen in Moodle erläutert.

![Image 535](index-519_1.png)

**496** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.42** Um das fertige Lernspiel in Moodle importieren zu können, muss es aus Hot Potatoes heraus in ein SCORM-Archiv exportiert werden.

**12.5.1.3■JQuiz – Multiple Choice-Fragen**

Multiple Choice-Fragen sind ein Klassiker in elektronischen Prüfungen. Sie haben den Vorteil, ein schnelles und eindeutiges Ergebnis liefern zu können. Allerdings sind diese Fragen auch nicht unumstritten, was nicht allein für elektronische Prüfungen gilt. Bei Multiple Choice-Fragen kommt es darauf an, nicht das Geschick des sinnerfassenden Lesens, sondern das Fachwissen zu prüfen.

Es werden eine Frage und mehrere Antworten zu dieser Frage formuliert. Die richtige Antwort bzw. die richtigen Antworten werden mit einer Checkbox als richtig markiert. Sehr wichtig bei elektronischen Lehrsystemen und vor allem bei den Prüfungen ist ein direktes Feedback. Dies sollte sowohl bei einer richtigen, vor allem aber auch bei einer falschen Antwort direkt erfolgen. In der Konfiguration der Antworten lässt sich ein Feedback formulieren, was auch direkt auf die Antwortmöglichkeiten abgestimmt werden kann.

**Ziel von Feedback in elektronischen Lernsystemen**

Feedback gehört zu den wichtigsten didaktischen Werkzeugen einer Lehrerin oder eines Lehrers. Es genügt nicht, einfach eine Antwort oder ein Statement eines Lernenden mit richtig oder falsch zu bewerten. Die Bewertung muss

begründet werden, damit auch aus einem Fehler ein Lernerfolg erwachsen

kann. Besonders wichtig ist dies in elektronischen Lehrsystemen, wo es

meist keinen direkten Kontakt zu den Lehrenden gibt.

■

![Image 536](index-520_1.png)

12.5 Externe Tools (Auswahl)

**497**

**Bild 12.43** Hot Potatoes bietet eine sehr einfache Oberfläche zur Erstellung von Multiple-Choice-Fragen.

**12.5.1.4■JCross – das Hot-Potatoes-Kreuzworträtsel**

Kreuzworträtsel sind grundsätzlich sehr beliebt, vor allem im Sprachentraining, wo es auf richtige Schreibweisen ankommt. Die Variante in Hot Potatoes kann nicht auf ein Glossar in Moodle oder auf die im System vorhandene Fragensammlung zugreifen. Die Begriffe müssen manuell in die Aufgabenstellung eingearbeitet und die zugehören Fragen entsprechend formuliert werden. Das ist selbstverständlich mit einem gewissen Aufwand verbunden.

Es wird zuerst eine Wortliste erstellt. Diese enthält die Begriffe, die später in das Kreuzworträtsel einzutragen sind. Aus dieser Wortliste wird das Raster erzeugt, in das die Lösungsbegriffe horizontal und vertikal eingetragen werden. Damit ist die Lösung bei der Entwicklung des Rätsels bereits ersichtlich.

Die Fragen zu den Lösungsbegriffen werden nachträglich formuliert. Natürlich ist das eine sehr zeitaufwendige Arbeit. Man kann allerdings Fragen und die Begriffe extern vorbereiten. Beispielsweise lassen sich Fragen und die Begriffe in einer Excel- oder LibreOffice-Tabelle in größeren Volumina vorbereiten und dann per Copy and Paste in die Felder des Hot-Potatoes-Programms einfügen.

**JCross ist mit Vorbereitungsaufwand verbunden**

Der Vorbereitungsaufwand für das JCross-Modul in Hot Potatoes ist vergleichsweise groß, weil Hot Potatoes als externes Tool nicht auf Moodle-interne Fragensammlungen zugreifen kann. Es fehlt leider auch eine direkte Import-Funktion auf Tabellen oder Textdateien.

■

![Image 537](index-521_1.png)

![Image 538](index-521_2.png)

![Image 539](index-521_3.png)

**498** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.44** 

Zuerst werden die Lösungsbegriffe fest-

gelegt. Das Raster und die Anordnung der

Begriffe errechnet Hot Potatoes.

**Bild 12.45** Die Lösungsbegriffe werden nach der Berechnung des Rasters in dasselbe automatisch eingetragen. Darum müssen sich Lehrende nicht kümmern.

**Bild 12.46** 

Nach dem Aufbau des Rasters

werden die Fragestellungen

zu jedem einzelnen Begriff

formuliert.

![Image 540](index-522_1.png)

12.5 Externe Tools (Auswahl)

**499**

**12.5.1.5■JMatch – Zuordnung**

Ein sehr einfaches Spiel, dessen Schwierigkeitsgrad nicht zuletzt auch von der Fragestellung als solche abhängt, ist das Zuordnungsspiel JMatch – sinnvoll einsetzbar ist es natürlich in der Sprachenausbildung. So können Verben beispielsweise verschiedenen Zeitfor-men zugeordnet werden. Vorsichtig muss man jedoch sein, wenn es um die Zuordnung der sprachlichen Fälle geht, was meist nicht eindeutig gelingt. Zum Beispiel ist bei „Sprache“

(singular) der Genitiv und der Dativ jeweils „der Sprache“. Die beiden Antworten wären identisch. Das erkennt das Spiel jedoch nicht, weil es feste Zuordnungen zu den Eingabe-feldern anlegt, nicht jedoch zu deren Inhalten.

**Beim Zuordnungsspiel: Auf Eindeutigkeit achten!**

Beim Zuordnungsspiel dürfen auf keinem Fall zwei identische Lösungs- oder Frageworte verwendet werden. Was formal richtig ist, wird vom System leider nicht zwingend erkannt.

■

**Bild 12.47** 

Bei der Formulierung der Lösungs-

paare muss auf deren Eindeutig-

keit geachtet werden. Das Spiel

wertet intern lediglich die Zuord-

nung der Felder aus, versteht aber

nicht, was darin enthalten ist.

**12.5.1.6■JMix – der „Schüttelsatz“**

Zum Üben des Satzbaus im Sprachtraining eignet sich auch der _Schüttelsatz_. Satzfragmente werden vom System durcheinander gewürfelt und die Aufgabe der Lernenden ist es, diese in die richtige Reihenfolge zu bringen. Das Spiel lässt sich auch mit einer kleinen Geschichte oder einem Fachtext gestalten.

Lehrende formulieren in Hot Potatoes _JMix_ eine Aufgabe, indem sie Satzfragmente Zeile für Zeile in das Feld Lösungssatz eintragen. In der Festlegung des Textes muss der Text natürlich in der richtigen Reihenfolge formuliert werden.

![Image 541](index-523_1.png)

![Image 542](index-523_2.png)

**500** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.48** 

Die Lösungsfragmente werden in

einzelnen Zeilen formuliert. Die

Reihenfolge muss hier allerdings

stimmen. Die Verwürfelung übernimmt

das Programm.

**12.5.1.7■Der Masher**

Der _Masher_ ist nicht unbedingt erforderlich, um einzelne Hot-Potatoes-Aufgaben zu erstellen, denn diese können direkt aus dem Editor in ein SCORM-Archiv exportiert und in einen Moodle-Kurs als Lernpaket importiert werden. Allerdings lassen sich mithilfe des Mashers mehrere Aufgaben – auch ganz verschiedene Typen – miteinander kombinieren und als ein Gesamtpaket speichern.

Die Dateien werden gezielt ausgewählt und können nachträglich in ihrer Reihenfolge bearbeitet werden. Mit einem Klick auf _Einheit erstellen_ wird ein gesamtes Lernpaket erstellt.

**Bild 12.49** Es werden gezielt Hot-Potatoes-Aufgaben – nicht die SCORM-Pakete – für ein gesamtes Lernpaket ausgewählt.

![Image 543](index-524_1.png)

![Image 544](index-524_2.png)

12.5 Externe Tools (Auswahl)

**501**

**Bild 12.50** 

Die Reihenfolge der Lernaktivitäten

kann verändert und der Inhalt jederzeit

bearbeitet werden.

**12.5.1.8■Hot Potatoes in Moodle verwenden**

Hot-Potatoes-Lernspiele werden als _Lernpaket_ in Moodle importiert. Dazu müssen die Pakete nach dem SCORM-Standard aus Hot Potatoes exportiert werden. Es lassen sich sowohl einzelne Lernspiele als auch ganze Pakete importieren. Die Einbindung des Pakets erfolgt mit der Aktivität _Lernpaket_ (Bild 12.51).

Das Verfahren zum Import des Lernpakets entspricht dem gewöhnlichen Upload einer Datei. Im einfachsten Fall wird das „gezippte“ SCORM-Paket mit der Maus in das freie For-mularfeld in Moodle geschoben. In der Beschreibung sollte in kurzen Worten auf die Aufgabenstellung eingegangen und diese Beschreibung aktiviert werden. Wie bei allen Aktivitäten, die in einem Moodle-Kurs eingesetzt werden können, gehören ein Name und eine Beschreibung zu den Pflichtinformationen.

**Bild 12.51** 

Mithilfe dieses Symbols werden Lernpakete nach dem

SCORM-Standard in Moodle-Kursen als Aktivität eingefügt.

![Image 545](index-525_1.jpg)

![Image 546](index-525_2.png)

**502** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.52** Das Lernpaket wird als ZIP-Datei hochgeladen. Es muss aus der Quelle in das SCORM-Format exportiert werden.

**Bild 12.53** Ein Klick auf das durch eine Zahl markierte Feld öffnet eine Frage (waagrecht und/oder senkrecht). Die Antwort wird in das Eingabefeld eingetragen und erscheint anschließend im Raster des Rätsels.

![Image 547](index-526_1.png)

![Image 548](index-526_2.jpg)

12.5 Externe Tools (Auswahl)

**503**

**Bild 12.54** Fehler werden intern gezählt. Am Schluss des Spiels wird das Ergebnis angezeigt und für die Auswertung durch die Lehrenden gespeichert.

**Bild 12.55** Die Ergebnisse der Hot-Potatoes-Lerneinheiten können erfasst und von den Lehrenden ausgewertet werden.

![Image 549](index-527_1.jpg)

**504** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.56** Ein mit dem Masher erstelltes Lernpaket bietet in einer Aktivität alle im Paket enthaltenen Lernspiele an. Diese können gezielt per Mausklick bearbeitet werden.

**12.5.2■HTML 5 Package (H5P)**

H5P steht für HTML5 Package. Damit wird lediglich die grundlegende Technik beschrieben, ohne auch nur ansatzweise die Potenziale dieses Content Collaboration Frameworks zu betonen. H5P dient der Entwicklung multimedialer und vor allem tatsächlich interaktiver Lehrinhalte. So können interaktive Videosequenzen mit Zusatzinformationen und Aufgaben zu einzelnen Abschnitten des Videos formuliert werden.

Interessant sind aber auch die Möglichkeiten, direktes Feedback einzuholen, was auch unterstützend im Präsenzunterricht möglich ist. Obwohl H5P noch eine sehr junge Technologie ist – sie basiert unter anderem auf HTML5 und kann auch multimediale Inhalte ohne zusätzliche Browser-Plugins in einer Webseite darstellen und wiedergeben–, gibt es bereits eine starke Community und eine Reihe von guten Lernmaterialien, die frei verfügbar sind.

Diese Lernmaterialien kann man kostenlos mit einem Online-Editor erstellen, wenn man sich auf der Projektseite H5P.org registriert. Man muss allerdings beachten, dass die Nutzung dieser Plattform auch Regeln mit sich bringt: So sind die darin erstellten Lernmodule grundsätzlich offen und dürfen auch in der Community genutzt und erweitert werden.

Die Verwendung dieser – selbst erstellten, aber doch öffentlich gehosteten – Lehrmaterialien ist in Moodle sehr einfach möglich: Mit Moodle 3.8 findet man im Text-/HTML-Editor einen Button, der ein kleines Eingabefeld öffnet. In dieses wird der Link auf die Lehreinheit gesetzt und kann damit in Moodle verwendet werden.

12.5 Externe Tools (Auswahl)

**505**

Eine andere Möglichkeit, die zudem ein eigenes Urheberrecht zulässt, ist die Nutzung eines eigenen H5P-Editors, der direkt in das Moodle-System als Plugin eingebunden werden kann. Dieses Plugin muss allerdings zuerst von der Moodle-Administration in das System installiert und konfiguriert werden.

**H5P-Aktivitäten-Plugin installieren!**

Neben der Möglichkeit, H5P-Inhalte in den Text-/HTML-Editor einer Kurs-

aktivität integrieren zu können, kann in Moodle auch ein H5P-Plugin direkt installiert werden. Damit ist es möglich, unabhängig von einem Account bei H5P.org Inhalte in Moodle zu gestalten.

■

H5P-Inhalte können – wenn sie extern über H5P.org erstellt wurden, über das Text-/

HTML-Editorfenster in eine beliebige Moodle-Aktivität eingebaut werden, wenn sie mit dem Texteditor arbeitet. Um jedoch eigene H5P- _Aktivitäten_ in Moodle-Kurse einbauen zu können, müssen der Trainer-Rolle durch die Moodle-Administration entsprechende Rechte6 eingeräumt werden:

Eingebettetes H5P hinzufügen: _atto/h5p:addembed_

Bereitstellen von H5P-Inhalten: _moodle/h5p:deploy_

Einstellung der H5P-Anzeigeoptionen: _moodle/h5p:setdisplayoptions_

Installation (empfohlener) Bibliotheken: _mod/hvp:installrecommendedh5plibraries_ Manche Fähigkeiten sind mit dem Risiko des Cross Site Scripting verbunden! Deswegen sind Administratoren in der Regel sehr umsichtig bei der Zuweisung dieser Rechte zu einer Rolle. Unter Umständen entscheidet sich die Administration für die Erschaffung einer speziellen Teacher-Rolle, der H5P-Rechte als Editoren eingeräumt werden. Aber es können auch zusätzliche Student-Rollen mit gestalterischen Rechten mit H5P eingerichtet werden.

H5P und dessen Möglichkeiten bieten sich förmlich an, Projekte durch Lernende ent wickeln zu lassen. Die Idee des _Flipped Classrooms_ 7 kann hier mit nahezu allen möglichen Medien des Internet und der Computertechnik umgesetzt werden. Die Lernenden erarbeiten selbstständig zu bestimmten Themen gestellte Aufgaben, recherchieren selbstständig, lernen Quellen zu bewerten und die Inhalte auf Plausibilität zu überprüfen. Die Ergebnisse bereiten sie multimedial auf und haben so auch an der Ausarbeitung sowie der Präsentation Freude. Dies steigert die Motivation.

6 Bitte die Schreibweisen beachten: h _**5**_ p und h _**v**_ p werden in der Bezeichnung der Fähigkeiten richtig verwendet.

Über die Erlaubnis, diese Fähigkeiten zu nutzen, entscheidet die Moodle-Administration.

7 Unter dem Begriff des _Flipped Classrooms_ versteht man gewissermaßen die Umkehr der Handlungen im Klassenraum. Die Lernenden erarbeiten den Unterrichtsstoff selbstständig und tragen diesen vor. Die Lehrenden geben den roten Faden vor, wirken moderierend und beratend. Selbstverständlich obliegt ihnen noch die endgültige Bewertung der Arbeiten.

**506** 12 Ergänzende Lernhilfen für Moodle

**Risikobewertung bei Student-Projekten**

H5P ist eine höchst interaktive und vielseitige Lerntechnologie. Sie hat große Potenziale für Lehrende, um interessante, multimediale und eben interaktive Lehreinheiten zu gestalten. Allerdings fördert es auch die Kreativität der Lernenden, wenn diese selbst Kurseinheiten ausarbeiten und online präsentieren können. Weil die Gestaltung von HTML5- und JavaScript-Inhalten auch das

Risiko des Cross Site Scripting mit sich bringt, empfiehlt es sich, eine neue Student-Rolle anlegen zu lassen, die das Recht zur Gestaltung von H5P-Inhalten erhält.

■

**12.5.2.1■H5P-Inhaltstypen**

Während bei Hot Potatoes fünf Spiele definiert sind, gibt es eine Vielzahl von Inhaltstypen für H5P. Es lohnt sich, sich mit diesen auseinander zu setzen und sie Schritt für Schritt in das eigene Lehrkonzept zu integrieren. Verschiedene Inhaltstypen sind bereits aus anderen Moodle-Aktivitäten oder aus Hot Potatoes bekannt und entsprechend ebenso in H5P umgesetzt worden. Die Mehrzahl der Inhaltstypen ist jedoch völlig neu. Folgende Inhaltstypen kennt H5P:

**Accordeon:** Sichtbar sind zunächst kurze Schlagworte oder einfache Beschreibungen.

Klickt man auf den Begriff, öffnet sich eine detaillierte Beschreibung. Der Inhaltstyp kann in rein präsentierenden Lektionen verwendet werden, wo es vermieden werden soll, Lernende sofort mit einer großen Informationsflut zu überfordern. Der Inhaltstyp kann aber auch der Selbstkontrolle dienen, wobei kurze Kontrollfragen sichtbar sind und mit einem Mausklick die Lösung eingeblendet wird.

**Agamotto:** eine Slideshow-Variante zur Darstellung von Bildern und erklärenden Texten.

**Arithmetic Quiz:** Rechenaufgaben werden gelöst. Wird dieses Quiz nach Zeit durchgeführt, fördert es die Fähigkeit des Kopfrechnens.

**Audio Recorder:** Aufnahmemöglichkeit für selbst gesprochene Texte oder – im Musik-unterricht – selbst gesungene Lieder bzw. Instrumentalaufnahmen.

**Branching Szenario:** Fragen mit verschiedenen Antwortmöglichkeiten werden wie Checklisten durchgegangen. Wenn der Lernende einen falschen Lösungsweg wählt, be -

ginnt das Szenario von Neuem. Beispielsweise könnte hier ein theoretisches Szenario durchgesprochen werden, wie eine stabile Seitenlage bei der Ersten Hilfe durchzuführen ist.

**Chart:** Verschiedene Diagrammtypen eignen sich zur Darstellung von Ergebnissen aus Aufgaben der Mathematik oder Statistik etc.

**Collage:** Die Lernenden erarbeiten aus verschiedenen Bildern eine Bildersammlung und bereiten diese für die Präsentation im Kurs auf.

**Column:** Hier können verschiedene Inhaltstypen kombiniert werden.

**Course Presentation:** Eine vereinfachte Form einer „PowerPoint“-ähnlichen Präsentation. Allerdings sollte hier nicht das Leistungsvolumen einer ausgereiften Präsentations-software erwartet werden.

12.5 Externe Tools (Auswahl)

**507**

**Dialog Cards:** „Flash Card Set“-Lernkartenspiel.

**Dictation:** Eine Audio-Aufzeichnung eines Diktats durch einen Lehrenden wird im Kurs von den Lernenden gehört. Diese schreiben die gehörten Sätze in die Lösungsfelder. Die Aufnahme kann mit einem beliebigen Programm oder direkt mit dem H5P-Audio Recorder erfolgen.

**Documentation Tool:** Ein durch ein Webformular geführtes Dokumentationswerkzeug.

Es eignet sich für einfache Formen eines „Projektmanagements“ zur Abarbeitung der Meilensteine.

**Drag and Drop:** Zuordnungsspiel, bei dem Texte und Bilder einander zugeordnet werden.

**Drag the Words:** Lückentextspiel, wobei die fehlenden Wörter aus einem Lösungspool gewählt und mit der Maus an die richtige Stelle geschoben werden.

**Essay:** Lernende schreiben einen kurzen Text zu einer Aufgabe. Das Programm prüft, ob bestimmte Stichworte im Text auftauchen. Dieser Inhaltstyp sollte jedoch keinesfalls von einer Lehrperson unkommentiert verwendet werden.

**Fill in the blanks:** Lückentext.

**Find the Hotspots**: Lernende müssen zu einer Aufgabenstellung in einem Bild den passenden Bereich finden und markieren. Das Tool eignet sich gut für spontane Überprüfun-gen während einer Präsenzphase, zum Beispiel in der Kurvendiskussion in der Mathematik: „Bezeichnen Sie in der vorliegenden Kurve einen Wendepunkt!“

**Find the Words:** Suchrätsel, vergleichbar dem „Cryptex“ (Abschnitt 12.3.3).

**Flash Cards:** Ein weiteres Lernkartenspiel.

**Guess the Answer:** Ein Lernkartenspiel mit Bildfragen.

**iFrame-Embedder:** Mithilfe eines iFrames wird es möglich, Inhalte anderer Webseiten einzubauen, ohne dabei geltende Urheberrechte zu verletzen. Allerdings werden iFrames nicht von allen Browsern unterstützt, denn sie können deaktiviert werden.

**Image Hotspots:** Ein Bild wird mit anklickbaren Informationen versehen. So können die Lernenden per Mausklick gewissermaßen „Fragen an das Bild richten“.

**Image Juxtaposition:** Vergleich zweier Bilder durch Überlagerung.

**Image Pairing:** Zuordnungsspiel mit Bildern.

**Image Sequencing:** Die Lernenden müssen eine Auswahl von Bildern in die richtige Reihenfolge bringen.

**Image Slider:** Slideshow-Präsentation mehrerer Bilder.

**Mark the Words:** Die Lernenden markieren Wörter, die der Aufgabenstellung entsprechen.

**Memory Game:** Klassisches Memory-Spiel mit verdeckten Kartenpaaren.

**Multiple Choice:** Beim Klassiker, besonders für Fragestellungen in E-Learning-Systemen, werden zu einer Fragestellung mehrere mögliche Antworten angeboten. Eine oder durchaus auch mehrere Antworten können richtig sein.

**Personality Quiz:** Es lassen sich analytische Fragen gestalten, mit denen Ansichten oder

„Persönlichkeitsbilder“ ausgewertet werden. Dabei ist es natürlich entscheidend, wie der Verfasser der Aufgaben die Gewichtung und die Interpretationsschwerpunkte setzt. Das

![Image 550](index-531_1.jpg)

**508** 12 Ergänzende Lernhilfen für Moodle

Personality Quiz ist deswegen eine hochinteressante Aufgabe, um die eigene Objektivität zu schulen. Es ist nicht alleine für die Ausbildung von Psychologen oder Kommunika-tionswissenschaftlern interessant.

**Quiz:** Dieser Inhaltstyp hat Parallelen zum _Masher_ in Hot Potatoes. Es ist hierbei möglich, ein kombiniertes Quiz aus verschiedenen Fragetypen zu entwickeln. Für jede Frage wird eine Bewertung ausgegeben und am Schluss des Quiz eine Gesamtbewertung (Zahl der richtigen Lösungen zu maximal erreichbaren Punkten).

**Single Choice Set:** Zu den gestellten Fragen gibt es nur eine einzige richtige Antwort.

**Summery:** Es werden hintereinander mehrere Fragen gestellt. Grundsätzlich ist jeweils eine Aussage richtig, die mit der Maus angeklickt wird. Nach der Antwort wird automatisch die nächste Frage sichtbar.

**True-False:** Die Lernenden bewerten, ob die präsentierten Aussagen wahr oder falsch sind.

**Timeline:** Die Lernenden erstellen eine Zeitleiste und können dazu passende Texte und Illustrationen per Mausklick einblenden. Als Einsatzschwerpunkt bietet sich Geschichts-unterricht an, aber auch andere Projekte lassen sich in einer Zeitleiste abbilden. Besonders interessant ist dies für Teamarbeiten. Zusätzlich können auch Lehrende das Instrument nutzen, um beispielsweise das Curriculum des laufenden Semesters zu präsentieren.

**Virtual Tour:** Auf einem Bild – auch auf einer 360°-Aufnahme – können Hotspots platziert werden, die Lernende suchen und erforschen sollen.

**Video:** Es wird nicht nur ein einfaches Video präsentiert, sondern dieses durch Break-points und interaktive Elemente ergänzt.

Die Inhaltstypen werden permanent ergänzt und weiterentwickelt. Es ist deswegen immer auch lohnenswert, die H5P.org-Projektseite zu besuchen.

**Bild 12.57** Auf der Projektseite h5p.org gibt es eine Übersicht der aktuell verfügbaren Inhaltstypen.

![Image 551](index-532_1.jpg)

12.5 Externe Tools (Auswahl)

**509**

**12.5.2.2■H5P in Moodle-Aktivitäten**

H5P-Inhalte können in Moodle auf verschiedene Weise genutzt werden. In diesem Abschnitt wird die Integration fertiger H5P-Inhalte in Textseiten vorgestellt. Es gibt im Editor ein kleines Icon mit schwarzem Untergrund und dem H5P-Logo. Damit wird ein kleines Formular geöffnet, welches mit einem einfachen Link auf die H5P-Ressource befüllt wird.

Dieser Inhalt muss allerdings zuerst einmal erstellt werden. Der einfachste Weg dazu ist ein eigener – kostenloser – Zugang zu H5P.org, der in wenigen Minuten eingerichtet ist und lediglich eine eigene E-Mail-Adresse erfordert.

**Achtung: Spamfilter arbeiten oft unpräzise!**

Möglicherweise erwartet man eine Bestätigungsmail von H5P.org und wartet vergebens. Es kann sich in diesem Fall ein Blick in den Spamordner des

Posteingangs lohnen. Das gleiche Problem hat man möglicherweise auch

mit der Bestätigungsmail bei der Registrierung am Moodle-System bereits

gehabt.

■

**Bild 12.58** Es soll eine Aufgabe des Inhaltstyps „Drag and Drop“ angelegt werden.

![Image 552](index-533_1.jpg)

![Image 553](index-533_2.jpg)

**510** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.59** Auch H5P fordert – unabhängig von deren Formulierung – eine Beschreibung der Aufgabe.

**Bild 12.60** Die fertige Aufgabe kann zunächst direkt in der H5P-Plattform getestet und optimiert werden. Über den unscheinbaren Link _<> Embed_ kann der Link für den späteren Moodle-Import abgerufen werden.

![Image 554](index-534_1.png)

12.5 Externe Tools (Auswahl)

**511**

**Bild 12.61** Der komplette Einfüge-Code wird markiert und kopiert. Dieser Code wird in Moodle eingefügt.

Ist der H5P-Inhalt erstellt, kann dieser direkt von der Quelle (H5P.org) in die Moodle-Aktivität als _iFrame_ 8 importiert werden. Im Beispiel wurde eine sehr einfache Aktivität _Textseite_ gewählt. Im Texteditor wird das H5P-Symbol gewählt, was in der Werkzeugleiste über dem Textfenster auswählbar ist. Es ist allerdings zu beachten, dass der Einsatz von iFrames aus Gründen des Datenschutzes nicht unumstritten ist. In iFrames werden Inhalte anderer Webseiten eingebunden. Das bedeutet, dass diese Seiten auch Cookies setzen dürfen, die dabei helfen können, das Surf- und Benutzerverhalten zu analysieren. Das ist nicht grundsätzlich verboten, jedoch muss im Sinn der Datenschutzgrundverordnung darauf hingewiesen werden.

**Achtung: Es greift die DSGVO!**

Mit einer Verlinkung auf den H5P.org-Webserver wird der eigene lokale Server verlassen. Die Systemadministration hat somit keinen Einfluss mehr auf die Inhalte einer fremden Webseite, die in einem iFrame präsentiert wird. Die Nutzung eines iFrames ist zwar keinesfalls verboten. Auf die _Möglichkeit_, dass fremde Seiten Tracking-Cookies setzen _könnten_, sollte jedoch hingewiesen werden.

■

8 iFrame steht für Inline Frame. Es wird ein Rahmen in eine Webseite – zum Beispiel die Moodle-Oberfläche – eingefügt, in die eine andere Webseite geladen werden kann.

![Image 555](index-535_1.jpg)

![Image 556](index-535_2.jpg)

**512** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.62** Der Link auf die H5P-Ressource wird in das Formularfenster im Moodle-Text-/HTML-Editor eingetragen.

**Bild 12.63** Moodle erzeugt intern ein kleines HTML-Skript. Die Klasse wird von der entsprechenden CSS-Formatierung benutzt.

![Image 557](index-536_1.jpg)

![Image 558](index-536_2.png)

12.5 Externe Tools (Auswahl)

**513**

**Bild 12.64** Im Editor erscheint nur ein Platzhalter, der auf einen gesetzten Link hinweist. Die Aufgabe wird erst in der Vorschau oder beim Ausführen sichtbar.

**Bild 12.65** Lernende finden nun in ihrem Fenster die Aufgabe, doch sie arbeiten über das Moodle-Fenster in einem fremden System!

![Image 559](index-537_1.png)

**514** 12 Ergänzende Lernhilfen für Moodle

**12.5.2.3■H5P-Aktivität in Moodle-Kursen**

Die Integration von Aufgaben aus fremden Systemen hat verschiedene Nachteile: Die Frage nach der Konformität zur Datenschutzgrundverordnung (DSGVO) wurde bereits angesprochen. Allerdings stellt sich auch die Frage nach der Verfügbarkeit. Auch H5P.org weist ausdrücklich darauf hin, dass die auf dieser Plattform erstellten Inhalte nicht grundsätzlich verfügbar sein werden (vgl. Bild 12.61). Es wird von Seiten der Plattformbetreiber zudem darauf hingewiesen, dass alle Inhalte grundsätzlich öffentlich sind und auch in anderen Lehrkonzepten nutzbar gemacht werden können. Wer seine Lehrinhalte mit einem Copy-right versehen und diese möglicherweise in kommerziellen Kursen anbieten möchte, für den ist die H5P-Plattform mit den aktuellen Strukturen die falsche Adresse.

Besser ist es deswegen, alle Inhalte in eigener Regie zu produzieren, was auch möglich ist.

Im Moodle Plugin Directory wird man fündig. Dort gibt es ein H5P-Plugin, das nicht nur eine neue Aktivität zur Kursgestaltung anbietet, sondern auch die Möglichkeit, die Inhalte direkt im Kurs zu erzeugen. Eine externe Anbindung zu H5P.org ist damit nicht erforderlich.

Es ist jedoch von der Moodle-Administration etwas Vorbereitung zu leisten: Zum einen muss das Plugin installiert und aktiviert werden (s. o.). Darüber hinaus sollten die Rollen in ihren Fähigkeiten noch einmal neu überdacht werden. Muss wirklich jede Trainer-Rolle H5P einsetzen dürfen? Es ist tatsächlich ein sehr leistungsfähiges Tool und in vielen Kursbereichen zweckmäßig.

H5P ist aber auch – wenn nicht sogar vor allem – für Lernende interessant, die selbstständig Inhalte entwickeln und gestalten wollen. Dies fördert die Motivation, steigert tatsächlich die Freude am Lernen, weil die eigene Kreativität an Bedeutung gewinnt und das Ergebnis durchaus Wertschätzung erfährt. Es birgt aber auch Risiken in sich, die allgemein durch die Möglichkeit, HTML-Inhalte editieren zu können, gegeben sind.

Es ist also auch Aufgabe der Administration unter Umständen weitere Trainer- und Student-Rollen anzulegen und ihnen die erforderlichen Fähigkeiten für die Erstellung von H5P-Content zuzuweisen.

**Bild 12.66** 

Ist das H5P-Plugin installiert, können

Aktivitäten direkt in den Kurs eingefügt

werden, ohne den Umweg über den

HTML-Editor und externe Quellen zu

beschreiten.

![Image 560](index-538_1.jpg)

![Image 561](index-538_2.jpg)

12.5 Externe Tools (Auswahl)

**515**

**Bild 12.67** Die Aktivität H5P – sie ist nur verfügbar, wenn das Plugin installiert wurde – kann nur dann genutzt werden, wenn die entsprechenden Fähigkeiten aktiviert wurden. Anderenfalls bleibt die Auswahl der Inhaltstypen leer.

**Bild 12.68** Nur wenn die Aktivität in einem Kursbereich hinzugefügt und die Erlaubnis, die Inhalts-bibliotheken zu nutzen, von der Administration erteilt wurde, können H5P-Inhalte in den Kurs eingefügt werden.

![Image 562](index-539_1.jpg)

**516** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.69** Sind die Fähigkeiten zur Installation der empfohlenen Bibliotheken vorhanden, können Inhaltstypen zur Gestaltung einer H5P-Aktivität gewählt werden (hier: Image Hotspots).

Am Beispiel eines _Image Hotspots_ soll die Verwendung einer eigenen H5P-Aktivität in einem Kursabschnitt vorgestellt werden. Wie bei jeder Aktivität werden mindestens zwei Pflichtfelder ausgefüllt: der Name der Aktivität und eine Beschreibung.

Die Aktivität _Image Hotspots_ benötigt zunächst ein Bild. Neben dem Upload werden hier auch zusätzlich Quellenangaben und Lizenzbedingungen vermerkt. Auch Moodle ist eine öffentliche Plattform und es ist das Urheberrecht zu beachten.

Das Bild sollte mehrere interessante Elemente enthalten, die es sich näher zu erklären lohnt. Die Erklärung dieser Hotspots erfolgt mithilfe kleiner Textblöcke, weiterer Erklär-Grafiken oder sogar mit Videosequenzen. Die Lernenden klicken auf den jeweiligen Hotspot und bekommen ihre Information dargeboten.

In der Lehre kann der Inhaltstyp _Image Hotspots_ auf verschiedene Weise verwendet werden:

**Reines Informationsmedium:** Die Lehrenden entwickeln ein Bild mit verschiedenen Elementen, die von den Lernenden zu erforschen sind. Dies dient der Wissensvermittlung. Wenn der Inhalt des Hintergrundbilds gut gewählt wird, können die Lernenden durchaus zusätzliche Informationen über die Zusammenhänge der Inhalte gewinnen.

**Eigene Projektarbeit:** Die Lernenden erarbeiten Texte, Illustrationen und Videosequenzen zu einem Themengebiet. Diese Elemente setzen sie als _Image Hotspots_ um und bieten diese anderen Mitlernenden als Lehrgangsunterlage an. Die Übung kann auch als Team-projekt gestaltet werden. Als Ergänzung der Arbeit lässt sich auch das Feedback der anderen Lernenden trainieren.

![Image 563](index-540_1.jpg)

![Image 564](index-540_2.jpg)

12.5 Externe Tools (Auswahl)

**517**

**Bild 12.70** Es wird die Aktivität „Image Hotspots“ im Kurs angelegt. In einem Bild werden verschiedene markante Punkte gesetzt, zu denen Erklärungen abgerufen werden können.

**Bild 12.71** Die verwendete Bilddatei unterliegt möglicherweise besonderen Lizenzbedingungen, zu den Metadaten des Bilds gehören deswegen Lizenzbedingungen und Quellenangaben.

![Image 565](index-541_1.jpg)

![Image 566](index-541_2.jpg)

**518** 12 Ergänzende Lernhilfen für Moodle

**Bild 12.72** Für jeden Hotspot wird ein eigener Informationsinhalt bereitgestellt. Dabei kann es sich um einen Text, ein weiteres Bild oder um ein Video handeln.

**Bild 12.73** Die Lernenden erhalten beim Klick auf einen Hotspot zusätzliche Informationen zum betreffenden Abschnitt.

![Image 567](index-542_1.png)

12.5 Externe Tools (Auswahl)

**519**

**Bild 12.74** In öffentlichen Publikationen ist die Angabe der Quelle und der Nutzungsrechte wichtig.

Auch Moodle-Kurse sind öffentliche Publikationen.

**Fragenkataloge**

**13 in Moodle**

Moodle ist eine Lernplattform, die auch für komplexe Lernzielkontrollen und sogar zur elektronischen Ablegung von Prüfungen verwendet werden kann. Hierzu wird ein Fragenkatalog benötigt, aus dem das Moodle-System die Prüfungsfragen entnehmen kann. Es ist wichtig, ausreichend viele Fragen mit verschiedenen Schwierigkeitsgraden zu definieren. In der Tat handelt es sich hierbei um eine zunächst zeitaufwendige Arbeit. Allerdings lohnt sich der Aufwand auf die lange Sicht aus verschiedenen Gründen:

Fragen können auch in künftigen Prüfungen verwendet werden.

Bei ausreichend vielen Fragen werden stets verschiedene Prüfungen durchgeführt.

Freitextaufgaben kompensieren Leseschwierigkeiten bei schlechten Handschriften der Lernenden.

Der Fragenkatalog fordert zwar einen hohen Startaufwand und regelmäßige Pflege, lässt sich aber auch sehr leicht erweitern, wodurch im Lauf der Zeit eine hochwertige und anspruchsvolle Fragensammlung entstehen kann. Hinzu kommt, dass bereits bestehende Fragenkataloge auch von Kolleginnen und Kollegen anpassbar und damit allgemein nutzbar sind. Wenn mehrere Lehrende Fragen ausarbeiten, entsteht eine sehr umfassende Sammlung, was wiederkehrende Fragen in verschiedenen Prüfungen unwahrscheinlich macht.

Um den Fragenkatalog anzulegen und dort Fragen zu erstellen oder zu verändern, sind Rechte der Teacher-Rolle erforderlich. Damit wird der Block _Kurs-Administration_ erreicht.

Lernende haben zu diesem Block keinen Zugang. Teacher ohne Autorenrechte sehen zwar den Block _Kurs-Administration_, können aber keine Fragen bearbeiten. Sie sehen in dem Block keinen Abschnitt _Fragen_.

**Zur Erinnerung**

Rollen sind in Moodle stets kontextbezogen! Das bedeutet, dass eine Person in einem Kurs eine Teacher-Rolle einnehmen kann, während sie in einem anderen Kurs möglicherweise lediglich als Teacher ohne Autorenrechte oder nur Student eingeschrieben ist. Entsprechend gestalten sich die Handlungsspielräume in den jeweiligen Kursen und Kursbereichen.

■

![Image 568](index-545_1.png)

**522** 13 Fragenkataloge in Moodle

**Bild 13.1** Nur mit den Rechten, Fragen zu erstellen und zu bearbeiten, ist dieser Menü-Teil in der _Kurs-Administration_ sichtbar.

**■**

**■ 13.1■Fragenkategorien**

Ein Fragenkatalog muss in der Praxis sehr umfangreich werden. Das hat verschiedene Gründe:

Die zu prüfenden Themengebiete weisen eine gewisse Komplexität auf und sollten um -

fassend berücksichtigt werden.

Prüfungsfragen sollten nicht von den Lernenden _vorhersehbar_ sein! Alleine unter dem Vorsatz, bei Wiederholungen und in kommenden Semestern stets eine neue Prüfung anzubieten, begründet sich die Anforderung eines sehr umfangreichen Fragenkatalogs.

Um dem Volumen eines solchen Fragenkatalogs eine gewisse Übersicht zu verleihen, werden die Fragen in Kategorien gegliedert. Das hat rein praktische Gründe: Zum Beispiel können Einschränkung der Nutzung auf einen Kurs festgelegt werden. Von besonderer Bedeutung ist allerdings eine Gewichtung der Schwierigkeitsstufen.

13.1 Fragenkategorien

**523**

**E-Learning ist kein Rationalisierungspotenzial!**

In Bezug auf Prüfungen und Lernzielkontrollen muss betont werden: Ja! Elektronische Prüfungen vereinfachen die Beurteilung der abgelieferten Arbeiten.

Es steckt jedoch sehr viel Anfangsarbeit in der Entwicklung elektronischer Lernzielkontrollen und Prüfungen. Dieser Aufwand sollte in der Zeitkalkulation für Kursvor- und Nachbearbeitungen entsprechend gewürdigt und bemessen

werden. Dies gilt auch, wenn ein erster Fragenpool bereits erstellt wurde, denn auch Fragen erfordern regelmäßige Pflege (Korrekturen, Ergänzungen).

Der Einsatz von E-Learning-Elementen dient also nicht der Kompensation

eines Lehrermangels und schon gar nicht der Rationalisierung im bestehenden System. Sinn ist es, die Qualität der Lehre zu verbessern und Lehrenden Zeit zu verschaffen, um genau dies zu erreichen.

■

**13.1.1■Anlegen einer Fragenklasse**

Kategorien sind hierarchisch gegliedert. Das bedeutet, dass eine Kategorie verschiedene Unterkategorien haben kann. Der Zugang und die Sichtweise der Kategorien sind allerdings stets auf einen Kontext bezogen. So werden Fragen grundsätzlich für einen Kurs angelegt.

Zugreifen können entsprechend nur die Rollen, die in diesem Kurs die entsprechenden Rechte besitzen.

**Lernende brauchen eine Sonderrolle!**

Lernende sehen in ihrem Kurs keinen Block „Kurs-Administration“. Sie haben keinen Zugriff auf Fragenkategorien oder Fragen. Soll jedoch die Entwicklung von Fragen als Kursprojekt vorgesehen werden, so bedarf dies der Definition einer besonderen Student-Rolle. Diese wird von der Moodle-Administration eingerichtet. Es empfiehlt sich zudem, die Fragen in einem eigenen Kurs ohne direkten Bezug zum Hauptkurs entwickeln zu lassen. So wird ausgeschlossen, dass tatsächliche Prüfungsfragen publik gemacht werden.

■

![Image 569](index-547_1.png)

![Image 570](index-547_2.jpg)

**524** 13 Fragenkataloge in Moodle

**Bild 13.2** Die Moodle-Administration sieht alle Kategorien im System. Mit diesen Rechten ist es möglich, Fragen über Kursgrenzen hinweg zu verschieben.

**Bild 13.3** Die Teacher-Rolle in einem Kurs sieht nur die Fragenkategorien des jeweiligen Kurses.

![Image 571](index-548_1.png)

13.1 Fragenkategorien

**525**

Die Anlage einer neuen Kategorie erfolgt im Block _Einstellungen_ unter _Kurs-Administration_ –

_Fragensammlung_. In diesem Fenster wählt man _Kategorien_. Im Abschnitt _Kategorie hinzufügen_ kann nun eine neue Fragenkategorie definiert und in die Hierarchie eingeordnet werden. Der Abschnitt muss unter Umständen „aufgeklappt“ werden.

Die Zuordnung zur Hierarchie ist die erste Aufgabe bei der Anlage einer neuen Kategorie.

Es ist zugleich die wichtigste Einstellung, um die dieser Kategorie zugewiesenen Fragen richtig in einem Test verwenden zu können. Der Name der Kategorie ist eine Pflichteingabe.

Er sollte aussagekräftig formuliert werden. Auch hier gilt es zu bedenken, dass die Fragensammlung sehr komplex und umfangreich werden kann. Für die Kategorie-Beschreibung steht das komplette HTML-Editor-Fenster zur Verfügung. Eine ID-Nummer kann frei gewählt werden und aus Buchstaben und Ziffern bestehen. Sie muss allerdings im System einmalig sein. Ihre Festlegung ist nicht zwingend erforderlich.

Für die Gestaltung der Hierarchie gibt es verschiedene Strategien, die Lehrende anhand ihres eigenen Kursprogramms bzw. Lehrplans festlegen. Ein Vorschlag wäre der folgende:

Oberste Kategorie-Ebene: Thema des Kurses

Erste Unter-Kategorie: Klassifizierung nach Schwierigkeitsgraden (leicht, mittel, schwer)

Zweite Unter-Kategorie: Einteilung nach Fragentypen

**Bild 13.4** Anlage einer neuen Kategorie. Der Name ist fachbezogen und wird direkt in die oberste Ebene der Kategorien dieses Kurses eingegliedert.

![Image 572](index-549_1.png)

**526** 13 Fragenkataloge in Moodle

**Bild 13.5** Die Fragenkategorien des Kurses können jederzeit bearbeitet und sowohl in ihrer Hierarchieebene als auch in der Reihenfolge verschoben werden.

**13.1.2■Klassifizierung von Schwierigkeitsgraden**

In einer elektronischen Prüfung können Fragen automatisch jeder Lernenden und jedem Lernenden individuell zugeordnet werden. Das bedeutet, dass alle Lernenden in einer gemeinsamen Prüfung jeweils eigene und voneinander unterschiedliche Fragen bearbeiten.

Das Risiko des berühmt-berüchtigten „Abschreibens“ ist damit deutlich geringer und es werden objektivere Testergebnisse erzielt.

Es gilt allerdings auch bei individualisierten Prüfungen der Grundsatz der Chancengleichheit! Es müssen deswegen die Fragen nach unterschiedlichen Schwierigkeitsgraden einge-teilt und entsprechend gewichtet werden.

Der erste Schritt zur Klassifizierung ist zunächst einmal die Einteilung in Kategorien. Es sollen drei Kategorien ausreichen:

**Leicht:** Hier werden Fragen eingeordnet, die ein selbstverständliches Minimalwissen prüfen. Ihnen werden in der Regel nur wenige Punkte zugewiesen. Dafür sollten die Fragen auch schnell zu beantworten sein, damit ausreichend Zeit für die Bearbeitung der anspruchsvolleren Fragen bleibt.

**Mittel:** Diese Fragenkategorie sei für das regulär zu prüfende durchschnittliche Wissen vorgeschlagen. In dieser Kategorie werden Fragen formuliert, die grundlegende Kenntnis und das Verständnis des vermittelten Lehrstoffs feststellen sollen. Die Einstufung in der Punktevergabe sollte deutlich über dem Niveau der leichten Fragen liegen.

**Experten:** Ein oder zwei Fragen sollten in einem Test die besonders engagierten Lernenden fordern, aber auch anerkennend belohnen. Die Fragen dürfen ein inhaltlich hohes Niveau haben, was sich auch in der Bewertung niederschlagen muss. Die Anzahl dieser

![Image 573](index-550_1.png)

13.2 Anlage einer neuen Frage

**527**

Fragen und die Zahl der erreichbaren Punkte sollte wohlüberlegt sein. Dominieren die

„Expertenaufgaben“ drücken sie möglicherweise das Ergebnis all derer, die „nur“ die einfachen und mittleren Fragen richtig beantwortet haben. Mit diesen Fragen sollte ein gutes Ergebnis möglich sein. Für ein „sehr gut“ darf gehobenes Wissen eingefordert werden.

**Bild 13.6** Struktur einer Kategorie in einem Fragenkatalog mit drei Unterkategorien für Fragen verschiedener Leistungsniveaus.

**■**

**■ 13.2■Anlage einer neuen Frage**

Mit der Anlage einer neuen Frage wird zunächst die Zuordnung zu einer der vorbereiteten Kategorien festgelegt (oberer umrandeter Bereich in Bild 13.7). Nach dem Klick auf den Button _Neue Frage erstellen_ wird zunächst ein Dialog geöffnet, in dem der Fragentyp (Abschnitt 13.3) zu wählen ist. Damit wird der jeweils zugehörige Fragendialog geöffnet.

In diesem Dialog wird jeder Frage ein Titel zugewiesen. Dies ist eine Pflichteingabe, die auch in der Auflistung der Fragen erscheinen wird. Selbstverständlich ist auch der Fragetext ein Pflichtfeld. Dieser wird entsprechend der Aufgabenstellung vom Lehrenden frei formuliert.

Grundsätzlich wird die Beantwortung einer Frage bewertet. So muss auch die Zahl der erreichbaren Punkte festgelegt werden. Eine eher leichte Aufgabe wird zweckmäßigerweise mit einer kleineren Punktzahl bewertet als die richtige Antwort auf eine anspruchsvolle Fragestellung. Grundsätzlich ist Feedback ein sehr wichtiges Instrument, um den Lernerfolg der Lernenden zu stärken. Feedback sollte sowohl für richtige als auch für falsche Antworten formuliert werden. Dabei ist es wichtig, auf die Aufgabenstellung und einen möglichen Fehler Bezug zu nehmen.

Es kann durchaus sinnvoll sein, eine (fehlerhaft beantwortete) Frage in mehreren Versuchen anzubieten. In diesem Fall können Punktabzüge festgelegt werden, deren Höhe abhängig von der Zahl der Versuche ist.

![Image 574](index-551_1.jpg)

![Image 575](index-551_2.jpg)

**528** 13 Fragenkataloge in Moodle

**Bild 13.7** Die Fragenkategorie sollte bereits mit der Erstellung der Frage festgelegt werden, um die Übersicht zu bewahren.

**Bild 13.8** Die neu zu formulierende Frage entspricht einem der in Moodle definierten Fragentypen.

Nach dieser Auswahl erscheint der folgende Dialog mit unterschiedlichen Feldern und Parametern.

13.3 Fragetypen und Syntax

**529**

**■**

**■ 13.3■Fragetypen und Syntax**

Mit der Anlage einer neuen Aufgabe gehört neben der Einordnung in eine Kategorie auch die Wahl des Fragetyps zu den Grundeinstellungen. Anders als bei den sechs Kontrollfragen einer Lektion gibt es für die Entwicklung eines Fragenkatalogs für die Aktivität _Test_ weitaus umfassendere Möglichkeiten:

Multiple Choice

Wahr/Falsch

Zuordnung

Kurzantwort

Numerisch

Freitext

Berechnet

Berechnete Multiple Choice Aufgabe

Drag and Drop auf ein Bild

Drag and Drop auf einen Text

Drag and Drop auf Markierungen

Einfach berechnet

Lückentext

Lückentextauswahl

Zufällige Kurzantwort-Zuordnung

Bei sehr umfangreichen Fragenkatalogen ist es zu empfehlen, für jeden verwendeten Fragentypus in jeder Schwierigkeitsstufe eine eigene Unterkategorie zu definieren. Wird diese Struktur von Anfang an organisatorisch umgesetzt, ist das Management des Fragenkatalogs und die spätere Erstellung von Tests sehr einfach durchführbar.

**13.3.1■Multiple Choice**

Eine Multiple Choice-Frage kann verschiedene Antwortmöglichkeiten bieten. In Betracht kommen:

Eine Antwort ist richtig.

Mehrere Antworten sind richtig.

Alle Antworten sind richtig.

Mit der Wahl des Fragetyps „Multiple Choice“ kann eine Vorgabe auf nur eine mögliche Antwort festgelegt werden. Dies hat Auswirkungen auf die Bewertung der Antworten. Bei nur einer möglichen Antwort muss diese Antwort mit 100 % bewertet werden. Sind mehrere Antworten richtig, so kann bestimmt werden, welche Anteile an der Gesamtpunktzahl eine richtige Antwort haben soll. Die insgesamt vergebene Wertung muss 100 % betragen. Liegt die Summe der positiven Bewertung unter oder über 100 %, meldet sich Moodle mit einem Fehler.

**530** 13 Fragenkataloge in Moodle

**Richtige Fragen durch positive Bewertung**

Eine besondere Kennzeichnung der richtigen Fragen findet nicht statt. Was richtig ist, bekommt einen positiven prozentualen Anteil an den zu vergebenden Punkten.

■

Ebenso lassen sich Wertungen für falsche Antworten vorgeben. Hier dürfen allerdings Wer-tungsabzüge von mehr als 100 % vergeben werden. Im Beispiel wird jede falsche Antwort mit –100 % bewertet. Das verhindert „erfolgreiches Raten“. Eine falsche Antwort führt dazu, dass keine Punkte für diese Frage vergeben werden.

Werden mehrere Antwortversuche bei fehlerhaften Lösungen eingeräumt, so kann hier eine Verringerung der erreichbaren Punkte festgelegt werden. Damit wird vermieden, dass Kandidaten die Fragen ohne Abzüge so oft durchspielen bis sie das gewünschte Ergebnis erreicht haben.

Zu jeder möglichen Antwort kann (und sollte) ein direktes Feedback formuliert werden. Die Kandidaten erhalten so eine Begründung, warum eine Antwort richtig oder falsch ist.

Zusätzlich kann ein Gesamtfeedback gegeben werden, das sich auf die Fragestellung allgemein bezieht. Es können Texte für folgende allgemeine Fälle vorbereitet werden:

Feedback bei vollständig richtigen Antworten.

Feedback bei unvollständig (teilweise richtig) beantworteter Frage.

Feedback bei falscher Lösung.

Unabhängig von der Richtigkeit der Antworten kann auch ein direktes Feedback formuliert werden, was unmittelbar nach der Abgabe ausgegeben wird. Es sollte allerdings, wenn ein solches allgemeines Feedback vorgesehen ist, nicht mit einem zu langen Text formuliert werden. Wird die Frage in einer Prüfung eingesetzt, deren Bearbeitungszeit begrenzt ist, hemmt das die Bearbeitung der gesamten Prüfung.

![Image 576](index-554_1.png)

![Image 577](index-554_2.jpg)

13.3 Fragetypen und Syntax

**531**

**Bild 13.9** Am Beginn jeder Fragestellung steht deren Formulierung.

**Bild 13.10** Ein allgemeines Feedback kann in Übungsfragen wertvolle Hinweise enthalten. Es wird direkt nach der Abgabe gesendet, unabhängig davon, welches Ergebnis die Antworten bringen.

![Image 578](index-555_1.jpg)

![Image 579](index-555_2.jpg)

**532** 13 Fragenkataloge in Moodle

**Bild 13.11** Richtige Antworten werden mit einer positiven Bewertung markiert. Falsche Antworten erhalten eine negative Bewertung. –100 % verhindern, dass ein Kandidat durch pures Raten oder Markierung aller Antworten Punkte gewinnen kann.

**Bild 13.12** Ein kombiniertes Feedback bewertet das Gesamtergebnis der Antworten.

![Image 580](index-556_1.jpg)

![Image 581](index-556_2.png)

13.3 Fragetypen und Syntax

**533**

**Bild 13.13** Mehrfache Versuche sollten mit reduzierten Punkten bewertet werden. Die maximale Punktzahl kann also bei dieser Frage nur beim ersten Versuch erreicht werden.

**Bild 13.14** In der Vorschau können Lehrende die Aufgabe testen. Lernende sehen ein ähnliches Bild.

![Image 582](index-557_1.jpg)

**534** 13 Fragenkataloge in Moodle

**13.3.2■Wahr/Falsch**

Bei der Wahr/Falsch-Frage wird eine Behauptung aufgestellt. Die Kandidaten entscheiden lediglich, ob diese Behauptung stimmt oder nicht. Es wird mit der Definition der Frage festgelegt, ob die Aussage wahr oder falsch ist. Die Feedbackfelder für beide Fälle sind vorgegeben.

**Parallelen in den Definitionen der Fragen**

Jede Frage ist verbal zu formulieren und benötigt eine Überschrift. Dies haben alle Fragen gemeinsam. Auch ist jeder Frage eine gewisse Zahl an Punkten zuzuweisen und es sollte Feedback zu den Antworten gegeben werden. Auf

diese Details wurde im Zusammenhang mit dem Fragetyp _Multiple Choice_ eingegangen. Diese Felder werden deswegen nicht speziell illustriert.

■

**Bild 13.15** Es wird Feedback für die Wahl von Wahr oder Falsch formuliert. Ob die Behauptung wirklich richtig ist, wird in der positiven Bewertung der Antwort bestimmt.

![Image 583](index-558_1.jpg)

![Image 584](index-558_2.jpg)

13.3 Fragetypen und Syntax

**535**

**Bild 13.16** Die Aufgabe in der Vorschau für die Lehrenden dient der Simulation und der Fehlerkorrektur. Die Fragestellung in der Kandidatensicht hat weniger Schaltflächen.

**13.3.3■Zuordnung**

Bei einer _Zuordnungsfrage_ werden mehrere Begriffe oder Behauptungen formuliert und dazu passend ein Begriff oder eine Erklärung. Es müssen mindestens zwei Paare vollständig angelegt werden. Fragen bzw. die Behauptungen müssen zudem grundsätzlich auch einen Antwortteil besitzen. Anders sieht es bei den Antwortblöcken aus. Hier können durchaus Begriffe eingetragen werden, obwohl das Fragenfeld leer bleibt. Diese Elemente sind dann natürlich nicht zuzuordnen, was jedoch den Schwierigkeitsgrad steigert.

**Bild 13.17** Es hat durchaus einen Grund, warum in Frage 3 nur ein Antwort-Element eingetragen wird. Dieses Element ist nicht zuzuordnen und steigert den Schwierigkeitsgrad der Aufgabe.

![Image 585](index-559_1.png)

**536** 13 Fragenkataloge in Moodle

**Bild 13.18** Aufgabe der Zuordnungsfrage ist es, zum gefragten Begriff die richtige Antwort zu wählen.

**13.3.4■Kurzantwort**

Die _Kurzantwort_ ist im Grunde ein sehr einfacher Fragetypus. Es werden wie üblich eine Frage und ein Fragentitel formuliert und es wird die Anzahl der erreichbaren Punkte festgelegt. Die Kandidaten antworten jedoch mit einem frei eingegebenen Begriff und das stellt die Lehrenden vor eine Herausforderung: Soll die Rechtschreibung tatsächlich ein KO-Kriterium sein?

Lehrende müssen sich nicht um die Problematik der Groß- und Kleinschreibung kümmern.

Hier wird die Entscheidung bei der Definition der Frage getroffen, ob Groß- und Kleinschreibung zu beachten ist oder nicht. Im Sprachunterricht spielt dies gewiss eine wichtige Rolle.

Kommt es jedoch vor allem auf die fachlich-inhaltlich richtige Antwort an, kann man hier tolerant sein.

Der Fragetypus Kurzantwort lässt es darüber hinaus zu, verschiedene mögliche Antworten zu akzeptieren. So kann jede mögliche Schreibweise, die aus fachlicher Sichtweise als richtig zu bewerten ist, in ein Antwortfeld geschrieben werden.

**Ein Beispiel:**

Die Fragestellung lautet: _Wie heißt das Lernmanagement-System, mit dem Sie hier arbeiten?_

Die erste mögliche Antwort ist natürlich: _Moodle_! Selbstverständlich sollte in diesem Fall die Groß- und Kleinschreibung keine Rolle spielen und deswegen wird diese Einstellung auf _unwichtig_ gesetzt. Moodle akzeptiert also – obwohl nur ein Antwortfeld ausgefüllt ist – auch die Antworten _MOODLE_ oder _moodle_.

Richtig ist es natürlich auch, die Abkürzung (die Moodle ja ist) auszuschreiben. In einem weiteren Antwortfeld wird deswegen der folgende Text eingetragen: _Modular Object Oriented Dynamic Learning Environment_.

Beide Antwortmöglichkeiten – die Kandidaten geben schließlich nur eine Antwort in ihr Textfeld ab – werden in diesem Fall mit 100 % bewertet, bringen also die volle Punktzahl!

![Image 586](index-560_1.png)

13.3 Fragetypen und Syntax

**537**

Wie sieht es nun jedoch aus, wenn die Antwort einen kleinen Flüchtigkeitsfehler enthält und ein Kandidat den folgenden Lösungsvorschlag in das Textfeld einträgt: _Modular Object Oriented **Digital** Learning Environment_

Das ist eine durchaus gängige Interpretation der Abkürzung Moodle. Es gibt auch in anderen Bereichen mögliche Irrtümer, die zumindest unter der Vergabe von Teilpunkten akzeptiert werden. In einer mündlichen oder schriftlichen Prüfung, die jeweils von Menschen (und nicht einem Algorithmus) bewertet werden, ist das die Regel. Computer kennen das Wort „Kulanz“ nicht. Diese Kulanz kann durch geeignete Formulierung auch teilweise richtiger Lösungen1 mit der Festlegung geringerer Prozentsätze für die Punktevergabe in einer Kurzantwort-Frage umgesetzt werden.

**Bild 13.19** Zwei Antworten sind als richtig zu bewerten. In Antwort 3 wird deutlich: Ein Kandidat hat die Frage verstanden und kennt sich grundsätzlich auch aus, jedoch ist ein kleiner Fehler unter-laufen. Das Feedback zeigt in Fettschrift die korrekte Schreibweise und es werden nur 50 % der erreichbaren Punkte gegeben.

1 Kandidaten werden eine unberücksichtigte, jedoch möglicherweise teilweise richtige Antwort bei ihren Lehrenden reklamieren. Dies ist eine gute Gelegenheit, die möglichen Antworten im Fragenkatalog zu erweitern. Im Lauf der Zeit deckt die Frage auf diese Weise alle möglichen Flüchtigkeitsfehler ab.

![Image 587](index-561_1.png)

![Image 588](index-561_2.png)

**538** 13 Fragenkataloge in Moodle

**Bild 13.20** Eine richtige Antwort, die auch die volle Punktzahl bringt. Es gibt jedoch noch eine andere Alternative, auf die im (selbst vom Lehrenden) formulierten Feedback hingewiesen wird.

**Bild 13.21** Es heißt nicht „Digital“ Learning . . ., sondern „Dynamic“ Learning . . . Der Ansatz war jedoch vollkommen richtig. Soll dem Kandidaten deswegen kein Punkt gegeben werden? In der Fragendefinition kann auch diese Antwort als richtig vorgesehen werden, jedoch wird ihr eine geringere Gewichtung bei der Punktvergabe zugewiesen.

13.3 Fragetypen und Syntax

**539**

**13.3.5■Numerisch**

Beim _numerischen_ Fragentypus wird natürlich eine numerische Antwort erwartet. Allerdings kann diese Antwort sehr flexibel gestaltet werden. So lassen sich Einheiten und deren Teiler bzw. Vielfache berücksichtigen. Tückisch bei numerischen Aufgaben, die möglicherweise mehrere Rechenschritte erfordern, sind Rundungsfehler. Es sollte zwar in einer Aufgabenstellung klar kommuniziert werden, nach welchen Regeln und wo zu runden ist, trotzdem können verschiedene mögliche Rechenwege zu Abweichungen führen.

Wird eine Maßeinheit für das Ergebnis vorgegeben, dann kann ein Faktor für einen Punktabzug festgelegt werden, der greift, wenn die Einheit vergessen wird. Die Einheit ist natürlich kein numerischer Wert, sondern in der Regel aus Textzeichen bestimmt. Diese Zeichen sind frei wählbar und müssen eingestellt werden. Mit der Festlegung der Fragestellung muss vorgegeben werden, ob die Einheit links oder rechts vom Betrag zu setzen ist. Besonders bei Währungen sind hier verschiedene Varianten möglich. Diese sind in jedem Fall in der Fragestellung zu benennen, wenn die Lernenden internationalem Ursprungs sind.

**Internationale Schreibweisen bei numerischen Fragen**

Beispielsweise bei Währungen gibt es im internationalen Raum aber auch

national aus reiner „Gewohnheit“ verschiedene Varianten in der Schreibweise: Die Einheiten können vor oder nach dem Betrag geschrieben werden. Für

Moodle macht das tatsächlich einen Unterschied! Die Eingabe der Lösungen muss also in der von den Lehrenden festgelegten Schreibweise erfolgen.

Sonst führt das zu einem falschen Ergebnis.

■

In der Definition der Fragen erfolgt die Deklaration der Einheiten separat vom Wert des Betrags. In den Antworten wird also lediglich ein reiner Zahlenwert eingetragen. Buchstaben und andere Zeichen werden von Moodle nicht akzeptiert! Die Einheiten müssen in einem speziellen Abschnitt festgelegt werden. Es werden verschiedene Buchstaben oder Buchstabenketten als Maßeinheiten definiert.

Bei der Eingabe der Lösung ist es nicht entscheidend, ob ein (oder auch mehrere) Leerzeichen zwischen dem Betrag und der Maßeinheit vorhanden sind. Sehr wohl wird jedoch die Groß- und Kleinschreibung unterschieden. Diese muss absolut korrekt sein, damit die Lösung als richtig erkannt werden kann. Der Versuch, für die Einheit zwei Schreibweisen in Groß- und in Kleinschreibung mit dem jeweils gleichen Faktor zu deklarieren, schlug fehl!

Moodle meldet einen Datenbankfehler, der das Schreiben der Fragendeklaration in die Sys-temdatenbank unmöglich macht.

**Groß- und Kleinschreibung ist zu beachten!**

Bei der Eingabe von Maßeinheiten kann keine Toleranz von Groß- und Kleinschreibung gewährt werden. Das ist auch sinnvoll, denn es gibt beispielsweise einen Unterschied zwischen MV (1 000 000 V) und mV (0,001 V).

■

![Image 589](index-563_1.jpg)

![Image 590](index-563_2.jpg)

**540** 13 Fragenkataloge in Moodle

**Bild 13.22** Zwei richtige (numerische) Antworten werden festgelegt: Die erste Antwort gibt ein Feedback bei absoluter Richtigkeit, die zweite Antwort lässt eine Toleranz von 0,0001 zu. Die Einheiten werden hier noch nicht berücksichtigt.

**Bild 13.23** Eine fehlende oder falsche Maßeinheit führt hier zu 10 % Punktabzug. Es wird zudem festgelegt, mit welchen Maßeinheiten und welchen Faktoren zu arbeiten ist.

![Image 591](index-564_1.jpg)

![Image 592](index-564_2.png)

![Image 593](index-564_3.png)

13.3 Fragetypen und Syntax

**541**

**Bild 13.24** Es wurde versucht, zwei Varianten der Maßeinheit einmal in Groß- und einmal in Kleinschreibung mit dem gleichen Faktor zu deklarieren. Dies wird vom System nicht akzeptiert.

**Bild 13.25** Eine exakte Antwort! Sie stimmt auf das Hundertstel Millivolt genau. Es wird kein Toleranzfall aktiviert.

**Bild 13.26** Die eingegebene Lösung weicht um 0,05 mV von der richtigen Lösung ab. Das liegt innerhalb der eingestellten Toleranz von 0,1 mV und wird deswegen als richtig interpretiert.

![Image 594](index-565_1.png)

**542** 13 Fragenkataloge in Moodle

**Bild 13.27** Der Zahlenwert ist absolut richtig, aber es fehlt die Maßeinheit im Ergebnis. Deswegen wird ein Punktabzug von (hier) 10 % vorgenommen.

**13.3.6■Freitext**

In vielen Prüfungen werden Freitext-Fragen eingesetzt. Tatsächlich gibt es unter Lehrenden die Frage nach der Rechtfertigung des damit verbundenen Aufwands, eine IT-Infrastruktur für eine Prüfung einzusetzen, die ebenso mit Füllfeder oder Kugelschreiber auf Papier absolviert werden kann. Eine automatische Bewertung ist nicht möglich und ein Gesamtfeedback geht nicht individuell auf die Lösung ein. Eine Bewertung ist also grundsätzlich manuell vorzunehmen. Dies rechtfertigt noch nicht, Freitextaufgaben elektronisch zu präsentieren, denn auch die Bewertung auf Papier gelieferter Lösungen kann in das System manuell eingetragen werden.

Wer einmal die auf Papier unter Stress geschriebenen Freitext-Lösungen eines größeren Klassenverbands korrigieren und bewerten musste, wird dagegen den Wert der Freitextaufgaben in Moodle zu schätzen wissen: Es gibt dort keine unlesbare Handschrift. Natürlich könnte man die Regel anwenden, dass unlesbare Lösungen als falsch zu bewerten sind, doch bewertet man damit lediglich eine formale Schwäche des Lernenden. Das kann nicht das Ziel einer Prüfung sein, die das Beherrschen des Fachwissens feststellen soll.

Die Definition der Frage erfolgt wie bei den Typen zuvor. Mit der Wahl des Fragetypus wird zudem bereits das erforderliche Eingabefeld vorgegeben, welches in der Prüfung erscheint.

Dieses kann allerdings in der Größe verändert werden. In dieses Feld erfolgt die Verfassung der Lösung. Zudem kann ein Dateiupload erlaubt werden.

Es gibt weitere Felder in der Fragendeklaration: Das klassische „Allgemeine Feedback“

kann mit der Abgabe gegeben werden. Viel interessanter ist aber sicher die _Antwortvorlage_.

In dieses Feld können Hinweise und Vorgaben zur Formulierung der Antwort eingetragen werden. Diese erscheinen im Antwortfenster.

![Image 595](index-566_1.jpg)

![Image 596](index-566_2.jpg)

13.3 Fragetypen und Syntax

**543**

**Bild 13.28** Ein allgemeines Feedback sollte bei einer Freitextaufgabe formuliert werden. Kandidaten erhalten unmittelbar nach der Abgabe noch kein Ergebnis. Aus Hinweisen zur richtigen Lösung können die Kandidaten ihre eigene Leistung selbst abschätzen und grob bewerten.

**Bild 13.29** Fehlt die Antwortvorlage, bleibt das Eingabefeld leer. Ansonsten kann man den Kandidaten Lösungshinweise oder Teilüberschriften für die zu bearbeitenden Themen anbieten.

![Image 597](index-567_1.png)

**544** 13 Fragenkataloge in Moodle

**Bild 13.30** Diese Aufgabe sieht eine reine Freitextaufgabe vor. Die Beilage einer Datei ist nicht möglich.

**13.3.7■Berechnet**

Moodle bietet mit dem Fragentypus „Berechnet“ eine sehr dynamische Fragemethode an, die ideal in der Mathematik, im naturwissenschaftlichen oder im wirtschaftswissenschaft-lichen Unterricht genutzt werden kann. Die Kandidaten müssen die Aufgaben berechnen und das numerische Ergebnis in das Lösungsfeld eintragen. Anders als es bei den voran-gegangenen Beispielen zu sehen war, findet die Anlage einer berechneten Frage in mehreren Schritten statt:

Erster Schritt: Formulierung der Frage, Beschreibung der Antwort-Formel und Festlegung der erreichbaren Punktzahl. Ähnlich wie bei einer numerischen Frage kann auch die Verwendung von Maßeinheiten in verschiedenen Teiler- oder Vielfachstufen gefordert werden.

Zweiter Schritt: Wahl der Datensatzbereiche und Synchronisation mit anderen Fragen.

Dritter Schritt: Erstellung und Bearbeitung von Datensätzen für die Belegung der Platzhalter.

Damit Moodle die Berechnung aus variablen Werten selbst durchführen und bei jedem Versuch gewissermaßen eine neue Aufgabe generieren kann, ist eine besondere Syntax erforderlich.

Dies beginnt mit der Deklaration der Variablen. Eine Variable kann aus nahezu beliebigen Zeichenketten gebildet werden. Wichtig ist, dass eine Variable keine Leerzeichen enthalten darf. Sonst wird Moodle mit einer Fehlermeldung reagieren, wenn der zweite Schritt aufgerufen werden soll.

13.3 Fragetypen und Syntax

**545**

Variable Größen – in Moodle werden diese als Ersatzzeichen bezeichnet – werden in einer geschweiften Klammer eingefasst.

**Richtige Schreibweisen einer Variablen (Ersatzgröße) sind:**

{x}

{Rechenwert}

{VariableX}

**Falsch wäre dagegen diese Schreibweise:**

x

{Variable x}

Im ersten Fall fehlen die geschweiften Klammern und im zweiten Beispiel enthält der Name der Variablen ein Leerzeichen.

**Wichtig**

Diese Variablen bzw. Ersatzzeichen werden sowohl in der Aufgabenstellung als auch in der Lösungsformel verwendet!

■

Ein Beispiel soll die Verwendung von Ersatzzeichen bzw. Variablen zeigen. Zuerst wird die Aufgabe im _Fragetext_ formuliert. Es soll die elektrische Leistung (P in Watt) errechnet werden, die bei bekanntem Spannungsabfall (U) und bekanntem Stromfluss (I) in einem Widerstand umgesetzt wird. Die Formulierung des Fragetextes lautet also:

Berechnen Sie die in einem Widerstand umgesetzte elektrische Leistung!

* Der Spannungsabfall ist U = **{U}** V

* Es fließt ein Strom I = **{I}** A

Obwohl in der Lösung die Eingabe der Maßeinheiten erwartet wird, sind in den Variablen nur rein numerische Werte ohne Einheiten gespeichert. Die Einheiten müssen also als Text nach dem Platzhalter ergänzt werden.

Bei einer berechneten Aufgabe wird in den meisten Fällen nur eine einzige Antwort benötigt. Allerdings gibt es hier auch Ausnahmen. Man denke nur an die Lösung einer gemischt quadratischen Gleichung, bei der zwei Lösungen möglich sind. In diesem Fall muss neben dem angebotenen Antwortfeld ein weiteres Feld eröffnet werden. Beide Felder sind dann entsprechend zu bewerten:

Bei Aufgaben, wo _entweder_ die erste _oder_ die zweite Lösung richtig ist, werden beide Antworten mit 100 % bewertet.

Im Beispiel der gemischt quadratischen Gleichung sind zwei Lösungen richtig. Das bedeutet aber auch, dass zum Erreichen der vollen Punktzahl beide Lösungen zu berechnen sind. Jede Antwort wird also mit jeweils 50 % bewertet.

**546** 13 Fragenkataloge in Moodle

**Mehrere Antworten sind möglich!**

Sind in einer berechneten Aufgabe mehr als eine Antwort möglich oder ergibt die Berechnung per mathematischem Gesetz mehrere Lösungen, so können

weitere Antwortfelder in der Fragendefinition hinzugefügt werden. Es muss jedoch möglich sein, insgesamt 100 % zu erreichen. Können keine 100 %

erreicht werden, wird Moodle die Aufgabenstellung nicht akzeptieren.

■

Wenn nicht gerade einfache Grundrechnungen mit ganzen Zahlen durchgeführt werden, wird man zwangsweise mit dem Problem der Rundungsfehler zu tun haben. Das ist besonders dann der Fall, wenn komplexe Aufgaben zu lösen sind, deren Berechnung mehrere Zwischenschritte erfordern. Damit ein Ergebnis auch bei durch Rundung begründeten Abweichungen als richtig erkannt werden kann, ist es wichtig, einen Toleranzbereich festzulegen. Moodle sieht hier drei mögliche Varianten vor, um eine Toleranz zu definieren:

Relativ

Nominell

Geometrisch

In den meisten Fällen wird die _relative Toleranz_ ausreichend sein. Die Aufgabe ist richtig, wenn die Abweichung kleiner oder gleich dem eingetragenen Wert ist.

_Absolute Abweichung_ £ _eingetrageneToleranz_

Bei der _nominellen Toleranz_ berücksichtigt man ein sehr breites Ergebnisspektrum von sehr kleinen bis hin zu sehr großen Werten. Beispielsweise gerät die relative Toleranz an ihre Grenzen, wenn die Ergebnisse von einem sehr kleinen Bereich (deutlich unter 1) bis zu einem sehr großen Bereich (mehrere Hunderter- oder Tausenderstellen) variieren können.

Im letzteren Fall ist eine relative Toleranz von einem Hundertstel völlig sinnlos. Anders die nominelle Toleranz. Die Antwort wird als richtig gewertet, wenn das Verhältnis der Abweichung zum Betrag der tatsächlichen Lösung kleiner oder gleich der vorgegebenen Toleranz ist.

_Absolute Abweichung_ ≤ _eingetrageneToleranz_

_Lösungswert_

Bei der _geometrischen Toleranz_ wird ebenfalls mit Verhältnissen gearbeitet und damit die Bandbreite der möglichen Lösungen berücksichtigt. Hier werden jedoch zusätzlich alle Parameter quadriert.

_Absolute Abweichung_ 2 _eingetrageneToleranz_ 2

≤

_Lösungswert_ 2

![Image 598](index-570_1.png)

13.3 Fragetypen und Syntax

**547**

**Bild 13.31** In der Aufgabenstellung werden bereits Platzhalter verwendet. Diese werden von Moodle mit den Inhalten gefüllt, die für die Berechnung des Ergebnisses verwendet werden.

![Image 599](index-571_1.png)

**548** 13 Fragenkataloge in Moodle

**Bild 13.32** Jede mögliche Antwort wird aus einer Berechnungsformel ermittelt. Es sind Regeln der speziellen Syntax zu beachten.

Die Formulierung der Antwortformel setzt neben der richtigen Schreibweise der Variablen auch die Kenntnis einer besonderen Syntax voraus. Dabei ist die Schreibweise einfacher Grundrechenarten unkritisch: +, –, * und / sind hierfür bekannte Schreibweisen, die allgemein verwendet werden.

**Kein Gleichheitszeichen!**

Für die Antwortformeln in einer berechneten Frage wird _kein Gleichheitszeichen_ verwendet. Doch Achtung: In der nachfolgend beschriebenen _berechneten_ _Multiple Choice-Frage_ ist das anders geregelt!

■

Komplizierter wird es jedoch, wenn mit Potenzen zu arbeiten ist.

**Falsch ist: {x}^2** – diese Schreibweise ist zwar allgemein durchaus geläufig für die Potenz x2, kann jedoch in Moodle nicht verwendet werden! Hier muss tatsächlich – und das mit einem deutlichen mathematischen Umweg – mit einer Funktion gearbeitet werden: **exp(2*log({x}))** – diese Schreibweise ist in einer berechneten Aufgabenstellung richtig!

Ebenso richtig ist die Schreibweise **pow({x},2)**.

Auch wenn es in vereinzelten Fällen sehr kompliziert erscheint, können mithilfe der definierten Funktionen sehr komplexe Berechnungen programmiert werden.

13.3 Fragetypen und Syntax

**549**

**Funktionsschreibweise**

Alle Argumente der Funktionen werden in runde Klammern eingefasst! Die

Schreibweise der Variablen ändert sich dabei nicht. Eine Variable bzw. ein Ersatzzeichen wird stets in geschweiften Klammern dargestellt, welche Teil des Ersatzzeichens sind. Dies bleibt auch bei einer Verwendung innerhalb von Funktionen so.

■

**Tabelle 13.1** Funktionen für Antwortformeln in berechneten Fragetypen Funktion

Bedeutung

abs()

Absoluter Betrag (Ergebnis ist der Zahlenwert ohne Vorzeichen)

acos()

Arkus-Cosinus – „Umkehrfunktion“ des Cosinus

acosh()

Area-Cosinus Hyperbolicus: acos( _x_) = ln _x_ + _x_ 2 −

(

)1

asin()

Arkus-Sinus – „Umkehrfunktion“ des Sinus

asinh()

Area-Sinus Hyperbolicus: asin( _x_) = ln _x_ + _x_ 2 +

(

)1

atan2()

Es werden die kartesischen Koordinaten x, y als Argument übergeben. Das Ergebnis ist der Winkel im richtigen Quadranten.

atan()

Arkus-Tangens – „Umkehrfunktion“ des Tangens

atanh()

1

1



Area-Tangens Hyperbolicus: atanh( _x_)

+

= ⋅ _ln_

_x_

2

1− _x_ 

bindec()

Umrechnung einer Binärzahl in eine Dezimalzahl

cell()

Aufrunden

cos()

Kosinus

cosh()

Kosinus Hyperbolicus:

1

cosh _x_

( _ex e_− _x_

( )= ⋅

+

)

2

decbin()

Umrechnung einer Dezimalzahl in eine Binär- bzw. Dualzahl

decoct()

Umrechnung einer Dezimalzahl in eine Oktalzahl

deg2rad()

Umrechnung der Winkel von Grad (Degree) in Radiant

exp()

Exponentialfunktion nach dem folgenden Schema: _xn_ = exp _n_

( ⋅log( _x_))

expm1()

_expm x_

_ex_

1

1

( )= −

floor()

Abrunden

fmod()

Modulo: Es werden Dividend und Divisor als Argumente übergeben. Das Ergebnis ist der Rest der Division.

is_finite()

Das Ergebnis ist „1“, wenn das Argument endlich ist. Ansonsten ist das Ergebnis „0“

is_infinite() Das Ergebnis ist „1“, wenn das Argument unendlich ist. Ansonsten ist das Ergebnis

„0“

_(Fortsetzung nächste Seite)_

**550** 13 Fragenkataloge in Moodle

**Tabelle 13.1** Funktionen für Antwortformeln in berechneten Fragetypen _(Fortsetzung)_ Funktion

Bedeutung

is_nan()

Das Ergebnis ist „1“, wenn das Argument keine Zahl (Not a Number) ist.

log10()

Logarithmus zur Basis 10

log1p()

Log(x+1)

log()

Natürlicher Logarithmus zur Basis e – bitte Schreibweise beachten: _nicht_ ln!

max()

Maximalwert der als Argument übergebenen Zahlenwerte

min()

Minimalwert der als Argument übergebenen Zahlenwerte

octdec()

Umrechnung einer Oktal- in eine Dezimalzahl

pi()

Die Zahl Pi ( _p_) als Wert

pow()

Berechnung einer Potenz, wobei als Argumente durch Komma getrennt die Basis und der Exponent übergeben werden.

rad2deg()

Umrechnung eines Winkels von Radiant in Grad (Degree)

round()

Rundung einer Gleitkommazahl

sin()

Sinus

sinh()

1

Sinus-Hyperbolicus: sinh _x_

( _ex e_− _x_

( )= ⋅

−

)

2

sqrt()

Quadratwurzel

tan()

Tangens

**Parameter für verschiedene Funktionen der Trigonometrie**

Die Argumente der trigonometrischen Funktionen müssen als Radiant (nicht in Grad) deklariert werden!

■

Auch in einer berechneten Frage können bei der Eingabe des Ergebnisses Maßeinheiten inkl. der üblichen Teiler und Vielfachen verwendet werden. Es gilt auch hier, den Unterschied zwischen Groß- und Kleinschreibung zu beachten. Außerdem müssen die richtigen Faktoren vorgegeben werden, anhand derer Moodle die Werte entsprechend umrechnen kann.

Die reine Einheit wird immer mit dem Faktor 1 dargestellt. Im Beispiel wird eine elektrische Leistung in Watt als Lösung gefragt. Die Einheit ist also W. Will jemand die Antwort in Milli-Watt (mW) schreiben, was einem Tausendstel Watt entspricht, dann braucht dies den Faktor 1000, um mit der Ursprungseinheit kompatibel zu sein. Der einzugebende Faktor für mW ist deswegen 1000, denn 1000 mW sind gleich 1 W.

Ähnlich sieht es bei den Vielfachen aus. Um den Wert 1 Kilo-Watt (kW) in die Ausgangsein-heit Watt umzurechnen, muss der Faktor 0,001 eingestellt werden.

Auch bei den berechneten Aufgaben gilt, dass eine fehlende Einheit zu einem Punktabzug führt, dessen Höhe mit der Erstellung der Frage festgelegt wird.

![Image 600](index-574_1.jpg)

![Image 601](index-574_2.jpg)

13.3 Fragetypen und Syntax

**551**

**Bild 13.33** Die geforderten Maßeinheiten werden so festgelegt, wie es bereits beim numerischen Fragetypus zu sehen war.

**Bild 13.34** Sollen die Zahlenwerte der Platzhalter auch für weitere Aufgaben in einem Test verwendet werden, die einen Bezug zu dieser Berechnungsaufgabe haben, ist die Synchronisation zu aktivieren.

![Image 602](index-575_1.jpg)

![Image 603](index-575_2.jpg)

**552** 13 Fragenkataloge in Moodle

**Bild 13.35** Der Wertebereich kann an die gewünschten Werte angepasst und die Aufgaben somit praxisnah formuliert werden.

**Bild 13.36** Die im Test verwendeten Werte werden nicht grundsätzlich beim Test neu erzeugt. Es werden mit der Einrichtung der Frage Datensätze angelegt, aus denen die Fragestellung ihre Werte bezieht.

![Image 604](index-576_1.jpg)

13.3 Fragetypen und Syntax

**553**

**Bild 13.37** Hier wird ein soeben erzeugter Datensatz einschließlich der Berechnung und der verwendeten Werte angezeigt.

Wie in den Illustrationen zu erkennen ist, können die Wertebereiche aller Variablen individuell für die Aufgabe gewählt werden. Damit lassen sich sehr praxisnahe Aufgaben gestalten. Soll beispielsweise aus dem gegebenen Volumen eines Schwimmbeckens welches eine Länge von 50 m hat, für verschiedene Breiten die jeweilige Wassertiefe errechnet werden, sind für praxisnahe Aufgaben die vorgeschlagenen Zahlen von 1 bis 10 nicht realistisch. Die Wertebereiche lassen sich manuell anpassen.

Bei der Berechnung der Datensätze wird man schnell feststellen, dass Moodle eine gewisse Zeit für die Antwort und den Aufbau der Seite beansprucht. Während einer Prüfung, die rechtliche Relevanz haben kann, ist es jedoch wichtig, dass die verfügbare Zeit nicht durch ein langsames IT-System vergeudet wird. Aus diesem Grund wird mit der berechneten Frage ein Datensatz mit möglichen Inhalten der Ersatzzeichen angelegt und gespeichert.

Wie viele Zahlenkombinationen damit möglich sind, wird mit der Anlage der Frage be -

stimmt. Moodle berechnet also nicht bei der Aufgabenstellung Zufallszahlen, sondern wählt diese aus der bereits vorhandenen Datenbank aus!

Dieses Verfahren bietet noch einen weiteren Vorteil: Es ist denkbar, dass während des Tests eine weitere berechnete Frage gestellt wird, die zweckmäßiger Weise mit den gleichen Zahlen arbeitet, jedoch eine andere Größe erfragt. In diesem Beispiel – es wird aus einer gegebenen Spannung und einem gegebenen Strom die elektrische Leistung P = U*I berechnet –

bietet es sich an, in einer weiteren (berechneten) Frage nach der Größe des Widerstands zu fragen. Auch hier werden wieder die beiden Größen U und I benötigt. Die Berechnung des Widerstandes R = U/I erfolgt jedoch mit einer anderen Formel, welche die Kandidaten beherrschen müssen. Dazu müssen die Fragen allerdings _synchronisiert_ werden.

![Image 605](index-577_1.png)

![Image 606](index-577_2.png)

![Image 607](index-577_3.png)

**554** 13 Fragenkataloge in Moodle

**Bild 13.38** Eingabe eines Lösungsvorschlags (hier in der Vorschau): Der Betrag ist richtig und es wird auch die Einheit angegeben.

**Bild 13.39** Die Antwort ist richtig! Sie wird mit der vollen Punktzahl honoriert.

**Bild 13.40** Obwohl die Lösung im Betrag richtig ist, wurde die Angabe der Maßeinheit vergessen. Dies kostet den Abzug eines Punkts.

![Image 608](index-578_1.png)

13.3 Fragetypen und Syntax

**555**

**Bild 13.41** Hier wurde eine falsche Antwort eingetragen. Die richtige Lösung wird im roten Bereich dargestellt. Es werden keine Punkte vergeben.

**13.3.8■Berechnete Multiple Choice-Aufgabe**

Die berechnete Multiple Choice-Frage hat viele Parallelen zur einfachen berechneten Aufgabe. So ist die Syntax der Variablen, also der Ersatzzeichen, absolut identisch:

Ersatzzeichen werden in geschweifte Klammern geschrieben

Ersatzzeichen dürfen keine Leerzeichen enthalten

Auch die Schreibweise der Formeln entspricht weitgehend dem Verfahren, wie es bei den berechneten Fragen zu sehen war: Es gelten die üblichen Zeichen für die vier Grundrechenarten (+, –, * und /) sowie Klammern. Hinzu kommen die Funktionen aus Tabelle 13.1.

Anders als bei den berechneten Fragen wird bei den berechneten Multiple Choice-Antworten ein Gleichheitszeichen benötigt! Dies ist wichtig, weil die Antworten nicht allein rein numerisch, sondern auch in der Form kurzer Texte formuliert werden können, die errechnete Werte in ihrer Aussage enthalten.

Der gesamte Ausdruck muss ebenfalls in geschweifte Klammern gefasst werden! Für die in der Fragestellung geforderte Berechnung des Widerstands aus der Spannung und dem Strom würde man also diese Formel in die Antwortzeile eintragen:

**{={U}/{I}}**

Damit auch eine Einheit in der Antwort enthalten ist, wird diese einfach dazu geschrieben.

Das (entsprechend ergänzte) Beispiel sieht nun wie folgt aus:

**{={U}/{I}}** Ohm

In die Antwortzeile können also auch ganze Sätze eingebaut werden, die sowohl das Ergebnis als auch die ursprünglichen Werte beinhalten:

Aus der Spannung {U} V und dem fließenden Strom {I} A errechnet sich der Widerstand nach dem Ohm’schen Gesetz mit einer Größe von {={U}/{I}} Ohm.

**556** 13 Fragenkataloge in Moodle

**Gleichheitszeichen nur bei berechneten Multiple Choice-Fragen**

Bitte beachten: Bei einfachen berechneten Fragen ist die Form der Beantwortung rein numerisch und es ist ein, von den Kandidaten zu berechnender, Wert einzutragen. Das Feld ist also leer und erwartet das Ergebnis. Bei der einfachen berechneten Frage wird also KEIN Gleichheitszeichen benötigt.

Anders sieht es bei der Multiple Choice-Version der berechneten Frage aus: Hier werden Textantworten vorgegeben. Die Kandidaten wählen lediglich die richtigen Antworten aus. Damit Berechnungen von der reinen Präsentation

einer Formel unterschieden werden können, wird die besondere Syntax mit

dem Gleichheitszeichen benötigt.

■

Zwei weitere Unterschiede zur reinen berechneten Frage sind:

Die fehlende Definition von Einheiten einschließlich der zugehörigen Faktoren.

Außerdem werden keine Toleranzen für die Rechenergebnisse definiert.

Beides ist nicht nötig, weil die Antworten nicht aus (von den Lernenden) frei geschriebenen Rechenergebnissen bestehen, sondern durch die Wahl einer oder mehrerer vorgegebener Lösungen erfolgen.

Die übrigen Schritte gleichen denen der berechneten Frage, wobei auch hier im Wesentlichen die Erzeugung der Datensätze für die Variablen bzw. _Ersatzzeichen_ von Bedeutung ist.

Sie sind in ihrem Wertebereich und in ihrer Anzahl frei zu wählen. Darüber hinaus können sie mit gleichnamigen Ersatzzeichen von Fragen in einem Test im gleichen Kurs synchronisiert werden.

Parallelen gibt es natürlich auch zu den regulären Multiple Choice-Fragen (vgl. Ab -

schnitt 13.3.1). Es können zahlreiche Antwortmöglichkeiten entwickelt werden. Auch ist es möglich, dass mehrere Antworten richtig sind. Ein Beispiel wäre eine Antwort in einer bestimmten Länge, die in einer Antwort in Meter, in einer anderen in Fuß mit den jeweiligen Umrechnungen gegeben wird. Damit mehrere Antworten gültig sein können, muss die entsprechende Option aktiviert werden. Außerdem muss gewährleistet sein, dass mit der richtigen Beantwortung aller Frageteile auch tatsächlich 100 % der Punkte erreichbar sind.

Bei Abgabe einer falschen Antwort ist durch Vergabe von „–100 %“ der Entzug aller Punkte für diese Aufgabe möglich, auch wenn eine oder mehrere richtige Antwortelemente markiert wurden.

![Image 609](index-580_1.jpg)

![Image 610](index-580_2.jpg)

13.3 Fragetypen und Syntax

**557**

**Bild 13.42** In einer berechneten Multiple Choice-Fragestellung müssen auch die einer Berechnung zugrunde liegenden Werte enthalten sein. Dies funktioniert durch den Einsatz von Platzhaltern bzw.

„Ersatzzeichen“, wie sie in Moodle genannt werden.

**Bild 13.43** Platzhalter werden sowohl in der Antwort als auch im Feedback eingesetzt. So kann im Feedback der Rechenweg mit echten Zahlen dargestellt werden.

![Image 611](index-581_1.png)

![Image 612](index-581_2.png)

**558** 13 Fragenkataloge in Moodle

**Bild 13.44** Natürlich braucht eine Multiple Choice-Frage auch falsche Antworten. Auch diese werden mithilfe der Platzhalter erzeugt, um selbst Fehler plausibel erscheinen zu lassen.

**Bild 13.45** In der Vorschau erscheinen Fragestellung und Antwortvorschläge mit den tatsächlich verwendeten Zahlen.

![Image 613](index-582_1.png)

![Image 614](index-582_2.png)

13.3 Fragetypen und Syntax

**559**

**Bild 13.46** Es wurde die richtige Antwort gewählt und es wird die volle Punktzahl vergeben.

**Bild 13.47** Eine klar falsche Antwort! Es werden keine Punkte vergeben, jedoch wird neben der falschen Antwort ein Feedback gegeben, welches den Kandidaten hilft, ihren eigenen Fehler zu verstehen.

**560** 13 Fragenkataloge in Moodle

**13.3.9■Drag and Drop auf ein Bild**

Eine sehr interessante Aufgabenstellung, die sich auch gut zur Verwendung im Präsenzunterricht eignet, um ein spontanes Feedback zu einer Kurseinheit einzufordern, ist das _Drag and Drop auf ein Bild_. Da diese Frage vorwiegend mit rein grafischen Elementen gestaltet wird, ist sie zudem auch für untere Klassenstufen2 gut geeignet.

Neben den üblichen Pflichtelementen wie Fragetitel und Fragetext sowie der Festlegung der erreichbaren Punktzahl, ist für diese Art der Fragestellung ein detailreiches Hintergrundbild nötig, das eine Auflösung von bis zu maximal 600 x 400 Bildpunkten haben sollte.

Zusätzlich werden _verschiebbare Objekte_ benötigt. Das können Bilder in einem der folgenden Formate sein:

GIF

JPG/JPEG

PNG

SVG

Die Bilder, die als verschiebbare Objekte verwendet werden, sollten nicht mehr als 150 Bildpunkte in der Breite und 100 Bildpunkte in der Höhe haben.

**Alternativen beim Hochladen von Dateien**

Es gibt zwei Möglichkeiten, eine Bilddatei als verschiebbares Objekt in das System zu laden: Man kann den Weg über den Dialog _Datei wählen_ verwenden oder die Bilddatei einfach aus dem Explorer-Fenster des Betriebssystems in das dafür vorgesehene Feld ziehen.

■

Es ist auch möglich, einen Text als ein verschiebbares Objekt zu deklarieren. Der Text sollte jedoch sehr kurz und knapp, idealerweise ein Stichwort sein, weil der Platz auf dem Hintergrundbild sehr begrenzt ist. Eine kleine Steigerung des Schwierigkeitsgrads bietet die zufällige Anordnung der verschiebbaren Elemente. Damit wird der flüchtige Blick auf den Bildschirm des Nachbarn während der Prüfung selbst dann zu einem unsicheren Ergebnis führen, wenn dort scheinbar die gleiche Frage bearbeitet wird.

**Verschiebbare Texte mit Formaten**

Die unscheinbare Eingabezeile für den verschiebbaren Text versteht HTML-

Code. So ist es möglich, mithilfe von HTML Akzente zu setzen:

� <b>. . .</b> – Fettschrift

� <i>. . .</i> – Kursivschrift

2 Wenn von sogenannten „unteren Klassenstufen“ die Rede ist, ist dieser Begriff natürlich sehr differenziert zu betrachten, denn es muss zumindest die Fähigkeit der Lernenden entwickelt sein, sich im Moodle-System anzumelden und in den Kursen zu navigieren.

![Image 615](index-584_1.png)

13.3 Fragetypen und Syntax

**561**

� <su**p**>. . .</su**p**> – hochgestellt

� <sub>. . .</sub> – tiefgestellt

� <span style=“_CSS-Code_“>. . .</span> – Formatierung mit CSS-Code

■

Für eine sehr komplexe Aufgabenstellung können die verschiebbaren Objekte in Gruppen gegliedert werden. Es können nur Objekte auf die zu einer Gruppe passende _Dropzone_ geschoben werden. Damit kann die Aufgabe insgesamt vereinfacht oder thematisch in Teilaufgaben strukturiert werden.

**Bild 13.48** Wie bei jeder Frage gehören ein Fragetitel und ein Fragetext zu den wichtigsten Festlegungen bei einer Frage. Wichtig ist grundsätzlich auch die Festlegung der zu vergebenden Punktzahl.

![Image 616](index-585_1.png)

**562** 13 Fragenkataloge in Moodle

**Bild 13.49** Das Hintergrundbild ist die Ablagefläche für die Antworten. Es sollte Details beinhalten, nach denen gefragt wird.

![Image 617](index-586_1.png)

13.3 Fragetypen und Syntax

**563**

**Bild 13.50** „Unbekannter“ Typ ist etwas ungeschickt im System formuliert. Es handelt sich hier um Bilder in einem von vier Dateitypen, die hochgeladen werden können.

![Image 618](index-587_1.png)

**564** 13 Fragenkataloge in Moodle

**Bild 13.51** Ein verschiebbarer Text wird in die Textzeile am Ende des Antwortfelds eingetragen.

Die „Drag and Drop“-Aufgabe ist nur dann sinnvoll, wenn die richtigen Ablageorte, die sogenannten _Dropzones_, für die verschiebbaren Objekte eindeutig definiert sind. Die Größen der Dropzones legt Moodle automatisch fest. Es gibt einen Unterschied zwischen einer grafischen Zone und einer Text-Zone. Werden gemischte verschiebbare Elemente verwendet, dominiert das Format der grafischen Zone, damit alle Ablagebereiche das gleiche Aussehen haben.

Um die Dropzone zu definieren, braucht es darüber hinaus Koordinaten. Hier wird der linke obere Punkt der Dropzone festgelegt. Es gibt zwei Möglichkeiten, um diese Deklarationen vorzunehmen:

Die kompliziertere Variante ist es, auf dem Originalbild in einem Bildbearbeitungsprogramm (Bild 13.52 zeigt ein Beispiel mit dem kostenlosen Programm GIMP) die Koordinaten der Bildpunkte zu ermitteln. In den meisten Programmen wird die Position des Mauszeigers in der Statuszeile angezeigt. Die so ermittelten Koordinaten werden in die Felder _links_ und _oben_ eingetragen.

![Image 619](index-588_1.jpg)

13.3 Fragetypen und Syntax

**565**

Man muss allerdings nicht unbedingt investigativ in einer zusätzlichen Software tätig werden. Es geht durchaus einfacher, wenn man zunächst alle Koordinaten mit Standard-Parametern besetzt, die Frage zwischenspeichert (und weiterbearbeitet) und dann die in der Vorschau angezeigten verschiebbaren Elemente mit der Maus an die gewünschte Position verschiebt. Nach _erneutes Speichern_ der Frage werden die linken oberen Koordinaten der Dropzones automatisch aus den Positionen der Elemente übernommen.

**Bild 13.52** Am Ort, wo das rote Kreuz – stellvertretend für das Markierungskreuz des Mauszeigers –

platziert wurde, soll eine Dropzone eingefügt werden. Die Koordinaten sind im links umrandeten Bereich ablesbar und können in Moodle übernommen werden.

![Image 620](index-589_1.png)

![Image 621](index-589_2.png)

**566** 13 Fragenkataloge in Moodle

**Bild 13.53** Die Dropzones werden durch die Koordinaten des linken oberen Eckpunkts definiert.

Das zugeordnete Feld wird mit einer Drop-down-Liste gewählt.

**Bild 13.54** Um die Elemente in die Vorschau (in der Aufgabendeklaration!) anzuzeigen und gezielt verschieben zu können, muss die Frage gelegentlich gespeichert und danach weiter bearbeitet werden.

![Image 622](index-590_1.png)

13.3 Fragetypen und Syntax

**567**

**Bild 13.55** Die verschiebbaren Elemente werden außerhalb des Hintergrundbilds platziert und von der Kandidatin oder dem Kandidaten mit der Maus auf die jeweilige Dropzone geschoben.

![Image 623](index-591_1.png)

**568** 13 Fragenkataloge in Moodle

**Bild 13.56** Für jede richtige Zuordnung gibt es Punkte. Die volle Punktzahl wird erreicht, wenn alle Elemente richtig zugeordnet wurden.

**13.3.10■Drag and Drop auf einen Text**

Lückentexte sind eine sehr beliebte Fragetechnik. Moodle sieht dafür eine Variante zur freien Eingabe der Lösungen in die Textlücken vor, die jedoch in ihrer Syntax sehr komplex und in der Gestaltung der Texte anspruchsvoll ist (vgl. Abschnitt 13.3.13). Eine „Drag and Drop“-Aufgabe auf Textlücken ist dagegen sehr einfach zu gestalten. Auch sind Schreibfehler ausgeschlossen, weil die Lösungsworte bereits vorverfasst sind und in der Form verschiebbarer Elemente vorliegen. Diese Elemente werden mit der Maus auf die freien Felder geschoben, die durch Platzhalter in den Fragetext eingefügt werden.

Das Prinzip zur Erstellung eines solchen Fragetextes ist einfach: Aus dem Originaltext werden Wörter ausgeschnitten und diese in ein Antwortfeld unter _Auswahl_ eingesetzt. Auf der linken Seite ist neben dem Antwortfeld der Name des Platzhalters zu finden. Er wird durch ein Doppelpaar eckiger Klammern und eine fortlaufende, von Moodle generierte Zahl gebil-

![Image 624](index-592_1.jpg)

![Image 625](index-592_2.jpg)

13.3 Fragetypen und Syntax

**569**

det. Der erste Platzhalter, also das erste freie Feld, auf das ein verschiebbarer Text abgelegt werden kann, lautet demnach **[1](1)**. Dieser Platzhalter wird entsprechend in den Text geschrieben und das ursprüngliche Wort gelöscht (vgl. Bild 13.57).

Wie bereits bei den „Drag and Drop“-Aufgaben mit Bildern können die Antwortfelder auch hier gruppiert und damit verschiedenen Teilaufgaben zugeordnet werden.

**Bild 13.57** Im Fragetext werden anstelle der gesuchten Begriffe Platzhalter eingefügt.

**Bild 13.58** Jeder Variablen – hier [1](1) bis [3](3) – wird ein Begriff zugeordnet. Es können auch Platzhaltergruppen definiert werden. Diese erzeugen verschiedene Elemente, die nur in bestimmten Feldern abgelegt werden können.

![Image 626](index-593_1.png)

![Image 627](index-593_2.png)

![Image 628](index-593_3.png)

**570** 13 Fragenkataloge in Moodle

**Bild 13.59** Die Kandidaten müssen die Begriffe in die Platzhalterfelder verschieben.

**Bild 13.60** Wenn alle Begriffe in die richtigen Felder verschoben wurden, gibt es natürlich die volle Punktzahl. Zudem wird allgemein die richtige Lösung gezeigt.

**Bild 13.61** Zwei der Begriffe wurden falsch zugeordnet. Für die richtige Zuordnung gibt es hier einen Punkt.

![Image 629](index-594_1.jpg)

13.3 Fragetypen und Syntax

**571**

**13.3.11■Drag and Drop auf Markierungen**

Der Fragetyp _Drag and Drop auf Markierung_ bedarf einer gewissen Sorgfalt bei der Definition der Dropzones. Der Fragetypus ähnelt zunächst einmal der im Abschnitt 13.3.9

beschriebenen Variante, zeigt jedoch in der späteren Frage keine Platzierungsflächen für die richtigen Antworten an. Es werden vielmehr unsichtbare Markierungen in ein Hintergrundbild gesetzt, auf die die verschiebbaren Antwort-Elemente abzulegen sind.

Die Ablagemarkierungen müssen also großzügig bemessen werden, damit eine reelle Chance besteht, die richtige Antwort zu liefern. Zudem ist es wichtig, den Lernenden das exakte Verfahren zu erläutern, um Missverständnisse und Reklamationen der Ergebnisse zu vermeiden.

**Bild 13.62** Wie auch bei der „Drag and Drop“-Aufgabe auf ein Bild wird hier ein Hintergrundbild benötigt. Allerdings sind später keine Ablageflächen zu sehen. Diese Aufgabe ist somit etwas schwieriger zu lösen.

Neben den unsichtbaren Umrissen der Dropzones, die eine möglichst klare Aussage bei der Platzierung der verschiebbaren Elemente erfordern, kann die Art der Antwortabgabe zu -

sätzlich interessanter gestaltet werden: Es ist durchaus möglich, ein Element mehr als einmal auf dem Hintergrundbild zu platzieren. Die Trefferwahrscheinlichkeit steigt zwar damit, jedoch geht dieses „Raten“ zulasten der erreichbaren Punktzahl. Mit der Deklaration der Frage kann bereits festgelegt werden, ob ein Element nur einmal, eine begrenzte Zahl oder beliebig oft während der Beantwortung der Frage auf das Hintergrundbild geschoben werden darf.

![Image 630](index-595_1.jpg)

**572** 13 Fragenkataloge in Moodle

**Bild 13.63** Zunächst einmal werden Markierungen und die zugeordneten Begriffe definiert. Die Positionierung erfolgt im Anschluss.

Die Dropzones, also die Ablagebereiche, können – anders als beim Fragetyp nach Ab -

schnitt 13.3.9 – nahezu beliebig gestaltet werden. Es ist auch hier möglich, die Felder ausgehend von den Ursprungskoordinaten des Bilds zu entwickeln, d. h. sie mit der Maus am Zentrum zu fassen, auf das Zielobjekt im Bild zu ziehen und dann die Größe anzupassen, jedoch ist es auch möglich, die Koordinaten sowie die zusätzlich erforderlichen Parameter manuell einzutragen. Etwas anspruchsvoller gestaltet sich dabei die Deklaration eines Polygon-Felds.

Wird dieser Feldentwurf ohne weitere Deklaration gewählt, so bietet Moodle ein Dreieck an.

Im Feld Koordinaten kann die Deklaration des Polygons jedoch um beliebig viele weitere Eckpunkte erweitert werden. Bild 13.52 zeigt ein Beispiel, wie die Koordinaten der Bildpunkte alternativ ermittelt werden können.

Die Festlegung der Koordinaten erfolgt nach dem folgenden Muster:

Kreis (x,y-Koordinaten des Zentrums sowie Radius r): x,y _**;**_ r – der Radius wird mit einem Semikolon von den x,y-Koordinaten des Kreismittelpunkts getrennt.

Rechteck (x,y-Koordinaten des linken oberen Eckpunkts sowie Breite b und Höhe h): x,y _**;**_ b,h

Polygon (x,y-Koordinatenpaare für jeden Punkt): x1,y1 _**;**_ x2,y2 _**;**_ x3,y3 _**;**_ . . .

![Image 631](index-596_1.jpg)

13.3 Fragetypen und Syntax

**573**

**Bild 13.64** Sollen die verschiebbaren Elemente nur ein einziges Mal platzierbar sein oder können Kandidaten damit das Hintergrundbild beliebig oft „dekorieren“? Die Festlegung wird mit der Zuweisung der Begriffe zu den Platzhaltern getroffen.

**Unterschied Komma und Semikolon**

Parameter eines Koordinatenpaares werden durch ein Komma, die verschiedenen Koordinatenpaare untereinander durch ein Semikolon voneinander getrennt. Bei Bildpunkten sind keine Dezimalbrüche üblich.

■

Die Möglichkeiten der Technik sind begrenzt! Es sollte also entweder mit sehr großzügig bemessenen Dropzones gearbeitet werden, die eine gewisse Toleranz auch außerhalb des Zielobjekts bieten, oder die Dropzone sollte – mit einer Polygonform – nahezu exakt das Zielobjekt nachbilden.

Auch die Kandidatinnen und die Kandidaten müssen richtig informiert werden: Es ist eine weit verbreitete Annahme, dass der Mittelpunkt des verschiebbaren Objekts in die Dropzone geschoben werden muss. Diese Annahme ist jedoch falsch! Nicht der Mittelpunkt, sondern der kleine Zielkreis links oberhalb des Objekts markiert die Ablage! Dessen Position wird ausgewertet. Bild 13.67 zeigt die Auswirkungen einer falschen Deutung: Obwohl

![Image 632](index-597_1.jpg)

**574** 13 Fragenkataloge in Moodle

die Fragen eigentlich vollkommen korrekt beantwortet wurden, wurde kein Punkt vergeben. Die Zielmarkierung der verschiebbaren Objekte lag immer deutlich außerhalb der Dropzones!

**Kontroversen vorprogrammiert!**

„Aber ich habe doch den richtigen Begriff auf das Objekt platziert!“ oder „Dann müssen Sie die Markierungen eindeutig setzen!“ – das sind nur Beispiele von Studierenden-Reaktionen auf Punktabzüge bei diesem Aufgabentypus. Das

Prinzip der Platzierung sollte im Vorfeld einer Prüfung klargemacht und gegebenenfalls auch in Tests geübt werden. Auf jedem Fall sollte das Prinzip mit der Aufgabenstellung – gegebenenfalls ergänzend im Fragetext – erklärt werden, um Missverständnisse und spätere Diskussionen zu vermeiden.

■

**Bild 13.65** Es können für die Dropzones verschiedene Formen deklariert werden: Kreis, Rechteck und Polygon.

![Image 633](index-598_1.jpg)

13.3 Fragetypen und Syntax

**575**

**Bild 13.66** Hier sind alle Antworten richtig platziert. Es gibt die volle Punktzahl.

![Image 634](index-599_1.jpg)

**576** 13 Fragenkataloge in Moodle

**Bild 13.67** Die Aufgabe muss klar erklärt werden! Obwohl die Lösungsbegriffe über die richtigen Dropzones gesetzt wurden, werden die Platzierungen nicht als richtig angesehen. Die Marker liegen außerhalb der definierten Bereiche.

**13.3.12■Einfach berechnet**

Die berechnete Frage (vgl. Abschnitt 13.3.7) erfordert einen gewissen administrativen Aufwand, der durch mehrere Dialogseiten bei der Erstellung einer Frage geprägt ist. Mit der _einfach berechneten Frage_ steht eine Alternative zur Verfügung, die vergleichbare Aufgabenstellungen ermöglicht und trotzdem die komplette Aufgabengestaltung in nur einem Dialog gestattet.

Auch hier werden Platzhalter (Ersatzzeichen) verwendet, die sowohl in der Fragestellung, im Feedback als auch natürlich in der Berechnung der Lösung zum Einsatz kommen. Die Syntax entspricht der bei berechneten Fragen einschließlich der Funktionen (Tabelle 13.1).

Für die Ersatzzeichen werden wie bei der berechneten Frage mit der Deklaration Zahlenwerte angelegt und in Datensätzen gespeichert. Eine direkte Berechnung der Zufallszahlen erfolgt also nicht während der Aufgabenstellung in der laufenden Prüfung. Das verbessert die Performance des Systems.

![Image 635](index-600_1.jpg)

![Image 636](index-600_2.jpg)

13.3 Fragetypen und Syntax

**577**

Die Rechenergebnisse – wenn gefragt, mit den Maßeinheiten – werden frei in das Antwortfeld eingetragen. Durch Rundungen können aber Abweichungen von den durch den Computer errechneten Werten entstehen. Um die Antworten dennoch werten zu können, lassen sich Toleranzgrenzen festlegen. Wird die Verwendung von Maßeinheiten und deren Angabe in der Lösung erzwungen, lassen sich selbstverständlich auch die Faktoren der Teiler und Vielfachen deklarieren.

**Bild 13.68** Auch bei der einfach berechneten Frage kommen wieder die Ersatzzeichen (Variablen) in der bereits bekannten Schreibweise zum Einsatz.

**Bild 13.69** In der Antwortformel können auch Funktionen verwendet werden.

![Image 637](index-601_1.jpg)

![Image 638](index-601_2.jpg)

**578** 13 Fragenkataloge in Moodle

**Bild 13.70** Die Verwendung der Maßeinheiten ist in technischen Berechnungen sehr wichtig und sollte auch im Ergebnis eingefordert werden.

**Bild 13.71** Hier ist der wesentliche Unterschied zur „berechneten Frage“, dass die Datensätze für die Ersatzzeichen direkt in der ersten Deklarationsseite erzeugt werden.

![Image 639](index-602_1.png)

13.3 Fragetypen und Syntax

**579**

**Bild 13.72** Wenn die Lösung vom Betrag her richtig ist und auch die Maßeinheit (sofern in der Aufgabenstellung gefordert) in das Lösungsfeld eingetragen wurde, gibt es die volle Punktzahl.

**13.3.13■Lückentext**

Der Lückentext ist eine sehr aufwendig zu formulierende Frage. Sie wird als reiner Text gestaltet. Zu empfehlen ist die Verfassung der Texte in einem Texteditor, wie er auch von Programmierern verwendet wird. Ungeeignet ist dagegen die Verwendung eines Textverarbeitungsprogramms wie MS-Word oder LibreOffice Writer. Diese Programme liefern _formatierten Text_. Formatierter Text (Fett- oder Kursivschrift etc.) ist jedoch nur rein optisch auf dem Bildschirm oder auf dem Ausdruck zu sehen. Betrachtet man eine Word- oder Writer-Datei, so ist diese neben dem reinen, meist kaum noch deutbaren Text mit für den Menschen nicht mehr interpretierbarem Code durchmischt. Diese Dateien sind für Moodle-Fragen ungeeignet, weil hier nur reiner, unformatierter Text benötigt wird.

**Timeout bei Moodle beachten!**

Der zeitliche Aufwand für die Formulierung einer Lückentextfrage kann sehr groß sein. Möglicherweise wurde ein Zeitlimit für eine Moodle-Sitzung (Session Timeout) festgelegt, welches zum Logout führt, wenn während dieser Zeit keine Aktivität im System erkennbar ist. Hat man Pech und braucht sehr lange für die Verfassung der Frage, wird diese möglicherweise beim Versuch, die Frage zu speichern nicht mehr angenommen. Besser ist es, die Frage in einem externen Programm vorzubereiten.

■

Lücken werden mit einer geschweiften Klammer eingeleitet und auch wieder beendet:

**{**Lückenaufgabe**}**

**580** 13 Fragenkataloge in Moodle

Die Definition der „Lücke“ kann mit einer Zahl beginnen. Diese entspricht einem Faktor, der die Wertigkeit der Antwort beschreibt. Ist die Lückentextaufgabe aus beispielsweise vier Teilaufgaben mit insgesamt 5 Punkten und eine der Teilaufgaben mit der Wichtung „2“

bewertet, dann wird die richtige Lösung dieser Teilaufgabe zwei Punkte einbringen, die der anderen jeweils einen Punkt.

**Wichtungsangabe ist optional**

Die Angabe einer Wichtung, mit welcher die anteilige Punkteverteilung bei der Beantwortung der Teilaufgaben geregelt wird, ist nicht verpflichtend. Wird keine Wichtung angegeben und die Deklaration der Lücke direkt mit der Kennzeichnung des Typs begonnen, gilt eine Wichtung von Eins.

■

Während der reine Fragetext als unformatierter Text sehr einfach zu gestalten ist, ist die Syntax der Lücken sehr umfangreich und anspruchsvoll. Dies beginnt bei der Festlegung des Lückentypus. Hierbei sind folgende Kennzeichnen möglich (Tabelle 13.2):

Kurzantworten

Numerische Antworten

Multiple Choice-Antworten (Wahl im Dropdown-Menü, Radiobutton oder Checkboxen in horizontaler oder vertikaler Ausrichtung)

Die Kennzeichen müssen großgeschrieben werden. Sie werden von Doppelpunkten einge-schlossen.

**Tabelle 13.2** Art der Lückentextaufgabe

Kennzeichen

Groß-/Klein- Horizontal/ Sonstiges

schreibung

vertikal

:SHORTANSWER:

Unwichtig

Kurzantwort

:SA:

Unwichtig

Kurzantwort

:MW:

Unwichtig

Kurzantwort

:SHORTANSWER_C:

_WICHTIG_

Kurzantwort

:SAC:

_WICHTIG_

Kurzantwort

:MWC:

_WICHTIG_

Kurzantwort

:NUMERICAL:

Zahl

Numerische Kurzantwort

:NM:

Zahl

Numerische Kurzantwort

:MULTICHOICE:

./.

Auswahlmenü

:MC:

./.

Auswahlmenü

:MULTICHOICE_V:

./.

Vertikal

Radiobutton

:MCV:

./.

Vertikal

Radiobutton

:MULTICHOICE_H:

./.

Horizontal

Radiobutton

:MCH:

./.

Horizontal

Radiobutton

:MULTIRESPONSE:

./.

Vertikal

Checkboxen

13.3 Fragetypen und Syntax

**581**

Kennzeichen

Groß-/Klein- Horizontal/ Sonstiges

schreibung

vertikal

:MR:

./.

Vertikal

Checkboxen

:MULTIRESPONSE_H:

./.

Horizontal

Checkboxen

:MRH:

./.

Horizontal

Checkboxen

:MULTICHOICE_S:

./.

Auswahlmenü, Mischung der Fragen ist

möglich

:MCS:

./.

Auswahlmenü, Mischung der Fragen ist

möglich

:MULTICHOICE_VS:

./.

Vertikal

Radiobutton, Mischung der Fragen ist

möglich

:MCVS:

./.

Vertikal

Radiobutton, Mischung der Fragen ist

möglich

:MULTICHOICE_HS:

./.

Horizontal

Radiobutton, Mischung der Fragen ist

möglich

:MCHS:

./.

Horizontal

Radiobutton, Mischung der Fragen ist

möglich

:MULTIRESPONSE_S:

./.

Vertikal

Checkboxen, Mischung der Fragen ist

möglich

:MRS:

./.

Vertikal

Checkboxen, Mischung der Fragen ist

möglich

:MULTIRESPONSE_HS: ./.

Horizontal

Checkboxen, Mischung der Fragen ist

möglich

:MRHS:

./.

Horizontal

Checkboxen, Mischung der Fragen ist

möglich

Für die Lösungsbegriffe – egal, ob es sich um Kurztextantworten oder um eine Auswahl handelt – wird das Zeichen „Tilde“ _**~**_ als Trennzeichen verwendet. Eine richtige Antwort (100 %) wird mit dem vorangestellten Gleichheitszeichen gekennzeichnet. Eine Vergabe von Teilpunkten ist auch prozentual möglich. Der Betrag der Prozentangabe wird mit einem beginnenden und einem schließenden Prozentzeichen deklariert:

%100 % – 100 % der für diese Teilaufgabe erreichbaren Punkte werden vergeben. Die (Teil)-Aufgabe ist richtig.

%0 % – die Lösung der (Teil)-Aufgabe ist falsch.

%33 % – dieser Lösungsvorschlag der (Teil)-Aufgabe bringt ein Drittel der in dieser Aufgabe erreichbaren Punktzahl.

**Ein Ergebnis von 100 % muss möglich sein!**

Die verschiedenen Varianten der Lückentextfrage lassen auch verschiedene Antworten zu: Während Kurzantworten und „Multiple Choice“-Typen, deren

Ergebniseingabe mithilfe von Radiobutton erfolgt, nur eine einzige Eingabe vorsehen, lassen Checkboxen mehrere Antwortmarkierungen zu. Die Summe

aller möglichen richtigen Teillösungen muss 100 % ergeben.

■

![Image 640](index-605_1.png)

**582** 13 Fragenkataloge in Moodle

Die Syntax sieht auch Feedback vor. Das Feedback wird unmittelbar nach der Antwortoption getrennt durch ein „Hash“-Zeichen (#), geschrieben. Es wird nach der Abgabe der Antwort sichtbar, wenn man mit dem Mauszeiger über das Antwortfeld fährt.

Ein Beispiel: Es wird eine einfache Multiple Choice-Lückentextfrage (vgl. Bild 13.73) formuliert:

_Die Aussage, das Modular Object Oriented Dynamic Learning Environment, kurz:_

_**{2:MC:=Moodle#Die Antwort ist richtig!~H5P#Diese Antwort ist leider falsch!}**_

_ist zutreffend._

Es ist nur der in die geschweiften Klammern gesetzte Bereich interessant, der von links nach rechts analysiert werden soll:

Die Zahl _**2**_ wichtet die Zahl der erreichbaren Punkte auf das Doppelte. In dieser Aufgabe gibt es nur eine einzige Lücke, sodass die erreichbare Punktzahl damit zwei beträgt.

Die Kennzeichnung _**:MC:**_ steht für eine Multiple Choice-Lücke. Den Kandidaten wird ein Auswahlmenü angeboten. Darin wird die Lösung markiert. Die Reihenfolge der Lösungs-optionen entspricht hier der Reihenfolge der Deklaration. Sollen die Fragen gemischt werden, so müsste die Kennzeichnung _:MULTICHOICE_S:_ oder _:MCS:_ gewählt werden.

_**=Moodle**_ – das Gleichheitszeichen markiert die richtige Lösung. Alternativ könnte an dieser Stelle _%100 %_ stehen. Dem Gleichheitszeichen folgt der Lösungsbegriff, der auch einen längeren Text darstellen kann.

_**#**_ – das Zeichen Hash (die „Raute“) trennt die Lösungsoption von dem dazu gehörigen Feedback. Nach Abgabe der Lösung wird dieses Feedback beim Überfahren des Felds mit der Maus sichtbar.

_**~H5P**_ – die Tilde – das Zeichen ~ – trennt die verschiedenen Antwortoptionen voneinander. Hier fehlt zwischen der Tilde und dem Begriff „H5P“ das Gleichheitszeichen, wodurch diese Option als falsch deklariert wird. Alternativ könnte an dieser Stelle auch %0 %

gesetzt werden.

_**#**_ – auch für die falsche Antwortoption kann nach einem Hash (Raute) ein Feedback formuliert werden.

**Position des richtigen Ergebnisses**

Die richtige Antwort muss nicht unbedingt an der ersten Stelle der Reihenfolge gesetzt werden. Eine richtige Antwort wird jedoch grundsätzlich mit den

Gleichheitszeichen oder mit einem Prozentsatz größer als 0 % gekennzeichnet.

In der Summe muss jedoch bei der Beantwortung aller richtigen Antworten

100 % erreichbar sein.

■

**Bild 13.73** Eine Lückentextaufgabe in der einfachen Multiple Choice-Variante (Kennzeichnung: :MC: oder :MULTICHOICE:

![Image 641](index-606_1.png)

![Image 642](index-606_2.png)

![Image 643](index-606_3.png)

![Image 644](index-606_4.png)

![Image 645](index-606_5.png)

13.3 Fragetypen und Syntax

**583**

**Bild 13.74** Das Feedback zum Ergebnis wird sichtbar, wenn man das Feld mit dem Mauszeiger über-fährt.

**Bild 13.75** Die Kennzeichnung :MRS: oder :MULTIRESPONSE_S: bietet senkrecht platzierte Checkboxen als Lösungseingabe an. Checkboxen ermöglichen mehrere Markierungen.

**Bild 13.76** Die waagerechte Anordnung von Checkboxen wird mit der Kennzeichnung :MRHS: oder

:MULTIRESPONSE_HS: erreicht. Auch hier können mehrere Lösungen gewählt werden.

**Bild 13.77** Optisch den Checkboxen ähnlich, in der Funktion jedoch verschieden sind die Radiobutton. Diese lassen nur eine einzige Wahl zu. Die hier verwendete Kennzeichnung ist :MCHS: oder

:MULTICHOICE_HS:

**Bild 13.78** Bei einem Lückentext, der Kurzantworten vorsieht, genügt es, nur eine einzige Antwortoption vorzusehen. Gibt es mehrere richtige Antwortmöglichkeiten, können alle Varianten erfasst und als richtig deklariert werden. Das hier gezeigte Beispiel verwendet die Kennzeichnung :SA: oder

:SHORTANSWER:

![Image 646](index-607_1.png)

**584** 13 Fragenkataloge in Moodle

Soll bei einem Lückentext in der Variante Kurzantwort auch ein Feedback bei einer falschen Antwort gegeben werden, so kann dies mithilfe des Zeichens _Asterisk_ * erfolgen. Der Asterisk steht als Platzhalter für ein oder mehrere beliebige Zeichen. Diese Deklaration muss allerdings an letzter Stelle erfolgen, weil sonst auch die richtige Antwort möglicherweise

„abgefangen“ und als falsch interpretiert wird.

Ein Sonderfall der Lückentextaufgabe ist die numerische Antwort. Diese Form unterscheidet sich von den _numerischen_ und den _berechneten_ Fragetypen, wie sie bereits in vorangegange-nen Abschnitten erläutert wurden. Es werden beispielsweise keine Maßeinheiten abgefragt.

Auch werden keine Datensätze mit der Formulierung der Aufgabe erzeugt. Es wird lediglich das numerische Ergebnis und eine absolute Toleranz als Ergebnis festgelegt. Der Zahlenwert des Ergebnisses und der Toleranzwert werden durch einen Doppelpunkt getrennt.

**Ein Beispiel**

_Ein Rechteck hat eine Breite von 4 cm und eine Höhe von 3 cm. Demnach ist dessen Flächen-inhalt **{1:NUMERICAL:%100 %12:0,5#12 Quadratzentimeter ist die richtige Antwort.}**_

_**cm**_ 2 _._

Diese Aufgabe wird mit einer einfachen Wichtung bewertet. Weil nur eine Lücke in der Teilaufgabe vorgesehen ist, wird somit in dieser auch nur ein Punkt vergeben. Anstelle der Kennzeichnung _:NUMERICAL:_ kann auch die kürzere Variante _:NM:_ verwendet werden. Anstelle des Gleichheitszeichens wird in diesem Beispiel die prozentuale Schreibweise verwendet:

_%100 %_. Das Ergebnis wird als ein rein numerischer Wert eingetragen. Eine Toleranz – diese wäre bei einem so eindeutigen Ergebnis wie in diesem Fall überflüssig – wird durch einen Doppelpunkt vom Betrag der Lösung getrennt. In diesem Beispiel wird eine Toleranz von 0,5

(zur Demonstration) gewährt. Als richtig werden also Lösungen von 11,5 bis 12,5 betrachtet.

Die Vielfalt der verwendeten Steuer- und Sonderzeichen generiert insgesamt ein Problem: Was, wenn die Fragestellung die Verwendung eines dieser Zeichen in darstellbarer Form erfordert? Das ist nur durch eine _Maskierung_ der Zeichen **{ } * # ~ = : / \** möglich! Die Maskierung erfolgt mithilfe eines sogenannten Backslashs **\**. Soll ein Backslash selbst in der Fragestellung ausgegeben werden, wird deswegen \\ geschrieben. Die Darstellung eines Ausdrucks in geschweifter Klammer in der Fragestellung wird also wie folgt formuliert:

\{Ausdruck in einer geschweiften Klammer\}

Lückentextaufgaben können insgesamt sehr komplex und umfangreich formuliert werden.

Dabei ist es möglich, die verschiedenen Varianten zu mischen und einzelnen Teilaufgaben eigene Wichtungen zuzuweisen. Die erreichbare Gesamtpunktzahl ergibt sich aus der Summe aller Teilpunkte.

**Bild 13.79** Das Ergebnis der gesamten Aufgabe sind drei Punkte. Weil der untere Aufgabenteil mit der Wichtung 2 deklariert wurde, hat die richtige Wahl des Textes entsprechend zwei Punkte eingebracht, während der richtigen Antwort in der numerischen Lücke, der keine Wichtung zugewiesen wurde (es gilt pauschal 1), nur ein Punkt zugeteilt wurde.

![Image 647](index-608_1.png)

13.3 Fragetypen und Syntax

**585**

**13.3.14■Lückentextauswahl**

Die unter Abschnitt 13.3.10 beschriebene Lückentext-Aufgabe _Drag and Drop auf einen Text_ sah verschiebbare Elemente vor, die jeweils in die richtigen Textlücken eingefügt werden mussten. Die Lückentextauswahl ist von der Entwicklung und Konfiguration betrachtet mit diesem Aufgabentypus vergleichbar, jedoch wird die Frage anders präsentiert. Die Präsentation der Lösungsvorschläge erfolgt in einer Dropdown-Liste.

Den Auswahlangeboten werden Variablen zugeordnet, die in doppelten eckigen Klammern geschrieben werden. Um den Satz „ _Auf jedem Werkstoff hat die Temperatur einen direkten_ _Einfluss auf dessen Leitfähigkeit_“ mit Textlücken zu versehen, kann die Aufgabe folgendermaßen in den Fragetext geschrieben werden:

Auf jedem **[1](1)** hat die **[2](2)** einen direkten Einfluss auf dessen Leitfähigkeit.

In der Auswahlliste werden nun Deklarationen wie in Bild 13.80 vorgenommen. Mithilfe der Gruppen können die Antwortvorschläge auf ganz bestimmte Lücken verteilt werden. Es werden nur die Auswahlen in der Dropdown-Liste angezeigt, welche der gleichen Gruppe angehören wie die deklarierte Lösung.

**Eindeutige Zuordnung ist erforderlich!**

Innerhalb einer Gruppe muss ein richtiger Lösungsbegriff einmalig sein. Eine Auswahl darf also nicht für mehrere Fragen richtig sein, weil Moodle Feldinhalte, nicht jedoch deren Bedeutungen zuordnet. Soll ein Begriff in mehreren Lücken richtig sein, muss dieser verschiedenen Gruppen angehören.

■

**Bild 13.80** Es können mehr Lösungsvorschläge definiert werden als es Lücken im Text gibt.

Es muss jedoch jeder Lücke eine Lösung zugeordnet werden.

![Image 648](index-609_1.jpg)

![Image 649](index-609_2.jpg)

![Image 650](index-609_3.jpg)

**586** 13 Fragenkataloge in Moodle

**Bild 13.81** 

Dieser Lücke werden Antwort-

verschläge der Gruppe A zuge-

ordnet.

**Bild 13.82** 

In dieser Lücke sind die Ant-

wortvorschläge der Gruppe B

gelistet.

**13.3.15■Zufällige Kurzantwort-Zuordnung**

Der Fragetyp _Kurzantwort_ (Abschnitt 13.3.4) sieht eine einzige Frage vor, die mit einem frei verfassten Begriff beantwortet werden kann. Wenn verschiedene Kurzantwort-Fragen in einer gemeinsamen Kategorie vorliegen, dann bietet die zufällige Kurzantwort-Zuordnung eine interessante Verwendungsmöglichkeit dieses bereits vorhandenen Fragenbestands an.

In der Fragengestaltung wird lediglich festgelegt, wie viele Fragen gestellt werden sollen und wie viele Punkte mit deren richtiger Beantwortung zu verdienen sind. Moodle analysiert nun den Fundus aus verfügbaren Kurzantwort-Fragen und präsentiert diese in einer gemeinsamen Oberfläche. Allerdings werden nun keine frei formulierten Kurzantworten von den Kandidaten erwartet, sondern diese wählen die Antworten aus einer Dropdown-Liste aus.

Jedes Feld enthält dabei die gleichen Antwort-Optionen in exakt der gleichen Reihenfolge.

**Bild 13.83** 

Die zufälligen Kurzantwort-

Zuordnungen basieren auf

bereits vorhandenen Kurzant-

wort-Fragen, die hier allerdings

in der Form von Zuordnungen

zusammengefasst werden.

13.4 Import und Export von Fragen

**587**

**■**

**■ 13.4■Import und Export von Fragen**

Es ist unschwer festzustellen, dass die Gestaltung eines prüfungstauglichen Fragenkatalogs eine sehr umfassende, zeit- und arbeitsaufwendige Angelegenheit ist. Dieser Aufwand lässt sich verringern, wenn man zusammenarbeitet. Im schulischen Bereich kann es also sinnvoll sein, Prüfungsfragen auf gleicher Ebene auszutauschen. In einer Großstadt oder in einem Bundesland gibt es viele Schulen des gleichen Zweigs. Innerhalb jeder einzelnen Schule sind verschiedene Lehrerinnen und Lehrer für ein Fach zuständig. Nehmen wir also ein einfaches (fiktives) Rechenbeispiel:

In einer Region (mit vergleichbaren Lehrplänen) existieren (angenommen) 20 Schulen eines Zweigs.

Es gibt in jeder dieser Schulen durchschnittlich drei Lehrerinnen und Lehrer, die dieses Fach in einer vergleichbaren Klassenstufe unterrichten und prüfen.

Jede Lehrkraft entwickelt in drei Schwierigkeitsstufen jeweils fünf Fragen.

Pro Frage soll großzügig ein Zeitaufwand von 30 Minuten (im Durchschnitt) eingeräumt werden. Es ist natürlich zu bedenken, dass der Entwurf sehr umfangreicher Lückentextaufgaben durchaus längere Bearbeitungszeiten beanspruchen kann.

In einer Arbeitszeit von 7,5 Stunden pro Lehrkraft entstehen somit insgesamt 900 Fragen.

Insgesamt fallen für die Erstellung des – tatsächlich bemerkenswerten – Fragenkatalogs ca.

450 Arbeitsstunden an.

Würde jede einzelne Schule diese 900 Fragen jeweils in eigener Verantwortung erstellen wollen, müsste jede Lehrkraft alleine 300 Fragen entwerfen und dafür jeweils 150 Stunden aufwenden. Jede einzelne Schulleitung müsste nur für dieses eine Fach Personalkosten für 450 Arbeitsstunden kalkulieren. Bitte beachten: Es handelt sich nur um ein einziges Schul-fach einer einzigen Klassenstufe in einem einzigen Schulzweig!

**Frage mit offener Antwort**

Wie viele Arbeitsstunden werden erfahrungsgemäß in die Erstellung und Korrektur von Klausuren investiert? Jede Lehrerin und jeder Lehrer „freut“ sich in diesem Zusammenhang bei den Korrekturen über „kreative Kalligrafie“ der

Lernenden bei der Beantwortung der Prüfungsfragen auf Papier. Für die Interpretation diverser Handschriften wird ein gewisser Zeitaufschlag benötigt.

■

Der Aufwand für die individuelle Gestaltung eigener Fragenkataloge kann natürlich durch eine kleinere Anzahl von Fragen erheblich reduziert werden. Das bedeutet allerdings eine häufige Wiederholung der Fragen und damit verbunden eine Verbreitung der Information einschließlich der Lösungen unter den Lernenden.

Stehen Lehrende der gleichen Fachbereiche verschiedener Schulen im direkten Dialog, kann der Zeitaufwand also deutlich gesenkt und ein sehr umfangreicher Fragenkatalog gemeinsam entwickelt werden. Dazu ist es erforderlich, die eigenen Fragen zu exportieren und in die Kataloge der anderen Systeme zu importieren.

**588** 13 Fragenkataloge in Moodle

**Fragenaustausch spart Zeit und Kosten!**

Der für Prüfungen und Lernzielkontrollen zu leistende Aufwand ist grundsätzlich signifikant. Es gibt wohl kaum eine Lehrkraft, deren Wohnzimmer nicht

permanent mit zu korrigierenden Klausuren belegt ist. Auch Online-Prüfungen sparen effektiv nur dann Zeit, wenn man die Möglichkeiten der Kooperation zu nutzen versteht.

■

**13.4.1■Export eines Fragenkatalogs**

Der Export einer Fragensammlung erfolgt zur Sicherung des eigenen Fragenkatalogs, aber auch, um die Fragen mit Kolleginnen und Kollegen zu teilen. Sicherheitskopien sollten grundsätzlich für den gesamten Kurs angefertigt werden. Dies wurde bereits in einem früheren Kapitel beschrieben.

Der Export eines _Fragenkatalogs_ ist nur nach Klärung der rechtlichen Rahmenbedingungen (Urheberrecht) zur gemeinsamen Nutzung im Kollegenkreis oder schulübergreifend möglich. Wie in der Einleitung jedoch sehr rudimentär angedeutet, ist das Potenzial zur Einsparung von Arbeitszeit sehr groß.

**Urheberrecht beachten!**

Die Ausarbeitung einer Prüfungsfrage basiert auf der Leistung eines Urhebers.

Es wird also geistiges Eigentum geschaffen, dessen Nutzungsrecht zu regeln ist.

■

Der Export der Fragen kann über den Hauptdialog nicht auf einzelne Fragen beschränkt werden, sondern wirkt auf ganze Kategorien. Der Vorgang erfolgt in der Kurs-Administration im Abschnitt _Fragensammlung_. Dort wird _Export_ gewählt und im sich öffnenden Dialog das Dateiformat, die gewünschte Kategorie und – sofern dies das gewählte Format unterstützt – ob die Kategorie und der Kontext in die Datei hineingeschrieben werden sollen.

Damit ist die Angelegenheit auch beinahe schon erledigt. Der Rest ist ein gewöhnlicher Download einer Datei aus einer Internet-Quelle.

![Image 651](index-612_1.jpg)

![Image 652](index-612_2.jpg)

13.4 Import und Export von Fragen

**589**

**Bild 13.84** Das Moodle-XML-Format erlaubt die flexibelste Erfassung aller möglichen Prüfungsfragen beim Export. Die Syntax ist jedoch recht komplex.

**Bild 13.85** Nach der Wahl des Datenformats und der zu exportierenden Fragenkategorie wird die XML-Datei in bekannter Weise auf dem PC gespeichert.

![Image 653](index-613_1.png)

**590** 13 Fragenkataloge in Moodle

**13.4.2■Export einer einzelnen Frage**

Es ist natürlich auch möglich, nur eine einzige Datei zu exportieren. Dazu wird in der Ak -

tionsspalte des Fragenkatalogs bei der gewünschten Frage die Auswahl _Als Moodle-XML_

_kopieren_ gewählt. Der Download startet in diesem Fall sofort. Weitere Einstellungen erfolgen nicht und es werden auch keine anderen Dateiformate als Alternative angeboten.

**Speicherort der exportierten Frage**

Wohin auf dem eigenen Computer die XML-Datei mit der gewählten Frage

gespeichert wird, hängt maßgeblich von den Einstellungen des Webbrowsers ab. In der Regel wird es sich hierbei um das Download-Verzeichnis handeln, das zu den Standard-Verzeichnissen des Windows-Betriebssystems zählt und für jeden Benutzer-Account individuell angelegt wird.

■

**Bild 13.86** Eine einzelne Frage kann direkt aus der Liste der Fragensammlung heraus exportiert werden. Hier ist allerdings lediglich das Moodle-XML-Format vorgesehen.

![Image 654](index-614_1.jpg)

13.4 Import und Export von Fragen

**591**

**13.4.3■Import eines Fragenkatalogs**

Beim Blick in den Import-Dialog für Fragen wird schnell auffallen, dass die Zahl der Dateiformate deutlich größer ist als dies zuvor beim Export der Fall gewesen war. Das liegt daran, dass Moodle auch in der Lage ist, verschiedene Fragensammlungen aus alternativen Lernmanagementsystemen zu übernehmen. Das sind u. a.:

Blackboard,

ExamView,

WebCT.

In der Rubrik _Allgemeines_ des Dialogs wird die Kategorie gewählt, denen die zu importierenden Fragen zugeordnet werden sollen. Wenn eine Datei mehrere Fragen beinhaltet, ist zu beachten, dass diese Fragen dann alle einer gemeinsamen Kategorie zugeordnet werden.

Sehen Lehrende die Zuordnung in ihrem System anders, müssen die Fragen in der Fragen-liste einzeln verschoben werden. Hierbei sind stets die Grenzen zu berücksichtigen, die durch die Reichweite der jeweiligen Rollen gegeben sind. Eine systemweite Verteilung der Fragen auf beliebige Kurse in beliebigen Bereichen kann nur durch die Moodle-Administration erfolgen.

Der eigentliche Upload der Fragendatei erfolgt über den bereits bekannten Dialog: Es kann eine Datei über die Schaltfläche _Datei wählen_ aus dem Explorer-Fenster (in einem Windows-System) oder durch Verschieben der Datei in das umrandete Feld (Drag and Drop) hochgeladen werden. Wichtig ist, dass die gewählte Datei in ihrem Format dem eingestellten Dateiformat entspricht und dass sie im UTF-8-Code vorliegt.

**Bild 13.87** Neben den aus Moodle direkt exportierten Fragen können auch verschiedene andere Quellen beim Fragen-Import berücksichtigt werden.

![Image 655](index-615_1.jpg)

**592** 13 Fragenkataloge in Moodle

**Bild 13.88** Die einzelnen Fragen werden an dieser Stelle in einem Fenster gelistet, sind jedoch als einzelne Fragen im Katalog zu finden.

**■**

**■ 13.5■ Dateiformate für den Fragen-Import**

**und -Export**

Beim Im- und Export von Fragen werden reine textbasierende Formate verwendet. Wenn diese Dateien extern, also außerhalb des Moodle-Systems bearbeitet werden, ist es wichtig, dass diese im _UTF-8_-Format gespeichert werden. Mit etwas manuellem Arbeitsaufwand oder mit geeigneten Konverter-Programmen ist es zudem möglich, Fragen für die Verwendung in Textverarbeitungsprogrammen aufzubereiten. Somit können Prüfungen durchaus sowohl im Moodle-System als auch alternativ schriftlich durchgeführt werden.

**13.5.1■AIKEN-Format**

Beim AIKEN3-Format handelt es sich um ein sehr einfaches, aber ausschließlich auf Sin gle-Choice-Fragen begrenztes Datenformat. Es gibt nur wenige Syntaxregeln zu beachten. Diese müssen jedoch eingehalten werden, um Fehler zu vermeiden:

3 Howard Hathaway Aiken, Ph. D (1900 – 1973). war ein US-amerikanischer Mathematiker und Computertechniker.

Nach ihm wurde u. a. der Aiken-Code, ein Komplementärcode zur Darstellung von Dezimalziffern mit vier Bit benannt, wobei die Bit-Werte der Ziffern 0 bis 4 den invertierten Bitwerten der Ziffern 9 bis 5 entsprechen.

![Image 656](index-616_1.png)

13.5 Dateiformate für den Fragen-Import und -Export

**593**

Die Datei muss als Textdatei im Format _UTF-8_ gespeichert werden.

Die Frage und jede Lösungszeile werden jeweils in eine eigene Zeile geschrieben.

Eine Lösungszeile beginnt stets mit einem groß geschriebenen Buchstaben.

Auf den (groß geschriebenen) Buchstaben folgt entweder ein Punkt oder eine schließende runde Klammer.

In die letzte Zeile wird die Lösung geschrieben (ausschließlich große Buchstaben). Die Lösung wird mit dem Begriff _ANSWER:_ eingeleitet.

**Ein Beispiel:**

Mit welchem Lernmanagement System setzen Sie sich hier gerade auseinander?

A. LMS

B. H5P

C. Moodle

D. Nudel

E. Gar keines

ANSWER: C

**Bild 13.89** Die Vorschau einer mit dem Aiken-Format importierten Frage.

**13.5.2■GIFT-Format**

Das General-Import-Format-Template-(GIFT)-Format ist ein textbasierendes (UTF-8) Be -

schreibungsformat für folgende Fragetypen:

Multiple Choice

Wahr/Falsch

Kurzantwort

Zuordnung

Lückentext

Numerisch

![Image 657](index-617_1.jpg)

**594** 13 Fragenkataloge in Moodle

Durch die Vielseitigkeit ist die Syntax etwas komplexer:

// Kommentarzeile

:: (Am Beginn _und_ am Ende des Ausdrucks!) Titel der Frage – Beispiel: _::Titel::_

# Feedback

%%Prozentzahl%% Wichtung/Anteilige Verteilung der erreichbaren Punktzahl

: Zahlenbereich einer numerischen Frage

-> Zuordnung

{Antwort} – öffnende und schließende geschweifte Klammern definieren die Antwortmöglichkeiten

{#Zahl} – numerische Antwort

= richtige Antwort

~ falsche Antwort

{T} wahre Aussage

{F} falsche/unwahre Aussage

**Jede Frage braucht einen Titel!**

Für jede Frage im GIFT-Format sollte ein Titel – _::Fragetitel::_ – vorgegeben werden.

Sonst verwendet Moodle die ersten Begriffe des Fragetextes.

■

**Beispiel für eine Zuordnungsfrage im GIFT-Format:**

// Beispiel für eine Zuordnungsfrage

::Stadt-Land-Fluss::

Ordnen Sie die Begriffe richtig zu:

{

=Stadt -> Villach

=Bundesland -> Kärnten

=Staat -> Österreich

=Fluss -> Drau

}

**Bild 13.90** 

Die im GIFT-Format importierte

Zuordnungsfrage wurde als

solche korrekt erkannt und

richtig dargestellt.

![Image 658](index-618_1.png)

13.5 Dateiformate für den Fragen-Import und -Export

**595**

**Beispiel für eine Kurzantwort im GIFT-Format:**

// Beispiel für eine Kurzantwortfrage

::Deutsche Kanzlerin::

Die erste deutsche Bundeskanzlerin heißt Angela {=Merkel}.

**Bild 13.91** Auch eine Kurzantwort-Frage lässt sich mit dem GIFT-Format sehr einfach importieren.

Auch Lückentexte lassen sich mit dem GIFT-Format erstellen. Allerdings wird grundsätzlich jede Lücke als eine Frage betrachtet. Das folgende Listing einer GIFT-Datei (.txt oder vergleichbar im UTF-8-Format) formuliert insgesamt vier Fragen.

**Beispiel für eine Lückentextfrage im GIFT-Format**

// Beispiel für eine Lückentextfrage

::Flüsse in Villach::

Von Norden nach Südosten fließt die {

=Drau

~Gail

~Donau

} durch Villach.

::Westzufluss in Villach::

Die {

=Gail

~Drau

~Donau

} trifft aus westlicher Richtung kommend bei Villach ein.

::Villach – Abfluss::

Zwei Flüsse münden bei Villach ineinander. Die {

=Drau

~Gail

~Donau

} ist der gemeinsame Strom, der in östliche Richtung abfließt.

::Meer-Zufluss der Villach-Flüsse::

Die Drau fließt letztendlich in der Nähe von Osijek (Kroatien) in die {

=Donau

~Drau

~Gail

} und mündet in das Schwarze Meer.

![Image 659](index-619_1.png)

![Image 660](index-619_2.png)

**596** 13 Fragenkataloge in Moodle

**Bild 13.92** Der Import der Lückentextfragen aus der beschriebenen Datei im GIFT-Format erzeugt vier neue Fragen in der Fragensammlung.

**Bild 13.93** Wichtig ist, dass jeder Frage ein eigener Titel (::Titel::) zugeordnet wird, damit die Teilfra-gen auch bei größeren Fragensammlungen im Katalog auffindbar sind.

13.5 Dateiformate für den Fragen-Import und -Export

**597**

**13.5.3■Moodle-XML-Format**

XML (= Extensible Markup Language) ist eine universell nutzbare Beschreibungssprache, die unter anderem zur Übertragung von Informationen zwischen Sender und Empfänger eingesetzt wird, die nach genau festgelegten Regeln kommunizieren. Die Syntax der Elemente wird individuell für die verschiedenen Anwendungen festgelegt. „Moodle XML“ legt Elemente fest, deren Inhalte die Felder der Fragendeklarationen ansprechen.

XML-Elemente bestehen grundsätzlich aus einem in spitzen Klammern geschriebenen _Start-Tag_ <TAG> und einem ebenfalls in spitzen Klammern geschriebenen _End-Tag_ </TAG>.

Letzterer wird vor dem gleichen Wortlaut des Tag-Namen zusätzlich mit dem Zeichen _Slash_ /

gekennzeichnet. Zwischen diesen beiden Tags befindet sich der Inhalt des Elements. Damit ist XML in der Struktur der Internet-Beschreibungssprache HTML (Hypertext Markup Language) sehr ähnlich.

Die erste Zeile von Moodle XML lautet unabhängig vom Inhalt der Fragensammlung:

<?xml version=”1.0” encoding=”UTF-8”?>

Die XML-Datei für den Im- und Export von Fragen wird mit dem Tag <quiz> .... </quiz> umschlossen. Kommentare können beliebig in die Datei eingefügt werden und erleichtern in größeren Dateien die Übersicht. Sie werden vom System ignoriert und haben rein infor-mativen Charakter. Die Schreibweise eines Kommentars lautet.

<!-- Kommentar -->

Nun können in einer einzigen Moodle-XML-Datei mehrere Fragen verschiedenen Typs transportiert werden: Das Element, in dem eine Frage eingebaut wird, lautet:

<question type=**”Fragetyp”** > .... </question>

Die Codes für den Typ sind von den Moodle-Entwicklern festgelegt worden. Damit wird der Fragetypus definiert und damit auch die Art und Weise, wie die folgenden Elemente zu interpretieren sind.

**Tabelle 13.3** Moodle-XML-Fragetypen

Fragetyp-Attribut

Moodle-Fragetyp

calculated

Berechnete Frage

calculatedmulti

Berechnete Multiple Choice-Frage

calculatedsimple

Einfach berechnete Frage

category

Kategorie („leerer“ Block eines Fragentyps)

cloze

Lückentext

ddimageortext

Drag and Drop auf ein Bild

ddmarker

Drag and Drop auf eine Markierung

ddwtos

Drag and Drop auf einen Text

essay

Freitextfrage

gapselect

Lückentextauswahl

match

Zuordnungsfrage

_(Fortsetzung nächste Seite)_

**598** 13 Fragenkataloge in Moodle

**Tabelle 13.3** Moodle-XML-Fragetypen _(Fortsetzung)_

Fragetyp-Attribut

Moodle-Fragetyp

multichoice

Multiple Choice-Frage

numerical

Numerische Frage

randomsamatch

Zufällige Kurzantwortfragen

shortanswer

Kurzantwort-Frage

truefalse

Wahr/Falsch-Aufgabe

**Export der „zufälligen Kurzantwort-Fragen“**

Der Export _zufällige Kurzantwort-Fragen_ ist im Grunde genommen nicht möglich.

Dieser „Fragentypus“ stellt streng genommen lediglich eine Vorgabe dar, wie bereits vorhandene Kurzantwort-Fragen zu gemeinsamen Auswahlfragen

zusammengestellt werden. Der Export bzw. der Import einer solchen Frage ist also nur sinnvoll, wenn auch die Kurzantwortfragen der Kategorie exportiert und diese ebenfalls beim Import in einen anderen Fragenkatalog berücksichtigt werden. Zumindest muss im Ziel des Imports ein ausreichender Pool an

Kurzantwort fragen vorhanden sein.

■

Erinnert man sich an die Struktur der Pflichtelemente einer Fragendeklaration, so fallen sofort drei Felder auf:

Fragentitel <name>

Fragetext <questiontext>

Erreichbare Punktzahl <defaultgrade>

Darüber hinaus – wenngleich auch kein Pflichtelement – ist ein allgemeines Feedback Teil jeder Fragestellung geworden. Das XML-Element dafür heißt <generalfeedback>. Bis auf die erreichbare Punktzahl werden die drei Elemente noch um weitere Elemente ergänzt:

<text> enthält den eigentlichen Inhalt des Elements, wie er dargestellt wird. Es sind zudem Attribute für die Elemente zu beachten: Die Eingaben in die Moodle-Oberfläche werden in der Regel im HTML-Format vorgenommen, auch dann, wenn man selbst die Eingaben nicht im HTML-Modus des Editors vornimmt. Beim Element <questiontext> und <generalfeedback> wird deswegen das Attribut _format=“html“_ gesetzt.

Mit XML lassen sich sogar Bilder transportieren. Allerdings ist es ohne den Bezug auf ein Dateisystem oder ohne eine feste Verzeichnisstruktur (wie sie in einem ZIP-Archiv darstellbar ist) nicht möglich, auf eine externe Datei zu verweisen. Auch in der XML-Datei wird keine externe Datei aufgerufen. Dafür wird jedes Bild direkt, aber codiert nach dem Standard _base64,_ 4 vollständig in die XML-Datei geschrieben. In einem Texteditor betrachtet, kann also eine sehr große Datei mit scheinbar wirrem Inhalt entstehen.

4 base64 ist ein schon sehr alter Standard, der für die Übertragung von Binärdateien (ausführbare Programme, Bilder, Audio- und Videodaten etc.) über das Internet entwickelt wurde. Das Internet ist grundsätzlich jedoch in der Urfassung nur für die Übermittlung von reinem Text vorgesehen gewesen. base64 wandelt also jeweils 7 Bit in ein druckbares Zeichen um. Auf der Seite des Empfängers werden diese Daten wieder zurückgewandelt und das eigentliche Bild (etc.) wiederhergestellt.

13.5 Dateiformate für den Fragen-Import und -Export

**599**

<file name=”philippsburg.png” encoding=”base64”>

Der Inhalt dieses Elements wird bei der Betrachtung im Editor ungefähr so aussehen (sehr kleiner Auszug):

…iVBORw0KGgoAAAANSUhEUgAAAjcAAAF5CAIAAADs8Jx4AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAAB3RJ

TUUH5AQDCw83lUSsOwAAIABJREFUeNpsvVuSJcuxKwZ4ZDXPvdL8J6MPzeCORhLP7pXu0AfgsYoykWa 0zd3VVasyI/wBB+D8P/…

Betrachtet man Bild 13.94 so fällt in Zeile 389 ein <text>-Element auf. Der Inhalt wird mit einem eigenartigen Tag eingeleitet, der einem Kommentarelement ähnlich erscheint:

<![CDATA[ ... ]]>. Der durch drei Punkte vereinfacht symbolisierte Bereich enthält an dieser Stelle reinen HTML-Code. CDATA veranlasst Moodle dazu, den darin enthaltenen Inhalt nicht als XML-Code auszuwerten und den Inhalt 1:1 an eine weiterverarbeitende Instanz im Programm zu übergeben. In der Tat interpretiert der XML-Parser in Moodle also den Inhalt des CDATA-Elements wie einen Kommentar und ignoriert ihn zunächst, ohne diesen jedoch zu verwerfen.

Weitere Elemente (Auswahl) zeigt die Tabelle 13.4:

**Tabelle 13.4** Moodle-XML-Elemente (Auszug)

Element

Bedeutung

<question>

Gesamt-Container für eine Frage inkl. aller Teilelemente

<name>

Fragentitel

<text>

Textinhalt verschiedener Elemente wie <feedback> oder

<questiontext>

<generalfeedback>

Allgemeines Feedback (unabhängig vom Ergebnis der Antwort)

<defaultgrade>

Standardbewertung (Punktzahl)

<penalty>

Abzugsfaktor bei mehreren Versuchen

<hidden>

Verborgene Frage

<idnumber>

ID der Frage (sofern vergeben)

<shuffleanswers>

1 = Antwortoptionen mischen

0 = Antwortoptionen nicht mischen

<correctfeedback>

Allgemeines Feedback bei vollständig richtiger Antwort

<partiallycorrectfeedback> Allgemeines Feedback bei teilweise richtiger Antwort

<incorrectfeedback>

Allgemeines Feedback bei unrichtiger Antwort

<file>

Inhalt einer Datei im base64-Format

<drag>

Container für ein bewegliches Element

<no>

Nummer des beweglichen Elements

<noofdrags>

Maximale Zahl der Verwendung bei der Ablage im Zielbild

<coords>

Koordinaten der markanten Punkte einer Ablagezone sowie Radius

bzw. Höhen-/Breitendefinitionen (in Bildpunkten)

<shape>

Form der Ablagezone (circle, rectangle, polygon)

<choice>

Zugeordnete Nummer des beweglichen Elements

_(Fortsetzung nächste Seite)_

![Image 661](index-623_1.png)

**600** 13 Fragenkataloge in Moodle

**Tabelle 13.4** Moodle-XML-Elemente (Auszug) _(Fortsetzung)_

Element

Bedeutung

<quiz>

Haupt-Element einer Frage bzw. Fragesammlung

<drop>

Ablagezone für Drag-and-Drop-Aufgaben

<questiontext>

Container-Element für die eigentliche Fragestellung

<answernumbering>

Form der Antwortnummerierung (z. B.: „123“ für numerisches

Format oder „ABC“ für große Buchstaben als Nummernformat)

<answer fraction=“100“>

Bei Wahr/Falsch-Fragen: richtige Antwort

<answer fraction=”0”>

Bei Wahr/Falsch-Fragen: falsche Antwort

<answer>

Antwort-Element – enthält meist ein <text>-Element

<subquestion>

Container-Element für zusammengehörige Paare bei Zuordnungs-

fragen

**Bild 13.94** Ein Blick in einen – sehr kleinen – Ausschnitt einer Moodle-XML-Datei, in die verschiedene Fragen einer Kategorie exportiert wurden.

**13.5.4■XHTML-Format**

Das XHMTL-Format wurde ursprünglich im Webdesign eingesetzt. Es war ein Versuch, eine Harmonisierung der verschiedenen „Dialekte“ in der HTML-Welt zu erreichen. Durch die Kombination aus Standard-HTML-Elementen und zusätzlichen – auf die Anwendung bezogenen – XML-Elementen versuchte man auch in Moodle, eine systemunabhängige Beschreibungssprache zu etablieren. XHTML hat heute im Webdesign eine untergeordnete Bedeutung und wird hier nur der Vollständigkeit wegen erwähnt.

![Image 662](index-624_1.jpg)

13.5 Dateiformate für den Fragen-Import und -Export

**601**

**Moodle XML ist am flexibelsten verwendbar!**

Das universellste Dateiformat für den Austausch von Fragen und Fragenkatalogen zwischen Moodle-Systemen ist zweifellos Moodle XML. AIKEN und GIFT zeichnen sich durch eine sehr einfache Syntax aus, sind jedoch nur für wenige Fragetypen geeignet. XHTML gilt als veraltet.

■

**Bild 13.95** XHTML ist im Grunde genommen reines HTML (und CSS), wobei sich die Syntax der HTML-Elemente an die von XML anlehnt. Die XHTML-Technologie wird in der Praxis des Webdesigns jedoch kaum noch verwendet.


# 14 Lernzielkontrollen und Prüfungen

Die Feststellung der erbrachten Leistungen und deren Bewertung ist ein besonders anspruchsvolles und sensibles Thema. Es werden sowohl Fragen der Chancengleichheit als auch der rechtlich korrekten Durchführung einer Prüfung und des Datenschutzes berührt.

Moodle bietet verschiedene Optionen, um Prüfungen mit angemessenen Schwierigkeitsgraden zu gestalten, dabei die gebotene Fairness zu wahren und zudem Betrugsversuche auszuschließen. Das Kapitel behandelt deswegen nicht nur die Gestaltungsmöglichkeiten aussagekräftiger Fragenkataloge und die Formulierung von Prüfungen, sondern auch die Einschränkungen des Zugriffs auf die Prüfungsfragen durch zeitliche Grenzen, einen ge -

schützten IP-Adressraum bis hin zur Begrenzung auf die Verwendung eines bestimmten Webbrowsers. Hier wird der Safe Exam Browser (SEB) vorgestellt, eine Entwicklung der ETH Zürich1 zur sicheren Durchführung von Prüfungen. Ein sehr ausgereiftes Konzept auf dieser Basis ist seit vielen Jahren an der Alpen-Adria-Universität in Klagenfurt im Einsatz.

**■**

**■ 14.1■Kontrollübungen in Lektionen**

Lektionen sind eine ausgesprochen vielseitige Aktivität in Moodle. Neben den Inhaltsseiten lassen sich auch Fragenseiten in die Lektion einbauen. Dabei sind nur die folgenden Fragentypen vorgesehen:

Freitext

Kurzantwort

Multiple Choice

Numerisch

Wahr/Falsch

Zuordnung

Die Kontrollfragen sind recht einfach gestaltet, dienen aber durchaus der Motivation beim Lernen.

1 ETH = Eidgenössische Technische Hochschule

**604** 14 Lernzielkontrollen und Prüfungen

**■**

**■ 14.2■ Gestaltung elektronischer Prüfungs-**

**umgebungen**

Prüfungen sind – nicht nur auf akademischem Niveau – ein sehr sensibles Thema. Es geht nicht alleine darum, Fachwissen durch geschickte Fragestellungen zu überprüfen und zu bewerten. Es geht auch um Chancengleichheit und um Rechtssicherheit.

**■**

**■ 14.3■Klassische Prüfungen**

Der Ablauf einer klassischen Prüfung ist in einem großen Umfang von Kontrolle und Über-wachung geprägt. Damit wird rechtliche Sicherheit erreicht, die letztlich die Voraussetzung ist, um Prüfungsergebnisse auch international anzuerkennen.

Damit eine Prüfung tatsächlich als aussagekräftig gewertet werden kann, müssen folgende Faktoren gegeben sein:

Die Prüfung muss in Umfang und Schwierigkeitsgrad dem angestrebten fachlichen Niveau entsprechen.

Die Prüfungsteilnehmerinnen und -teilnehmer müssen sicher identifiziert werden.

Die Verwendung unzulässiger Hilfsmittel muss ausgeschlossen sein.

Absprachen zwischen den Kandidatinnen und Kandidaten müssen zuverlässig unterbunden werden.

Fremdhilfe muss ausgeschlossen sein.

Die vorgegebenen Bearbeitungszeiten sind einzuhalten.

Im Normalfall wird eine solche Prüfung in einem geschlossenen Lehrsaal durchgeführt, wobei entsprechend der Zahl der Teilnehmerinnen und Teilnehmer ausreichend viele Auf-sichtskräfte zugegen sind. Sind die Kandidatinnen und Kandidaten den aufsichtführenden Personen nicht persönlich eindeutig bekannt, dann prüfen sie die Identitäten beispielsweise durch persönliche Vergleiche der Studien- und Personalausweise.

Damit ist bereits die Identitätskontrolle bei rein elektronischen Fernprüfungen ein rechtlich relevantes Problem. Lösungsansätze, die jedoch nicht wirklich zuverlässige Aussagekraft bieten, wären ein Webcam-Check und ein Gesichtsvergleich mit einem vorliegenden Bild (Studierendenausweis, Moodle-Profilfoto etc.). Technisch realisierbar wäre auch die automatische Auswertung biometrischer Erkennungsmerkmale (Iris-Scan, Fingerprint etc.).

Dies müsste im Einzelfall jedoch datenschutzrechtlich überprüft und legitimiert werden.

Schwierig bei rein elektronischen Prüfungen außerhalb kontrollierbarer Örtlichkeiten ist auch, Betrugsversuche zu erkennen und zu verhindern. Selbst in überwachten Umgebungen gibt es immer wieder Betrugsversuche, die zur nicht ausreichenden Bewertung einer Prüfung führen müssen. Lehrende können gewiss eine Reihe „kreativer“ Beispiele benennen:

Der Klassiker: Spickzettel im Toilettenpapier („Nachschlagen“ beim WC-Gang)

Gefälschte Etiketten auf Getränkeflaschen

14.4 Die Aktivität „Test“

**605**

Spickzettel im Uhrenarmband oder in der Gürtelschnalle

Spickzettel im Strumpfband uvm.

Insbesondere die letzten Beispiele zeigen die Notwendigkeit eines gewissen personellen Aufwands zur Prüfungsaufsicht, wobei das Personal mit gemischten Geschlechtern zu wählen ist.

Betrugsversuche sind grundsätzlich anzunehmen, wenngleich natürlich nicht grundsätzlich einzelnen Kandidatinnen und Kandidaten zu unterstellen. Diesen Fakt zu ignorieren würde jedoch zur Entwertung des Prüfungsergebnisses und damit letztlich für die (mehr-heitlich) ehrlichen Absolventen zum Nachteil führen.

**Strittige Notlösung**

In Zeiten der Kontakteinschränkungen infolge der COVID-19-Pandemie im

Frühjahr 2020 wurde in den Kreisen Lehrender eine Fernprüfung über das

Moodle-System besprochen. Dies ist technisch möglich und kann in einer

geschlossenen lokalen Umgebung auch rechtssicher umgesetzt werden.

Während der Pandemiezeit wurde jedoch überlegt, Prüfungen aus dem Home-

Office der Lernenden anzuerkennen. Dabei sollte ein permanenter Zugriff auf die Webcam (beispielsweise über Skype oder ein Virtual Classroom-System) aufgebaut werden, welcher eine Beobachtung der Kandidatinnen und Kandidaten gestattet. Das umfasste auch die Vereinbarung eines gelegentlichen Kameraschwenks, um die Anwesenheit weiterer Personen und die Verwendung

unerlaubter Hilfsmittel auszuschließen.

■

Elektronische Fernprüfungen sind jedoch grundsätzlich möglich, wobei allerdings eine ver-lässliche Aufsicht zu gewährleisten ist. Damit ist es denkbar, erkrankte Kandidatinnen und Kandidaten auch bei einem Klinik- oder Reha-Aufenthalt zu prüfen. Von besonderer Bedeutung ist dieses Prinzip allerdings bei Prüfungen von Strafgefangenen während ihres Gefäng-nisaufenthaltes. Das ist keinesfalls abwegig und wird vereinzelt (analog) durchgeführt: Voll-zugsbeamte übernehmen hier die Aufsicht.

Insgesamt haben Fernprüfungen eine lange Tradition. So arbeitet beispielsweise die Fernuniversität in Hagen weltweit mit anderen Hochschulen zusammen und mietet dort Prüfungsräume sowie Aufsichtspersonal an. Die Prüfungsaufgaben werden in versiegelten Umschlägen geliefert und erst unmittelbar vor der Prüfung geöffnet. Unter vergleichbaren Bedingungen lassen sich auch elektronisch abgestützte Prüfungen durchführen.

**■**

**■ 14.4■Die Aktivität „Test“**

Moodle ist eine Lernplattform, die auch zur Durchführung von Lernzielkontrollen und Prüfungen eingesetzt werden kann. Hierzu wird die Aktivität _Test_ verwendet. Diese wird zunächst einmal eingerichtet, wobei verschiedene wichtige Entscheidungen zu treffen sind, bevor noch die erste Frage gestellt wird. Die zeitliche Befristung, die grundsätzlich auch bei

![Image 663](index-629_1.png)

![Image 664](index-629_2.png)

**606** 14 Lernzielkontrollen und Prüfungen

anderen Aktivitäten konfigurierbar ist, bekommt allerdings bei der Planung einer Prüfung eine besondere Bedeutung. Das dafür vorzusehende Zeitfenster sollte nicht zu eng bemessen sein. Es muss grundsätzlich mit Komplikationen gerechnet werden. Dies können sein:

Probleme bei der Raumbelegung: Der reservierte Prüfungsraum wird nicht rechtzeitig verfügbar.

Verzögerungen beim Identitätscheck.

Technische Probleme (Netzwerkverbindung, Probleme mit einzelnen Rechnern, mögliche Störungen oder Falschkonfigurationen im Moodle-System).

Nicht zuletzt kann eine umfangreiche Prüfung in mehreren Durchgängen durchgeführt werden. Die Prüfungsdauer wird jedoch grundsätzlich auf die exakt eingestellte Zeit begrenzt.

**Bild 14.1** Die Aktivität „Test“ wird zunächst wie jede gewöhnliche Aktivität eingerichtet. In der Detailkonfiguration sind jedoch einige wichtige zusätzliche Einstellungen vorzunehmen.

**Bild 14.2** Das Prüfungszeitfenster wird durch die Testöffnung und eine zeitliche Begrenzung festgelegt. Die Prüfung selbst wird zeitlich auf die Minute genau begrenzt.

14.4 Die Aktivität „Test“

**607**

**14.4.1■Bewertung der Prüfung**

Die Moodle-Administration kann Bewertungskategorien festsetzen, welche Lehrende letztlich den Prüfungen in ihren Kursen zuweisen können. Diese Kategorien haben den Sinn, verschiedene Bewertungen in einem Kontext zusammenzuführen. In den meisten Fällen wird die Standardeinstellung „Nicht kategorisiert“ verwendet. Andere Einstellungen müssen von der Moodle-Administration ausdrücklich (und systemübergreifend gültig) festgelegt und freigegeben werden.

**Bewertungskategorien sind Chefsache**

Die Deklaration von Bewertungskategorien obliegt der Moodle-Administration.

Die Einstellungen werden mit den entsprechenden Administrationsrechten in der Website-Administration vorgenommen:

_Zusatzoptionen – Bewertungen – Bewertungskategorieeinstellungen_

Darüber hinaus lassen sich u. a. Bewertungsskalen und Notenstufen festlegen.

■

Die _Bestehensgrenze_ wird auf einen Wert von 0 bis 10 festgelegt. Dabei sind realistische Grenzen von 5 bis 7,5 üblich, was einem Mindesterfolg von 50 % bis 75 % der Punktzahl entspricht. Es kann aber ebenso eine _Bestehensgrenze_ von 2 (20 %) festgelegt werden. Derartige Bewertungen stellt man bei Prüfungen ein, die vor allem einen hohen Stressfaktor haben und in ihrem Volumen grundsätzlich nicht in der gegebenen Zeit zu bewältigen sind.

Auch die Zahl der Versuche ist relevant. Sind aber mehrere Versuche zulässig, kann davon ausgegangen werden, dass hier verschiedene Ergebnisse erzielt werden. Die Fragen werden in der Regel völlig neu zusammengestellt, wenn der Auswahlpool groß genug ist. Für die Gesamtbeurteilung stellt sich nun die Frage, welcher der Versuche grundsätzlich zu bewerten ist. Es gibt hier vier Möglichkeiten:

Es wird grundsätzlich der erste Versuch bewertet. Hier obliegt es den Lehrenden, eventuell bessere spätere Versuche zu berücksichtigen.

Es wird grundsätzlich der letzte Versuch bewertet. Dies ist eine gängige Praxis. Entscheiden sich Studierende, eine (bereits bestandene) Klausur zu wiederholen, um im Idealfall ihr Ergebnis zu verbessern, wird der erste Versuch verworfen und es wird ein weiterer Antritt notiert. Das Risiko des Nicht-Bestehens ist damit groß.

Es wird der Durchschnitt aller Versuche bewertet.

Es wird der beste Versuch bewertet.

In einer regulären Klausur wird hier in der Regel nur ein Versuch gestattet. Zwar sind Wiederholungen nicht ausreichend bewerteter Arbeiten möglich, jedoch wird die Anzahl der möglichen Antritte begrenzt. Im Fall einer technischen Störung kann es jedoch passieren, dass ein Versuch abläuft und die Kandidatin oder der Kandidat die Arbeit nicht korrekt abgeben kann. In diesem Fall können Lehrende den Versuch aus dem System löschen oder in Teilen neu bewerten. Das ist individuell für jede Teilnehmerin und jeden Teilnehmer möglich (vgl. Abschnitt 14.4.5.3).

![Image 665](index-631_1.png)

![Image 666](index-631_2.png)

**608** 14 Lernzielkontrollen und Prüfungen

**Bild 14.3** Ab 50 % der erreichten Punktzahl ist dieser Test bestanden.

**Bild 14.4** Die Fragenanordnung sollte so gewählt werden, dass nur eine einzige Frage pro Bild-schirmseite zu sehen ist. Das kommt der Konzentration der Kandidaten zugute.

Mit der Konfiguration der Prüfung wird auch festgelegt, welches Feedback die Kandidatinnen und Kandidaten zu welchem Zeitpunkt bekommen. In einer rechtlich relevanten Abschlussprüfung wird natürlich nicht unmittelbar nach der Beantwortung einer Frage ein Feedback gegeben. Das ist schon gar nicht dann sinnvoll, wenn noch die Möglichkeit der Korrektur besteht. Bei (Präsenz-)Unterricht begleitenden Kontrollfragen kann dies allerdings gewünscht sein, weil die Fragen an dieser Stelle als eine zeitnahe Reflexion des Stoffs zu verstehen sind und das Feedback somit der Aufmerksamkeit zugutekommt bzw. zeitnah Verständnisfragen im Plenum provoziert.

Wie angedeutet, ist die eindeutige Identifikation der Kandidatinnen und Kandidaten für eine Prüfung von großer rechtlicher Relevanz. Moodle kann hier unterstützend wirksam sein, wenn das Profilbild während der Prüfung für die Aufsicht führenden Personen neben den Fragestellungen sichtbar ist. Das ist technisch möglich und kann wahlweise mit einem kleinen oder großen Bild umgesetzt werden. Das Bild selbst wird direkt bei der Navigation

![Image 667](index-632_1.png)

![Image 668](index-632_2.png)

14.4 Die Aktivität „Test“

**609**

platziert und nimmt keinen Platz ein, der für die Bearbeitung der Frage benötigt wird. Dennoch ist es rechtlich schwierig, auf ein Profilbild im Moodle-System zu bestehen. Hier handelt es sich um persönliche Daten, die in der Regel auf freiwilliger Basis in das System hochgeladen werden.

**Bild 14.5** Nichts ist spannender als das Ergebnis einer soeben geschriebenen Prüfung. Wie viel Feedback unmittelbar nach der Abgabe oder gar während des laufenden Versuchs gegeben wird, kann von den Lehrenden gezielt eingestellt werden.

**Bild 14.6** Das Nutzerbild kann die Identitätsprüfung während einer elektronischen Klausur erleichtern. Die verpflichtende Bereitstellung eines eindeutigen Personenfotos in das Moodle-System wird allerdings aus rechtlicher Perspektive zu diskutieren sein.

![Image 669](index-633_1.png)

**610** 14 Lernzielkontrollen und Prüfungen

**Bild 14.7** 

Das Moodle-Profilfoto in der Fragennavigation erleichtert

die Wiedererkennung der Teilnehmerin oder des Teil-

nehmers während einer Prüfung. Allerdings muss

man auch mit anonymisierten Abbildungen rechnen,

wie es hier gezeigt wird. Dann muss grundsätzlich der

Studierendenausweis geprüft werden.

**14.4.2■Begrenzung auf bestimmte Netzwerkbereiche**

Es wurde bereits angesprochen: Betrugsversuche gehören im Prüfungsalltag zum Tagesge-schäft. Es ist dabei zwar nur eine Minderheit, die ihre Chance sucht, das Ergebnis auf unlau-tere Weise zu manipulieren, jedoch entwertet allein die potenzielle Möglichkeit, dass die Ergebnisse gefälscht werden könnten,2 die Qualität der Prüfung und des gesamten Studien-gangs. Um das Sicherheitsniveau zu steigern, bietet Moodle bereits einige recht wirksame

„Bordwerkzeuge“.

So bietet Moodle die Möglichkeit, den Zugriff auf die Prüfung mit einem Kennwort zu schützen. Dieses Kennwort wird zweckmäßiger Weise erst mit dem Beginn der Prüfung kommuniziert und ist damit nur den im Saal anwesenden Teilnehmerinnen und Teilnehmern bekannt. Wenn ein konsequentes Handy-Verbot durchgesetzt wird und weitere Sicherheits-einstellungen aktiviert werden, ist lediglich der berühmte „WC-Gang“ eine potenzielle Sicherheitslücke, über die das Passwort nach außen verbreitet werden kann.

Damit besteht das Risiko, dass sich eine weitere Person außerhalb des überwachten Prüfungssaals mit fremder Identität einloggt und die Prüfung stellvertretend schreibt. Doch auch dieses Risiko lässt sich einschränken, wenn man den Prüfungssaal mit einer kabel-basierten Netzwerk-Infrastruktur ausrüstet. Diese lässt sich auf einen eng umrissenen Bereich von IP-Adressen3 konfigurieren. Natürlich ist das technisch recht aufwendig und vor allem ziemlich teuer! Wesentlich preiswerter sind WLAN-Infrastrukturen, die heute nahezu an jedem Universitäts- oder Fachhochschul-Campus sowie an den meisten Schulen vorhanden sind. Es empfiehlt sich jedoch, speziell in Prüfungsräumen ein eigenes WLAN zu betreiben, um die Überlastung des Netzes durch die reguläre Nutzung zu vermeiden.

Ein WLAN ist natürlich ein offenes Medium. Grundsätzlich kann also niemand ausschlie-ßen, dass direkt nebenan vom Prüfungssaal ein „Experte“ mit einem Laptop sitzt, sich mit falschen Zugangsdaten am Moodle-System anmeldet und die Prüfung für eine Teilnehmerin 2 Tatsächlich ist die Form des Konjunktivs mit Absicht gewählt, denn Sicherheitslücken werden meist denen nachteilig ausgelegt, die einen sehr guten Erfolg durch viel persönlichen Fleiß erzielt haben. Prüfungssicherheit bedeutet vor allem, die Anerkennung ehrlich erworbener Leistungen zu schützen.

3 IP steht für Internet Protocol. Tatsächlich beschreibt diese Abkürzung das Verfahren, mit dem Datenpakete über das Internet übertragen werden. Das gleiche Protokoll wird allerdings auch in einem lokalen Netzwerk verwendet.

Die IP-Adresse ist in einem solchen System die Adresse des Computers.

14.4 Die Aktivität „Test“

**611**

oder einen Teilnehmer „übernimmt“. Das ist grundsätzlich zunächst einmal möglich! Es ist aber auch selbst in diesen einfachen Infrastrukturen möglich, Betrügern das Leben schwer zu machen. Auf jedem Fall ist es zudem möglich, einen Betrug im Nachhinein zu beweisen.

**Form der IP-Adresse**

Mit der Beschränkung auf bestimmte IP-Adressen kann der Zugriff auf den

Test lediglich auf Computer eingeschränkt werden, denen eine passende

Adresse zugewiesen wurde. Hierbei können – getrennt durch Kommata –

einzelne Adressen eingestellt werden. Es ist zudem möglich, Teiladressen festzulegen, um den Zugang zur Prüfung auf Rechner innerhalb eines Sub-netzes zu beschränken. Der Teil der Hostadressen wird nicht geschrieben.

Möglich ist auch eine Schreibweise in diesem Format: 192.168.0.0/24.

■

**14.4.2.1■Parallelanmeldungen vermeiden**

Die _Moodle-Administration_ kann die Zahl der gleichzeitigen Anmeldungen in das Moodle-System pauschal begrenzen. Das passiert in der _Website-Administration_ unter _Plugins –_

_Authentifizierung – Übersicht_. Dort ist ein Bereich _Grundeinstellungen_ zu finden. Hier muss der Wert bei _Gleichzeitige Anmeldungen begrenzen_ auf 1 gesetzt werden.

Das funktioniert allerdings nur bei Authentifizierungsverfahren, die direkt im Moodle-System umgesetzt werden. Single Sign On (SSO)-Verfahren werden durch die Einstellungen in Moodle nicht berührt! Hier müssen in den Authentifizierungsservern Lösungen gefunden werden.

Erfolgt nun die offizielle Anmeldung an das Moodle-System durch die Prüfungskandidatinnen und -kandidaten im Prüfungssaal, funktioniert das System wie immer einwandfrei.

Versucht nun eine weitere Person, sich mit einem bereits aktiven Account einzuloggen, so wird auch dies gelingen. Allerdings wird die Verbindung zum Computer, der das erste Login herstellte, unterbrochen. Möglicherweise fällt dies dem Aufsicht führenden Personal auf.

![Image 670](index-635_1.jpg)

**612** 14 Lernzielkontrollen und Prüfungen

**Bild 14.8** Wenn versucht wird, sich mit einem zweiten Rechner unter Verwendung der gleichen Zugangsdaten, in Moodle anzumelden, werden bestehende Sitzungen ungültig und fordern eine erneute Anmeldung. Voraussetzung: Die gleichzeitige Anmeldung ist auf „1“ begrenzt.

**14.4.2.2■Vollbild-Modus erzwingen**

Die eben gezeigte Einschränkung ist nicht in der Lage, grundsätzlich die Übergabe einer Prüfung an eine illegale Hilfskraft zu unterbinden. Es bewirkt, dass dem betrügerisch arbeitenden Kandidaten Zeit verloren geht und dass durch ungewöhnliche Bewegung am Bildschirm Auffälligkeiten durch die Aufsichten erkannt werden. Eine Kommunikation – zum Beispiel via Chat – ist also grundsätzlich nicht auszuschließen.

Das kann auch die Einstellung _Vollbild-Popup mit JavaScript-Sicherheit_ im Feld _Browsersicher-heit_ der Test-Konfiguration nicht erzwingen. Etwas effektiver ist da der _Safe Exam Browser_, auf den in Abschnitt 14.5 näher eingegangen wird. Wer Unterlagen auf der eigenen Festplatte nachschlagen oder über ein zweites Browser-Fenster im Internet recherchieren möchte, wird sich von der Einschränkung des Vollbild-Popups nicht aufhalten lassen.

Das Vollbild-Popup zeigt eine reine Browser-Oberfläche ohne jegliche Menüs. Zudem werden nur die für die Prüfung erforderlichen Elemente in Moodle dargestellt. Der Klick in den Chat oder die Suche im Internet erfordert also grundsätzlich den Wechsel des Fensters.

**Klare Vereinbarungen sind erforderlich!**

Aufsichtführende Personen dürfen auch bei einem Verdacht nicht einfach so in die Tasten eines privaten Computers greifen. Allerdings kann vor Beginn der Prüfung eine Vereinbarung getroffen werden, deren Missachtung pauschal als Betrugsversuch zu werten ist. Zu dieser Vereinbarung muss gehören:

![Image 671](index-636_1.png)

![Image 672](index-636_2.png)

14.4 Die Aktivität „Test“

**613**

� Es darf kein Programmfenster mit Ausnahme des für diese Moodle-Sitzung benötigten Browsers geöffnet sein.

� Es darf kein Programm geöffnet sein, was nicht einem ausdrücklich zuge-lassenen Hilfsmittel entspricht.

� Es darf kein Messenger aktiv sein (Skype etc.), auch nicht minimiert im Systemtray.

� Auf Aufforderung durch die Aufsicht haben die Kandidatinnen und Kandidaten mit der Tastenkombination [Alt]-[Tab] die geöffneten Fenster zu präsentieren.

■

**Bild 14.9** Zugriffsbeschränkungen auf die Prüfung können durch ein Kennwort, durch Beschränkungen des IP-Adressbereichs und durch besondere Browsertypen festgelegt werden. Einen vollkom-menen Schutz gegen Betrugsversuche bieten sie allerdings nicht.

**Bild 14.10** Das Vollbild-Popup, welches in der Standard-Installation eines Moodle-Systems eingestellt werden kann, zwingt zum Zugriff auf andere Programmfenster und damit zu einem deutlich sichtbaren und möglicherweise zeitaufwendigen Wechsel des Programmfensters. Sicherheit gegen Betrug bietet es nicht.

![Image 673](index-637_1.jpg)

**614** 14 Lernzielkontrollen und Prüfungen

**Bild 14.11** Dem Vollbild fehlen sämtliche Steuerelemente des Browsers und weitere Menüelemente.

**14.4.2.3■Nachträgliches Betrugsindiz**

Alle Anmeldungen im System und Zugriffe auf Moodle-Ressourcen werden in den Protollen einer jeden Benutzerin und eines jeden Benutzers gespeichert. Tauchen in diesen Protokollen mehrere Zugriffe auf die Prüfung unter gleichem Benutzerzugang jedoch mit verschiedenen IP-Adressen auf, so kann dies auf einen externen Helfer hinweisen. Besonders dann, wenn nur eine einzige Moodle-Sitzung aktiv sein kann, werden die Log-Daten interessante Hinweise bieten: Jeder Identitätswechsel erfordert nämlich eine neue Anmeldung am System. Auch die Logins werden protokolliert und dabei zusätzlich die IP-Adressen gespeichert.

Um den Schein der Prüfungsteilnahme zu wahren, müssen auch betrügerische Kandidatinnen und Kandidaten in der Prüfung aktiv sein. Wechseln sie die Frage nachdem sich ein Helfer mit ihrem Account eingeloggt hat, wird die Sitzung ungültig und es wird eine erneute Anmeldung erforderlich. Dies ist am Bildschirm deutlich erkennbar und es besteht das Risiko, dass das Aufsichtspersonal dies bemerkt. In den Logdateien ist dieses Wechselspiel jedoch sehr auffällig. Im Zweifelsfall kann zudem noch tiefer geforscht werden. Die IT-Abteilung hat Zugriff auf die Logdateien des Webservers. Dessen Datenflut ist zwar sehr umfangreich, kann jedoch mit geeigneten Suchfiltern vergleichsweise schnell analysiert werden.

Nicht nachweisbar ist auf diesem Weg die Nutzung unerlaubter Hilfsmittel, wie zum Beispiel der Zugriff auf Unterlagen auf der eigenen Festplatte oder Internet-Recherchen.

![Image 674](index-638_1.png)

14.4 Die Aktivität „Test“

**615**

**Betrug verhindern mit Standardmitteln?**

Es ist tatsächlich möglich, Betrugsversuche technisch mit einer extrem hohen Wirkung zu unterbinden. Das beweist die sichere Prüfungsumgebung (SPU) an der Alpen-Adria-Universität in Klagenfurt. Dahinter steht eine aufwendige Infrastruktur.

Ohne großen technischen Aufwand existieren Schlupflöcher, die eine Durchführung von Betrugsversuchen möglich machen. Betrug absolut zu verschleiern und Spuren zu verwischen, ist jedoch nicht möglich und hier bieten die Server-Systeme mit ihren Protokoll-Dateien eine lückenlose Aufzeichnung der Vorgänge im System.

■

**Bild 14.12** Personen mit einer Teacher-Rolle können in den Benutzerprofilen verschiedene Berichte einsehen. Sehr informativ sind hier die Log-Daten.

![Image 675](index-639_1.png)

**616** 14 Lernzielkontrollen und Prüfungen

**Bild 14.13** Ein nahezu zeitgleicher Zugriff auf ein und dieselbe Prüfung abwechselnd mit mehreren IP-Adressen durch eine scheinbar „einzige“ Person deutet auf eine unerlaubte Manipulation hin.

**14.4.3■Test und Testfragen**

Nach der Konfiguration der Test-Aktivität kann diese noch nicht sofort in einer Prüfung eingesetzt werden. Es fehlt noch die Zuweisung von Fragen in diesen Test. Hier gibt es drei verschiedene Möglichkeiten:

Hinzufügen einzelner Fragen, die mit der Prüfung auch augenblicklich formuliert werden.

Hinzufügen fest gewählter Fragen aus der Fragensammlung.

Hinzufügen zufälliger Fragen aus der Fragensammlung.

Am aufwendigsten ist die Verfassung einzelner Fragen für jeden Test. Diese Option sollte nur in Ausnahmefällen eingesetzt werden, beispielsweise dann, wenn ein aktuelles Themengebiet spontan in den Lehrplan übernommen wurde und ebenfalls in der Prüfung abgefragt werden soll.

![Image 676](index-640_1.png)

14.4 Die Aktivität „Test“

**617**

**Fragenzuordnung**

Die Zuordnung der Fragen startet beim erstmaligen Aufruf des Tests durch die Teacher-Person. Jederzeit kann die Fragenzuordnung im _Einstellungs_-

Block in der _Test-Administration_ unter _Testinhalt bearbeiten_ ergänzt und korrigiert werden.

■

Die _Test-Administration_ ist sehr vielseitig. Die Test-Administration ist nur sichtbar, wenn ein Test im Kurs gewählt wurde. Die Fragenzuordnung kann theoretisch jederzeit verändert werden. Allerdings ist dies nur möglich, solange noch keine Versuche aktiviert wurden.

Änderungen während eines laufenden Prüfungszyklus würden die Chancengleichheit in Frage stellen.

Ist die Fragensammlung ausreichend groß, kann eine bestimmte Zahl von Fragen nach dem Zufallsprinzip aus verschiedenen Kategorien entnommen werden. Hier ist eine Kategorisie-rung der Fragen wichtig, um eine Auswahl möglichst gleicher Schwierigkeitsgrade zu ermöglichen.

**Bild 14.14** Wenn dem Test noch keine Fragen zugewiesen wurden, führt der erste Klick eines Lehrenden zu den erforderlichen Dialogen.

![Image 677](index-641_1.png)

**618** 14 Lernzielkontrollen und Prüfungen

**Bild 14.15** Jederzeit können die Fragen im Test in der Testadministration ergänzt oder verändert werden. Allerdings ist das nur möglich, wenn noch keine Testversuche stattgefunden haben.

**14.4.3.1■Fixierte Prüfung mit gleichen Fragen**

Die gezielte Auswahl von Prüfungsfragen aus einer Fragensammlung gewährleistet absolute Chancengleichheit. Alle Kandidaten bearbeiten die gleichen Fragen. Auch weitere Prüfungen lassen sich vergleichsweise schnell mithilfe einer fertigen Fragensammlung zusammenstellen, aus der die gewünschten Fragen beim Testdesign gezielt gewählt werden. Das Risiko des Abschreibens ist überschaubar und kann durch räumliche Distanz – Belegung jedes zweiten Platzes und jeder zweiten Zeile – deutlich reduziert werden.

**Fragensammlung**

Die Erstellung einer Fragensammlung und deren Zuordnung wurde in einem

eigenen Kapitel ausführlich beschrieben. Die Bewertung nach Schwierigkeitsstufen erfolgt natürlich subjektiv, ist jedoch die mit Gewissheit anspruchs-vollste Aufgabe im Design von Prüfungen.

■

![Image 678](index-642_1.jpg)

![Image 679](index-642_2.png)

14.4 Die Aktivität „Test“

**619**

**Bild 14.16** Die Option _aus der Fragensammlung_ führt zur manuellen Auswahl von Fragen aus einem be -

reits bestehenden Fundus. Alle Prüfungskandidatinnen und -kandidaten bearbeiten die gleiche Prüfung.

**Bild 14.17** Die für den Test gewünschten Fragen werden per Mausklick ausgewählt. Es ist auch möglich, alle Fragen zu selektieren.

![Image 680](index-643_1.png)

**620** 14 Lernzielkontrollen und Prüfungen

**Bild 14.18** Nach der Auswahl der Fragen kann deren Bewertung, deren Reihenfolge der Erscheinung – falls diese nicht zufällig erfolgen soll – im Detail eingestellt werden. Fragen können zudem entfernt und ergänzt werden.

**14.4.3.2■Prüfung mit zufälligen Fragstellungen**

Eine sehr beliebte Form der Prüfungsgestaltung ist die Verwendung zufällig aus einer Sammlung gewählter Fragen. Das erfordert eine umfassende Vorbereitung, bietet jedoch den Vorteil einer spontanen Wiederholbarkeit auch mit neuen Fragen. Darüber hinaus verringert eine zufällige Wahl von Fragen das Risiko des Abschreibens. Hier ist es allerdings absolut wichtig, verschiedene Fragensammlungen mit unterschiedlichen Schwierigkeitsstufen anzulegen. Das Kapitel zur Erstellung von Prüfungsfragen hat dies bereits diskutiert.

Aus jeder Fragenkategorie wird dann die Nutzung einer gewissen Anzahl von Fragen festgelegt. Die Anzahl und die Bewertung der jeweiligen Fragenklassen sollten geschickt auf-einander abgestimmt werden. Werden zu viele schwierige Fragen gestellt, deren Bewertung mit einer großen Punktzahl verbunden ist, wird es für die Kandidatinnen und Kandidaten schwierig, mit der Beantwortung einfacher und mittelschwerer Fragen ein ausreichendes oder gar befriedigendes Ergebnis zu erzielen.

**Zufällige Fragenwahl ist ein Sicherheitsgewinn**

Durch die automatische Gestaltung einer Prüfung mit zufälligen Fragen von identischem Niveau wird die Prüfung als solches authentisch. Es ist den

Lernenden damit kaum möglich, eine „Klausurensammlung“ zu veröffentlichen, die gezieltes „Bulimie-Lernen“ mit fertigen Lösungswegen ermöglicht.

■

![Image 681](index-644_1.jpg)

14.4 Die Aktivität „Test“

**621**

Wie Bild 14.20 zeigt, können die Wertigkeiten der Fragen nachträglich angepasst werden.

Schwierige Fragen werden eine höhere Punktzahl erzielen als einfache. Die Punktzahlen lassen sich also an das Niveau der Kandidatinnen und Kandidaten anpassen, um tatsächlich eine aussagekräftige und dem Aufwand gerecht werdende Prüfung zu entwickeln. Bei der Punktezuweisung sollte jedoch stets im Blick behalten werden, dass es auch durchschnittlichen Lernenden möglich sein sollte, mit einem genügenden Ergebnis die Prüfung zu bestehen. Um in den Bereich eines sehr guten Ergebnisses zu gelangen, sollte die Bewertung so bemessen sein, dass zumindest eine schwierige Frage mit voller Punktzahl zu beantworten ist. Auf der anderen Seite sollte die Masse der einfachen und mittelschweren Antworten bei überwiegend richtiger Beantwortung genügen, um ein ausreichendes Ergebnis zu erreichen.4

**Bild 14.19** Es wird die Fragenkategorie gewählt und entschieden, wie viele Fragen aus dieser Kategorie in die Prüfung einfließen sollen.

4 Die Punkteverteilung in Bild 18.20 entspricht nicht diesen Zielsetzungen. Sie dienen der optischen Abgrenzung der verschiedenen Schwierigkeitsgrade in der Illustration. Ein besseres Design würde möglicherweise eine schwierige Frage weniger in dieser Beispielprüfung vorsehen und die einfachen Fragen etwas besser bewerten (zwei oder drei Punkte). Denkbar ist auch, eine größere Anzahl mittelschwerer Fragen zu stellen.

![Image 682](index-645_1.png)

**622** 14 Lernzielkontrollen und Prüfungen

**Bild 14.20** Die Fragen werden in diesem Fall nicht speziell aufgelistet. Es wird auf die Zufallsfrage hingewiesen und in Klammern die Kategorie gesetzt. Die Punktzahl kann auf der rechten Seite detailliert festgelegt werden.

**14.4.4■Prüfung durchführen**

Wenn die administrativen Abläufe erledigt sind, wenn also die Anwesenheit der Kandidatinnen und Kandidaten sowie deren Identitäten überprüft wurden, kann die Prüfung beginnen. Das Zeitfenster ist in der Voreinstellung bereits so gewählt, dass eine gewisse Reserve bei einer Systemstörung oder im Fall einer dringenden Erklärung gegeben ist und eingeräumt werden kann.

Bis zum Beginn der Prüfung kann die Prüfungsleitung den Test versteckt schalten. Es kann so niemand versuchen, den Test vor dem eigentlichen Prüfungsbeginn zu aktivieren. Die Prüfungszeit beginnt erst in dem Augenblick, wenn sich die Kandidatin oder der Kandidat in den Test einschaltet. Dies passiert mit einer ausdrücklichen Willenserklärung: _Test jetzt_ _durchführen_.

Dies ist der Augenblick, ab dem die Zeit zu laufen beginnt, wenn eine Zeitbegrenzung vorgesehen ist.

![Image 683](index-646_1.jpg)

14.4 Die Aktivität „Test“

**623**

**Zeitbegrenzung**

Die zeitliche Begrenzung eines Tests muss ausdrücklich aktiviert werden (vgl.

Bild 14.2). Sonst kann der Test so lange bearbeitet werden, wie die Sitzung der Teilnehmerin bzw. des Teilnehmers in Moodle dauert.

■

**Bild 14.21** Der Test ist aktiviert. Die Bearbeitungszeit beginnt individuell für jede Kandidatin und jeden Kandidaten mit dem Start des Tests.

![Image 684](index-647_1.jpg)

![Image 685](index-647_2.jpg)

**624** 14 Lernzielkontrollen und Prüfungen

**Bild 14.22** In der Navigation ist klar zu erkennen, welche Fragen bereits beantwortet wurden und welche noch offen sind.

**Bild 14.23** Gibt es für die Bearbeitung der Prüfungsaufgaben ein Zeitlimit, so wird der Countdown bis zur automatischen Abgabe in der Navigation angezeigt.

![Image 686](index-648_1.jpg)

14.4 Die Aktivität „Test“

**625**

Die Form der Abgabe einer Arbeit kann von sehr moderat bis streng geregelt festgelegt werden. Die restriktive Variante, die in Verbindung mit einer zeitlichen Begrenzung der Prüfung möglich ist, ist die automatische Abgabe der Prüfung. Der Test wird dann direkt geschlossen. Alle aktuell vorliegenden Antworten werden gespeichert und fließen in die Bewertung mit ein.

Es gibt die Option, eine Nachfrist für die Abgabe einzuräumen. In dieser Zeit können allerdings keine Fragen mehr beantwortet werden. Einigen Lernenden ist es aber wichtig, sich ihre Lösungen noch einmal anzusehen, um sich im Nachhinein darüber Gedanken machen zu können. Bei einer elektronischen Prüfung, wo nach dem Abschluss des Tests auch direktes Feedback gegeben werden kann, ist dies allerdings nicht wirklich nötig.

Eine weitere Option ist der Zwang, die Arbeit vor dem Ablauf des Zeitlimits abgeben zu müssen, damit der Test gewertet wird. Es gibt verschiedene Ansätze, die für und gegen diese Variante sprechen. Für diese Variante sprechen Prüfungsmodalitäten, bei denen die Lernenden mit ihrer Abgabe der Prüfung entscheiden, ob sie diese als Antritt werten lassen wollen oder nicht. Gerne wird dies von Lehrenden jedoch nicht vorgesehen, weil die Art und die Inhalte der Fragestellung somit als Information nach außen dringen können.

Die bevorzugte Variante wird es sein, die Prüfung automatisch mit dem Ablauf der Zeit abzugeben und alle bis dahin beantworteten Fragen in die Wertung einzubeziehen. Als Bekundung des Prüfungsantritts gilt dann beispielsweise der Start des Tests.

**Bild 14.24** Wer sich entschließt, die Prüfung zu beenden, bekommt vor der endgültigen Abgabe eine Zusammenfassung präsentiert. Hier ist zu erkennen, ob womöglich die Bearbeitung einer Frage vergessen wurde.

![Image 687](index-649_1.jpg)

![Image 688](index-649_2.jpg)

**626** 14 Lernzielkontrollen und Prüfungen

**Bild 14.25** Die Abgabe ist rechtsverbindlich und findet deswegen über mehrere Schritte und eine endgültige Bestätigung statt. Danach kann der Versuch nicht mehr bearbeitet werden!

**Bild 14.26** Wenn die Lehrenden dies in den _Überprüfungsoptionen_ bei der Konfiguration des Tests einstellen, können die Lernenden nach der Abgabe sofort ihr Feedback zu den Aufgaben einsehen und erkennen, wo sie eventuell Fehler gemacht haben.

14.4 Die Aktivität „Test“

**627**

**14.4.5■Prüfungsverlauf und Ergebnisberichte**

Für die Lehrenden ist es während einer Prüfung wichtig, das System und dessen Funktion im Blick zu behalten. Aus diesem Personenkreis muss deswegen mindestens eine Kollegin oder ein Kollege die _Test-Administration_ beherrschen.

Dies ist wichtig für den Eingriff im Pannenfall sowie für die direkte Klärung strittiger Fragen bei den Prüfungsergebnissen.

**14.4.5.1■Ergebnisübersicht**

Die meistgestellte Frage unmittelbar nach einer Prüfung zielt auf die Chancen von Bestehen und Nicht-Bestehen ab. Tatsächlich ist es mit dem Moodle-System möglich, bereits unmittelbar nach der Abgabe ein Ergebnis mitzuteilen. Die einzige Ausnahme stellen Prüfungen dar, die mit Freitextaufgaben gestaltet wurden. Diese erfordern grundsätzlich die manuelle Korrektur und Bewertung durch das Lehrpersonal.

Da möglicherweise Reklamationen zu bearbeiten sind und sich die Lehrenden eine eigene Bewertung vorbehalten, kann im Prüfungssaal noch keine rechtlich verbindliche Aussage zum Ergebnis der Prüfung im Einzelfall getroffen werden. Denkbar ist es allerdings, die Tendenz des Gesamtergebnisses zu kommunizieren. Hier bietet Moodle zwei verschiedene Berichtsansichten:

Ein Diagramm

Eine tabellarische Ansicht (Klick auf _Grafikdaten anzeigen_)

Die Darstellungen zeigen die Verteilung der Teilnehmerinnen und Teilnehmer (y-Achse) über die Bewertungsbreite (x-Achse). Auf diese Weise kann sofort erkannt werden, wie groß der Anteil derer ist, die diese Prüfung nicht bestanden haben.

**Mehrere Wege führen zur Statistik**

Es gibt zwei Wege, die Berichte direkt zu erreichen. In einem Fall kann die Lehrkraft im Prüfungsabschnitt des Moodle-Kurses auf den Link _Versuche_ klicken. Dort werden die bereits absolvierten Versuche und deren Teilnehmerinnen und Teilnehmer aufgelistet. Auch die Bewertungsdiagramme sind hier zugänglich.

Der normale Weg führt über die _Test-Administration_. Unter _Ergebnisse_ wird hier die _Bewertung_ gewählt. Detaillierte statistische Auswertungen des Ergebnisses sind ebenfalls in der Test-Administration unter _Ergebnisse – Statistik_ zu finden.

Es ist hier auch möglich, die Statistiken zur weiteren Analyse als CSV-Datei oder in einem gängigen Tabellenformat zu exportieren.

■

![Image 689](index-651_1.png)

![Image 690](index-651_2.png)

**628** 14 Lernzielkontrollen und Prüfungen

**Bild 14.27** Personen mit der Teacher-Rolle haben sehr umfassende Möglichkeiten, die Ergebnisse im Detail zu beobachten. Eine Möglichkeit ist der Klick auf den Link „Versuche“ im Prüfungs- Start-Fenster.

**Bild 14.28** 

Die Bearbeitung der Testinhalte und die Administration der Prüfung

sowie deren Auswertung findet in der Test-Administration statt.

![Image 691](index-652_1.png)

![Image 692](index-652_2.png)

14.4 Die Aktivität „Test“

**629**

**Bild 14.29** Welche Informationen der Bericht umfassen soll, kann eingestellt werden. Während einer Prüfung ist es sinnvoll, die in Bearbeitung befindlichen Versuche zu betrachten, um Rückfragen besser beantworten zu können.

**Bild 14.30** Die Liste ist in der Praxis natürlich bedeutend länger. Die Ergebnisse der einzelnen Kandidatinnen und Kandidaten können direkt untersucht und im Einzelfall auch korrigiert werden.

![Image 693](index-653_1.jpg)

![Image 694](index-653_2.png)

**630** 14 Lernzielkontrollen und Prüfungen

**Bild 14.31** In dieser Simulation gab es nur eine einzige Abgabe. In der Praxis wird hier aber bereits nach dem Test deutlich sichtbar, wie das Ergebnis ausgefallen ist.

**Bild 14.32** Die Werte des Säulendiagramms können auch in einer tabellarischen Ansicht dargestellt werden. Es wird detailliert ersichtlich, wie viele Kandidatinnen und Kandidaten welchen Erfolg erreicht haben.

![Image 695](index-654_1.png)

14.4 Die Aktivität „Test“

**631**

**Bild 14.33** Für eine detaillierte Analyse der Prüfung kann eine Statistik exportiert werden.

**14.4.5.2■Eingriffe in Einzelfälle**

Der zeitliche Ablauf einer Prüfung ist eng getaktet. Die Regeln sind erläutert, die Teilnehmerinnen und Teilnehmer sind motiviert und beginnen ihre Arbeit. Plötzlich gibt es ein Problem: Bei einer Kandidatin oder einem Kandidaten wird der Bildschirm dunkel. Nichts geht mehr, doch im Hintergrund läuft die Zeit unerbittlich weiter.

Eine gut organisierte Prüfungsmannschaft wird Ersatzgeräte vorsehen, die im Fall einer Störung von den Teilnehmerinnen und Teilnehmern zur Fortsetzung der Prüfung genutzt werden können. Das bedeutet aber auch einen zeitlichen Verlust:

Der Fehler tritt auf. Die Kandidatin oder der Kandidat versucht, das Problem zu beheben.

Die Kandidatin bzw. der Kandidat bittet das Aufsichtspersonal um Rat. Die Aufsicht prüft das Problem und kann den Fehler nicht direkt beheben.

Die Aufsicht weist der Kandidatin bzw. dem Kandidaten einen Platz mit einem Ersatzgerät zu. Dieses ist zweckmäßigerweise aufgebaut und bereits gestartet, sodass nur noch eine Anmeldung am Moodle-System erforderlich ist.

Die Kandidatin bzw. der Kandidat wechselt den Platz und meldet sich am Moodle-System an. Dort kann nun am Ersatzgerät die Prüfung fortgesetzt werden.

**632** 14 Lernzielkontrollen und Prüfungen

Das Problem ist nun, dass jeder einzelne dieser Schritte einige Minuten Zeit in Anspruch nimmt, die möglicherweise für das Prüfungsergebnis entscheidend sein kann. Hinzu kommt der Stress durch die unvorhergesehene technische Panne. Nicht zuletzt ist die Kandidatin bzw. der Kandidat durch den Umzug im Prüfungssaal aus dem eigenen Fluss gekommen und muss sich erst wieder in die Prüfung hineinversetzen. Eine solche Panne kann also durchaus fünf bis zehn Minuten der kostbaren Bearbeitungszeit kosten.

**Störungen protokollieren!**

Wie gesehen kann eine nachträgliche Auswertung der Logdateien erfolgen,

um Schummeleien zu enttarnen. Im Fall eines Wechsels des Prüfungsgeräts

wird ebenfalls der Fall eintreten, dass die Prüfung mit zwei Geräten (zwei verschiedenen IP-Adressen) durchgeführt wurde. Eine saubere Dokumentation der Störung schließt in diesem Fall irrtümliche Betrugsverdachtsmomente aus.

■

Eine individuelle Verlängerung der Bearbeitungszeit ist in der _Test-Administration_ als _Nutzeränderung_ vorzunehmen. Hier wird zuerst einmal der betreffende Nutzer bzw. die Nutzerin gewählt, denn nur allein auf diese Teilnehmerin bzw. diesen Teilnehmer beziehen sich die folgenden Einstellungen. So kann die Anzahl der erlaubten Versuche verändert werden.

Im hier gezeigten Fall soll allerdings die Bearbeitungszeit von ursprünglich 60 Minuten auf 90 Minuten verlängert werden. Welcher Zeitwert genau eingestellt wird, hängt vom Grund der Maßnahme ab. Das können sein:

Technische Störung (wie oben beschrieben).

Teilnahme einer beeinträchtigten Person, für die der allgemeine Zeitrahmen einen unzu-mutbaren Nachteil darstellen würde.

Nach dem Speichern wird die Änderung sofort wirksam. Das bedeutet, dass der Countdown auch beim bereits laufenden Versuch einen neuen Wert anzeigt.

**Die Fähigkeit, Zeitlimits zu ignorieren**

Moodle kennt eine besondere Fähigkeit:

_mod/quiz/ignoretimelimits_

Ist diese Fähigkeit auf _erlaubt_ gesetzt, dann würde die damit verbundene Rolle nicht auf die Begrenzung der Bearbeitungsdauer reagieren. Wenn Menschen an der Prüfung teilnehmen, die möglicherweise aufgrund motorischer Einschränkungen durch die knappe Zeit einen Nachteil haben, wäre es möglich, hier einen Ausgleich zu schaffen. Sinnvoller ist allerdings, in diesen Fällen eine Ausnahme durch die _Nutzeränderung_ herzustellen.

■

![Image 696](index-656_1.png)

![Image 697](index-656_2.png)

14.4 Die Aktivität „Test“

**633**

**Bild 14.34** Um die Bearbeitungszeit einer Teilnehmerin oder eines Teilnehmers zu verlängern, muss eine (individuelle) Nutzeränderung in der Test-Administration vorgenommen werden.

**Bild 14.35** Es wird zuerst gezielt die Teilnehmerin oder der Teilnehmer gewählt, dessen Bearbeitungszeit verändert werden soll. Dann wird die Zeitbegrenzung um die ausgefallenen Minuten erhöht. Nach der Speicherung wird das neue Zeitlimit sofort in der Prüfung wirksam.

![Image 698](index-657_1.png)

**634** 14 Lernzielkontrollen und Prüfungen

**Bild 14.36** Die verbleibende Zeit ist nun deutlich mehr als ursprünglich 60 Minuten. Die Anpassung ist auch während eines bereits laufenden Tests möglich.

**14.4.5.3■Ergebniskorrekturen und Zusatzversuche**

Es gibt mindestens zwei Fälle, in denen die Korrektur eines Ergebnisses und gegebenenfalls eine Neubewertung erforderlich sein können.

Ein tatsächlicher Fehler in der Aufgabendeklaration führte zu einer falschen automatischen Bewertung trotz einer fachlich richtigen Antwort.

Freitextaufgaben müssen grundsätzlich manuell bewertet werden.

Im bereits angesprochenen Bereich _Bewertung_ _(Test-Administration – Ergebnisse)_ gibt es eine Liste aller durchgeführten Versuche. Diese Liste kann wie bei einer gängigen Tabellenkalkulation durch einen Klick auf die jeweilige Spaltenüberschrift sortiert werden. Zudem erleichtert der alphabetische Index die Suche nach bestimmten Teilnehmerinnen und Teilnehmern.

Diese Tabelle bietet zunächst verschiedene Möglichkeiten:

den kompletten Versuch der Teilnehmerin bzw. des Teilnehmers überprüfen.

eine einzelne Antwort überprüfen.

Im Fall einer gezielten Reklamation oder einer zu bewertenden Freitextaufgabe wird man die Antwort direkt überprüfen wollen. Dazu klickt man auf den Zahlenwert des Ergebnisses. Um einen Versuch der betreffenden Person zu überprüfen, gibt es sowohl unter deren Namen einen Link als auch die Möglichkeit auf den Zahlenwert der gesamten Bewertung zu klicken.

![Image 699](index-658_1.png)

14.4 Die Aktivität „Test“

**635**

Ebenso in diesem Bereich lassen sich zusätzliche Versuche aktivieren. Ist die Anzahl der möglichen Versuche begrenzt oder bei mehreren möglichen Versuchen mit Punktabzügen sanktioniert, kann im Fall eines begründeten Abbruchs oder Misserfolgs eines Versuchs dieser gelöscht und damit ein weiterer Antritt ermöglicht werden. Ein Beispiel für einen solchen begründeten Fall wäre der Sturm des Prüfungssaales durch Störer, wodurch den Kandidatinnen und Kandidaten die für die Prüfung wichtige Konzentration genommen wird. Auch technische Störungen oder Krankheitsfälle sind begründete Fälle, die einen erneuten Versuch rechtfertigen.

**Bild 14.37** Ein ungültiger Versuch kann durch eine lehrende Person gelöscht und damit ein erneuter Antritt ermöglicht werden. Die Löschung ist zu dokumentieren und die Ergebnisse zuvor zu speichern.

![Image 700](index-659_1.jpg)

![Image 701](index-659_2.png)

**636** 14 Lernzielkontrollen und Prüfungen

**Bild 14.38** Ein Klick auf den Zahlenwert der Bewertung führt zur Überprüfung einer einzelnen Antwort. Hier lässt sich erkennen und klären, wenn etwas schiefgelaufen ist.

**Bild 14.39** Natürlich ist die Antwort in diesem Fall falsch. Aber was, wenn die Antwort strittig wäre und die Vergabe von Teilpunkten gerechtfertigt? Dann gibt es hier die Möglichkeit, die automatisch von Moodle vergebenen Punkte zu überschreiben.

![Image 702](index-660_1.png)

14.4 Die Aktivität „Test“

**637**

**14.4.5.4■Grundsätzliche manuelle Bewertung**

Wie bereits angesprochen, gibt es Fragen, deren Antworten sich nicht automatisch durch Moodle (nach den Regeln des Fragenerstellers) bewerten lassen. Das mag in einiger Zukunft unter dem Einsatz künstlicher Intelligenz5 anders aussehen, jedoch ist Moodle derzeit noch nicht in der Lage, Texte zu verstehen und zu interpretieren, um daraus belastbare Bewertungen abzuleiten.

Freitextantworten müssen also heute nach wie vor vom Lehrenden gelesen und bewertet werden. Es fließen hier also unvermeidlich subjektive Einflüsse in die Bewertung mit ein.

Was dies betrifft, so bietet die elektronische Prüfungsform zunächst keinen echten Gewinn.

Zumindest ist die Bewertung vom reinen Prozedere betrachtet nicht anders als bei der Be -

urteilung einer auf Papier geschriebenen Arbeit.

Es gibt aber bereits an dieser Stelle Meinungen, die allein durch die elektronische Abgabe einer Freitextantwort einen positiven Effekt hinsichtlich der Neutralisierung subjektiver Einflüsse sehen. Diese Ansichten werden wohl wissend vertreten, dass die Identitäten der Kandidatinnen und Kandidaten bekannt sind und demnach persönliche Sympathie oder Antipathie nicht ausgeschlossen werden kann. Es wird argumentiert, dass das Schriftbild einen unterbewussten, jedoch direkten Einfluss auf die Bewertung haben kann. Ein schönes Schriftbild wirkt offensichtlich „kompetenter“ als eine ungelenke Handschrift, die womöglich noch durch viele Durchstreichungen und Rechtschreibfehler negativ betont wird.

Tatsächlich ist es die Vielfalt der Handschriften der Teilnehmerinnen und Teilnehmer, die das deutlichste Argument für eine elektronische Prüfung darstellt. Dabei wird keinerlei subjektive Bewertung betrachtet, sondern allein der praktische Aspekt. Schlechte Handschriften sind schwer zu lesen und können somit zu Fehldeutungen führen. Es erfordert viel Zeit, eine handschriftliche Arbeit mit dem Anspruch auf Fairness zu beurteilen. Eine in ein Textfeld geschriebene Antwort wird immer in einer klar lesbaren Computerschrift dargestellt. Dies erleichtert die Lesbarkeit und damit die Bewertung. Es bringt für Lehrende einen deutlichen Zeitgewinn in der Bearbeitung der Prüfungen.

**Bild 14.40** 

Die Frage 2 – es handelt sich um eine Freitextaufgabe, die

das System nicht automatisch bewerten kann – zeigt hier

zwei verschiedene Ergebnisse: In der ersten Zeile wird sie als

„Falsch“ gekennzeichnet. Nur in der zweiten Zeile wird die

Bewertung gefordert.

5 Künstliche Intelligenz (KI) ist eine mittlerweile sehr weit fortgeschrittene Technologie. Die Spitze des Eisbergs ist jedem im Alltag bekannt, wenn Sprachsteuerungssysteme eingesetzt werden. Diese nutzen allerdings sehr große Rechenleistungen in einem entfernten System – meist in den USA gehostet, weil dort die führenden Unternehmen dieser Branche beheimatet sind. Das wirft bereits Fragen hinsichtlich des Daten- und Persönlichkeitsschutzes auf.

Es werden nicht allein die Sprachbefehle gedeutet und in konkrete Schaltanweisungen umgesetzt, sondern es können auch Sprachanalysen durchgeführt und tiefgreifende Forschungen betrieben werden. Stimme ist ein biometrisches Merkmal, das zur eindeutigen Erkennung eines Menschen verwendet werden kann. Auch das Militär forscht intensiv im Bereich der künstlichen Intelligenz. Bildungssysteme werden möglicherweise von den Ergebnissen – wenngleich nicht primär – profitieren können. Es wird jedoch noch einige Jahre dauern, bis tatsächlich Bildungssysteme auf der Basis künstlicher Intelligenz eingesetzt werden können.

![Image 703](index-661_1.png)

**638** 14 Lernzielkontrollen und Prüfungen

**Bild 14.41** Nach einer einfachen mathematischen Betrachtung erscheint die angezeigte Zeile unlogisch: Es wurde von zwei Lösungen noch keine bewertet. Es ist aber nur eine einzige Frage zur Bewertung ausstehend. Dies spiegelt die Aussage des vorherigen Bilds wider.

![Image 704](index-662_1.png)

![Image 705](index-662_2.png)

14.4 Die Aktivität „Test“

**639**

**Bild 14.42** In der manuellen Bewertung können Lehrende ein persönliches Feedback zur Antwort geben. Die zu vergebenden Punkte werden manuell eingetragen und sind nach der Speicherung im System gültig.

**Bild 14.43** Eine Freitextantwort wurde automatisch als „falsch“ gekennzeichnet. Dazu war das System automatisch in der Lage, weil keine Antwort geliefert wurde. Es gibt im Antwortfeld keinen Inhalt.

**640** 14 Lernzielkontrollen und Prüfungen

In Bild 14.40 sind zwei Zeilen zu erkennen, wobei die Freitextantwort (Frage 2) nur in einem Fall eine Bewertung fordert. In der ersten Zeile wird dagegen ein rotes X gesetzt und damit eine falsche Antwort indiziert. Obwohl Moodle im Prinzip nicht in der Lage ist, eine Freitextantwort zu bewerten, gibt es eine Ausnahme: Ist das Antwortfeld leer, so kann keine richtige Antwort vorliegen! Hier ist es also eindeutig, dass es keine Punkte zu vergeben gibt, und Moodle wird diese Antwort nicht mehr zur manuellen Bewertung anbieten.

Ist das Textfeld jedoch ausgefüllt und sei es nur mit einem einzigen Druckzeichen, dann ist die Antwort zu sichten und zu bewerten. Für die Bewertung sind zwei Schritte vorzunehmen. Wichtig ist rein formal die Vergabe der Punkte, die in das Ergebnis des Kurses mit einfließen. Optional, aber aus didaktischen Gründen sehr wichtig ist das persönliche Feedback. Dieses wird in ein eigenes Textfeld eingetragen.

**■**

**■ 14.5■Der Safe Exam Browser der ETH-Zürich**

Wie in Abschnitt 14.4.2 bereits angedeutet, ist es schwierig, Betrugsversuche durch die technischen Möglichkeiten von Moodle zu verhindern. Dieses Problem wurde in der Schweiz erkannt und von der Abteilung „Lernentwicklung und -technologie“ der ETH Zürich in ein sehr zuverlässiges Produkt umgesetzt: Der Safe Exam Browser (SEB) ist ein sogenanntes _Kiosk System_ 6. Dieser Browser ist für verschiedene Plattformen verfügbar:

MS-Windows

Mac OS

iOS

Der Safe Exam Browser wird über das Lernmanagementsystem aufgerufen. Ist der Browser aktiv, dann erscheint die Oberfläche im Vollbildmodus. Allerdings gibt es einen wesentlichen Unterschied zum Vollbildmodus mit JavaScript (vgl. Abschnitt 14.4.2.2): Der Safe Exam Browser bietet keine Hintertüren. Tastenkombinationen wie **Alt**+**Tab** lassen sich sperren.

**Safe Exam Browser – nicht allein für Moodle**

Der Safe Exam Browser wird nicht nur mit Moodle, sondern auch in anderen Lernmanagementsystemen eingesetzt. Das sind u. a. ILIAS und OpenOLAT.

■

6 Der Begriff eines Kiosk-Systems kommt aus der multimedialen Werbetechnologie. Öffentliche Internet-Terminals sollen den potenziellen Kunden ermutigen, durch die Webseiten des eigenen Unternehmens zu navigieren, jedoch soll es keine Plattform für den Besuch beliebiger Seiten darstellen.

![Image 706](index-664_1.jpg)

![Image 707](index-664_2.png)

14.5 Der Safe Exam Browser der ETH-Zürich

**641**

**Bild 14.44** Der Safe Exam Browser kann kostenlos für die wichtigsten Betriebssysteme heruntergeladen werden. Linux-User können den Safe Exam Browser jedoch nicht verwenden.

**Bild 14.45** Vor dem ersten Einsatz des Safe Exam Browsers ist die Konfiguration erforderlich. Dies ist grundsätzlich eine Aufgabe der Lehrenden, welche die Regeln der Prüfung und damit auch die für die Verwendung von Werkzeugen festlegen.

**642** 14 Lernzielkontrollen und Prüfungen

Der Safe Exam Browser ist kein Webbrowser im klassischen Sinn. Seine Aufgabe ist es, Funktionen außer Kraft zu setzen und den Zugriff auf andere Programme des Computers einzuschränken. Es soll also verhindert werden, dass während der Prüfung andere Webseiten aufgerufen werden als es für die Bearbeitung der Prüfung nötig ist. Um das zu ge -

währleisten, ist eine spezielle Konfiguration erforderlich, die vom Lehrenden zu erstellen ist. In dieser Konfiguration wird unter anderem festgelegt, welche zusätzlichen Programme verfügbar sein dürfen. Das ist durchaus im Sinn einer Prüfung, denn möglicherweise sind Aufgaben mithilfe externer Software zu lösen. Man denke nur an die Programmierung von Robotern mit der jeweiligen Administrationssoftware.

Die Konfigurationsdatei des Safe Exam Browsers enthält jedoch noch sehr viel mehr Details.

Die wichtigste Information ist die Adresse der Testaktivität, welche die Prüfung beinhaltet.

Damit startet der Safe Exam Browser automatisch mit einem Anmeldebildschirm des Moodle- Systems. Nach dem Login gelangen die Kandidatinnen und Kandidaten direkt zur Prüfung.

Der Safe Exam Browser kann entweder direkt auf den Rechnern der Teilnehmerinnen und Teilnehmer installiert oder mit einem via Netzwerk gebooteten Betriebssystem mitgeliefert werden. Beides birgt vor allem rechtliche, aber auch technische Probleme.

Das Booten eines kompletten Betriebssystems über das Netzwerk ist durchaus ein Konzept, welches auch im Business-Bereich verwendet wird. Die eigentlichen Computer sind quasi nur „dumme Technologie“ ohne eigenes Betriebssystem und ohne eigene Software. Es handelt sich um sogenannte Thin Clients. Damit dies jedoch funktionieren kann, müssen die Computer für das Booten über das Netzwerk konfiguriert werden. Komplikationen können hierbei neue BIOS-Technologien hervorrufen, wenn diese eine ID beinhalten, die direkt mit der Lizenz eines Betriebssystems verbunden ist. Eine der größten Herausforderungen stellt jedoch die Schaffung einer geeigneten Infrastruktur dar. Eine Verkabelung geeigneter Prü-fungssäle ist kostspielig und erfordert neben dem rein technischen Aufwand auch eine entsprechende Administration. Diese Räume werden quasi per se für Prüfungen bevorzugt zu belegen sein. Es stellt sich damit also auch ein organisatorisches Problem.

Die feste Installation auf privaten Computern der Kandidatinnen und Kandidaten ist rechtlich nicht unumstritten. Es stellen sich Fragen nach einer eventuellen Haftung. Gibt es Störungen im System, kann alleine die Behauptung, der Safe Exam Browser (oder eine andere im Prüfungskontext installierte Software) hätte die Störung verursacht, Streitigkeiten verursachen, die durchaus juristisches Niveau erreichen können.

Zusätzlich muss in der Organisationsstruktur der Schule oder Hochschule eine Beratungs-stelle installiert werden. Der Safe Exam Browser erfordert eine Einführung in dessen Benutzung und den entsprechenden technischen Support. Man darf davon ausgehen, dass an Schulen und Hochschulen nur ein Bruchteil der Lernenden einen technisch orientierten Hintergrund besitzt. Die meisten Lernenden benutzen das Internet, ein Smartphone und den Laptop als reines Werkzeug und verlassen sich auf dessen Funktion. Für technische Feinheiten wird also professionelle Hilfe benötigt und diese Experten müssen mit allen denkbaren Varianten der verwendeten Geräte, deren Betriebssystemen und Formfaktoren vertraut sein. Dies ist grundsätzlich eine Herausforderung in einer zunehmend digitalisier-ten Gesellschaft.

![Image 708](index-666_1.png)

![Image 709](index-666_2.jpg)

14.5 Der Safe Exam Browser der ETH-Zürich

**643**

**Bild 14.46** 

Die Konfiguration des Safe Exam Browsers ist nur

mit einem Administrator-Passwort zugänglich.

Damit werden Manipulationen ausgeschlossen.

Der Safe Exam Browser unterscheidet sich vor allem durch die Restriktion beim Zugriff auf Ressourcen des eigenen Computers vom Vollbildmodus wie er für Prüfungen in Moodle vorgesehen werden kann. Programme, die während einer Prüfung als Hilfsmittel zugelassen sind, müssen ausdrücklich in der Konfiguration des Safe Exam Browsers eingetragen werden. Ebenso lässt sich der Aufruf von Webseiten durch den Safe Exam Browser beschränken. Die Recherche nach einer Antwort über eine Suchmaschine ist damit ausgeschlossen.

Die mit dem Safe Exam Browser verbundenen Einschränkungen bei der Nutzung des Computers während der Prüfungszeit betreffen auch gängige Tastencodes wie beispielsweise **Alt**+**Tab**, mit denen zwischen aktiven Programmfenstern umgeschaltet werden kann. Die Einstellungen des Safe Exam Browsers können so weit reichen, dass eine Rückkehr ins Betriebssystem nicht mehr möglich ist. In der Regel wird man jedoch eine Exit-Sequenz aus drei Funktionstasten oder ein Passwort zum Beenden des Safe Exam Browsers vorsehen.

Um die Restriktionen zu umgehen, müsste also lediglich die Konfiguration des Browsers verändert werden. Diese liegt in der Datei _SebClientSettings.seb_ vor. Sie ist jedoch nicht mit einem gewöhnlichen Editor zu bearbeiten und damit gesichert. Um die Einstellungen zu bearbeiten wird das Programm _SEBConfigTool.exe_ benötigt, was mit dem Safe Exam Browser installiert wird. In der Regel wird der Zugriff auf die Konfiguration durch ein Administrations-Kennwort geschützt. Damit ist eine Manipulation der Einstellungen ausgeschlossen.

**Bild 14.47** Die wichtigsten Einstellungen werden in diesem Fenster vorgenommen. Dazu gehören die Startadresse, über die der Safe Exam Browser den Weg zur Prüfung findet, die Kennwörter für den Konfigurationszugang und die Ausstiegssequenzen, um nach der Prüfung wieder zum regulären Betriebssystem zurückzukehren.

![Image 710](index-667_1.png)

**644** 14 Lernzielkontrollen und Prüfungen

**Bild 14.48** Im Einzelfall können auf dem Computer installierte Programme als erlaubte Hilfsmittel freigegeben werden.

![Image 711](index-668_1.png)

14.6 Leistungen einzelner Students **645**

**Bild 14.49** Dem Safe Exam Browser fehlen sämtliche Menü- und Navigationsleisten, wie man sie sonst von einem gewöhnlichen Webbrowser kennt. Auch die im unteren Bereich dargestellte Taskleiste kann deaktiviert werden. Es steht einzig und allein der Prüfungsinhalt zur Verfügung.

**■**

**■ 14.6■Leistungen einzelner Students**

Lehrende stehen spätestens am Ende einer Lehrveranstaltung vor der Aufgabe, die gesamten Leistungen des Kurses zu beurteilen. Eine mit der Aktivität _Test_ durchgeführte Prüfung ist meist nur eine Komponente und sollte grundsätzlich nicht die einzige Wertungsgrund-lage darstellen. Eine solche Prüfung stellt schließlich nur eine Momentaufnahme dar und spiegelt die Tagesform der Kandidatin bzw. des Kandidaten wider.

Lehrende können sich über den Leistungsstand der Teilnehmerinnen und Teilnehmer ihres Kurses informieren, wenn sie in die Teilnehmerliste blicken. Dort kann jedes einzelne Nutzer-Profil aufgerufen werden. Mit den entsprechenden Rechten der Teacher-Rolle kann in diesen Profilen die Bewertungsübersicht aufgerufen werden. Darin finden natürlich auch die betroffenen Lernenden eine Übersicht zu den von ihnen erbrachten Leistungen.

![Image 712](index-669_1.png)

**646** 14 Lernzielkontrollen und Prüfungen

In der Leistungsübersicht finden die betreffenden Students alle sie betreffenden Kurse. Personen mit der Teacher-Rolle haben Einblick in die Ergebnisse der von ihnen betreuten Kurse. Es lassen sich die Ergebnisse jeder einzelnen Aktivität des Kurses einsehen und einzelne Ergebnisse beantworteter Fragen nachvollziehen.

**Bild 14.50** Lehrende haben die Möglichkeit, die Ergebnisse ihrer Lernenden zu prüfen und bei Bedarf anzupassen.

![Image 713](index-670_1.jpg)

![Image 714](index-670_2.jpg)

14.6 Leistungen einzelner Students **647**

**Bild 14.51** Lehrenden mit den entsprechenden Rechten ist in den Nutzerprofilen die Bewertungsübersicht im Block _Berichte_ zugänglich.

**Bild 14.52** Lehrende können lernende Personen in verschiedenen Kursen betreuen. Nur auf die Bewertungen dieser Kurse gibt es einen Zugriff.

![Image 715](index-671_1.png)

**648** 14 Lernzielkontrollen und Prüfungen

**Bild 14.53** Nicht nur die Prüfungsergebnisse, sondern auch die Fortschritte in einzelnen Lektionen des Kurses sind ersichtlich und können in die Gesamtbeurteilung einbezogen werden.

![Image 716](index-672_1.png)

14.6 Leistungen einzelner Students **649**

**Bild 14.54** Es ist möglich, nachträglich Fragen und Aktivitäten zu betrachten und deren Bewertung zu prüfen.