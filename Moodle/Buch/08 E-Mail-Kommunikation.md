Moodle benötigt aus mehreren Gründen eine Schnittstelle zu einem E-Mail-Dienst:

Der Administrator bekommt automatische Systemmeldungen.

Students (Lernende) bekommen automatische Meldungen zu Neuheiten in den Foren.

Abwicklung von Selbsteinschreibungen.

Direkte E-Mail-Kommunikation zwischen Benutzerinnen und Benutzern im System. (Voraussetzung: Die E-Mail-Adressen müssen in den Profilen sichtbar sein.)

Die Grundeinstellungen im System für die E-Mail-Kommunikation obliegen dem Moodle-Administrator bzw. der -Administratorin. In der _Website-Administration_, Register _Server_ sind für den Versand und den Empfang im Abschnitt _E-Mail_ die jeweiligen Einstellungen vorzunehmen.

**Bild 8.1** Im Bereich „E-Mail“ der Server-Konfiguration werden vor allem Serveradressen und die jeweils erforderlichen Zugangsdaten definiert.

![Image 267](index-305_1.jpg)

**282** 8 E-Mail-Kommunikation

**■**

**■ 8.1■Konfiguration für ausgehende E-Mails**

Der E-Mail-Ausgang wird über einen sogenannten SMTP-Server versendet. Einen solchen SMTP-Server nutzt jede Person, die am PC oder dem Smartphone Nachrichten mit dem E-Mail-Dienst verschickt. Die jeweils nötigen Konfigurationsdaten werden vom Betreiber des E-Mail-Servers geliefert. Das kann ein beliebiger öffentlicher Anbieter und sogar ein Freemailer wie GMX, Microsoft (Outlook, ehemals Hotmail), Google (GMAIL) etc. sein. Möglicherweise gibt es bereits im hauseigenen IT-System einen solchen Mail-Server. In diesem Fall ist für die Einrichtung der Zugangsdaten und deren Bereitstellung der zuständige Systemverwalter verantwortlich.

**■**

**■ 8.2■SMTP-Konfiguration**

Für die Konfiguration ausgehender E-Mails wird zunächst die Adresse des SMTP-Servers benötigt. Das Feld kann frei bleiben, wenn der Webserver, auf dem das Moodle-System läuft, bereits für den E-Mail-Versand vorbereitet ist und die PHP-Standard-Methoden für den Versand verwenden kann.

**Bild 8.2** Die Server-Adresse für den Postausgang bekommt man vom Anbieter des E-Mail-Dienstes (auch öffentliche Freemailer kommen in Frage) oder vom Systemadministrator in der eigenen IT-Abteilung.

In diesen Bereich sind weitere wichtige Daten einzutragen:

SMTP-Sicherheit

SMTP-Authentifizierung

SMTP-Anmeldename

SMTP-Kennwort

8.2 SMTP-Konfiguration

**283**

Diese Daten, die ebenfalls vom Betreiber des E-Mail-Servers bezogen werden, dienen der Sicherheit gegen Missbrauch des eigenen Postfachs. Man stelle sich den möglichen Ärger vor, wenn über dieses Mail-Postfach unerlaubte Inhalte (Gewaltverherrlichung, Kinderpor-nografie, Terrorplanung etc.) versendet werden. Es versteht sich somit von selbst, dass auch der Zugang zum E-Mail-Server geschützt werden muss.

**Der E-Mail-Dienst ist die moderne „Postkarte“!**

Ähnlich wie bei einer klassischen Postkarte werden Nachrichten mit dem E-Mail-Dienst unverschlüsselt, also in Klartext übertragen! Gelingt es, die Datenübertragung anzuzapfen, können E-Mail-Inhalte somit unbemerkt von Unbekannten gelesen und durchaus auch manipuliert werden. Für vertrauliche Informationen empfiehlt sich also somit eine Verschlüsselung der Inhalte. Auf jeden Fall sollte der Zugriff auf das E-Mail-Konto ausschließlich nach einer persönlichen Authentifizierung erfolgen.

■

Für die Herstellung der Sitzung zwischen dem E-Mail-Programm auf dem eigenen PC bzw.

hier dem Moodle-System und dem öffentlichen Mail-Server, sollte eine gesicherte Verbindung verwendet werden, damit kriminellen Elementen keine Möglichkeit des Missbrauchs eröffnet wird. „Keine“ SMTP-Sicherheit ist deswegen eine schlechte Entscheidung. Die meisten Server bieten entsprechend verschlüsselte Übertragungen nach dem SSL- oder dem TLS-Protokoll an.

_SSL_ steht für Secure Socket Layer. _TLS_ gilt als eine Weiterentwicklung von SSL und steht für Transport Layer Security. Die entsprechenden Protokolle können auch durch die jeweiligen _Port-Adressen_ 1 bezeichnet werden: SSL = 465 und TLS = 587 (jeweils für den SMTP-Zugang).

Eine weitere wichtige Einstellung ist die SMTP-Authentifizierung.2 Die Standardeinstellung ist hier „LOGIN“. Hierbei erfolgt die Übermittlung der Zugangsdaten (Benutzername und Kennwort) unverschlüsselt wie auch beim Verfahren „PLAIN“. Allerdings erfolgt die Übertragung in zwei Schritten.

Das Verfahren „CRAM-MD5“ arbeitet nach dem sogenannten Challenge-Response-Verfahren. Hierbei sendet der Server einen Zufallswert an das Moodle-System, welcher mit dem Passwort zu kombinieren ist, um daraus einen MD5-Hashwert, eine Prüfsumme, zu erzeugen. Nur diese Prüfsumme, nicht aber das Passwort, wird übertragen. Selbstverständlich ist die Prüfsumme stets eine andere, weil ein Teil der dazu verwendeten Vorlage ein Zufallswert ist. Ähnlich funktioniert auch das NTLM3-Verfahren.

In großen Moodle-Installationen kann es die Verarbeitungsgeschwindigkeit beim E-Mail-Versand beschleunigen, wenn mehrere Nachrichten in einer gemeinsamen SMTP-Sitzung an den Ausgangsserver übertragen werden. Wird dagegen das _Limit für die SMTP-Session_ auf 1

gesetzt, so wird für jede Übertragung eine eigene Verbindung zum Mail-Server etabliert.

1 Während mit der IP-Adresse ein Computer innerhalb eines Netzwerks adressiert wird, stehen die Port-Adressen für den Serverdienst auf diesem Computer.

2 Welches Verfahren zur SMTP-Authentifizierung angewendet wird und deswegen einzustellen ist, hängt von den Vorgaben des Mail-Server-Betreibers ab. Diese Einstellung ist also nicht frei wählbar.

3 NTLM steht für NT LAN Manager. Das Authentifizierungsverfahren beruht auf dem Challenge-Response-Prinzip.

**284** 8 E-Mail-Kommunikation

**■**

**■ 8.3■No Reply**

Systemmeldungen sind automatisch generierte Nachrichten von einer Maschine! Es ist deswegen nicht sinnvoll, eine Antwort-Möglichkeit vorzusehen. Allerdings soll beim Empfänger eine E-Mail-Adresse des Absenders angezeigt werden (siehe Bild 8.4). Für den Empfänger der Nachricht sollte jedoch die Absenderadresse ausdrücklich darauf hinweisen, dass diese keine Antworten akzeptiert. Dies wird meist mit Begriffen wie _No Reply_ oder _Bitte_ _nicht antworten_ etc. in der Adresse bereits kundgetan.

**Ein Beispiel**

Die reguläre E-Mail-Adresse eines Moodle-Administrators sei _moodleadmin@domain.tld_.

Diese soll jedoch nicht öffentlich erscheinen und es sind keine Antworten auf automatisch generierte Systemnachrichten erwünscht. Die Absenderadresse des Moodle-Systems wird deswegen entsprechend geändert:

_noreply@domain.tld_

**Rechtliche Rahmenbedingungen beachten!**

Es gibt verschiedene gesetzliche Bestimmungen, die den unaufgeforderten

Versand von E-Mails regeln. Auch beim E-Mail-Versand hat sich eine Art

Impressumspflicht etabliert. In der E-Mail sollte deswegen eine Signatur enthalten sein, aus der der Absender, dessen Kontaktdaten und der Zweck

der Nachricht hervorgehen. Das gilt auch dann, wenn die Mail an im System registrierte Benutzerinnen und Benutzer gesendet wird.

■

**■**

**■ 8.4■Anzeigeeinstellungen**

Ob eine gesendete E-Mail auch so beim Empfänger ankommt, wie sie geschrieben wurde, hängt wesentlich vom verwendeten Zeichensatz ab. Dieser sollte der Systemeinstellung entsprechen und auch für den E-Mail-Versand nicht verändert werden. Abweichungen werden in der Regel nur in wenigen Ausnahmefällen erforderlich sein.

Das Feld _Via-Information_ für E-Mails bezieht sich auf die Darstellung eines Absendernamens, wie er im Posteingang des Empfängers erscheint (vgl. Bild 8.4). Auch dies ist eine zusätzliche Information für den Empfänger über den Ursprung der Nachricht. Hier stehen drei Optionen zur Auswahl:

_Nie_ – das bedeutet, dass grundsätzlich neben dem Absendernamen kein Hinweis erscheint, dass der Versand der Nachricht aus dem Moodle-System erfolgt.

_Immer_ – dies ist die Standardeinstellung – sie bewirkt einen grundsätzlichen Hinweis über den Ursprung der Nachricht.

_Nur falls von einer No-Reply-Adresse_ – die Einschränkung bezieht sich auf Sendungen, die keine Antwort entgegennehmen können.

8.5 Test der Einstellungen

**285**

E-Mail-Postfächer sind heute meist stark gefüllt. Dabei wird gleichzeitig die Zeit für die Prüfung einer E-Mail, ob diese denn tatsächlich wichtig und relevant sei, immer knapper.

Deswegen werden die meisten E-Mails heute nicht einmal mehr gelesen. Die Entscheidung, ob eine Nachricht gelesen, ignoriert oder direkt in den Papierkorb geschoben wird, wird meist nach dem kurzen „Überfliegen“ der Betreffzeilen getroffen.

Damit sofort erkennbar ist, dass es sich bei der E-Mail um eine Nachricht aus dem Moodle-System handelt, kann vor die eigentliche Betreffzeile ein Präfix gesetzt werden. Dieses sollte nicht zu lang, aber dennoch aussagekräftig formuliert werden.

Zu experimentieren ist mit der Einstellung der Zeilenumschaltung. Hier gibt es die Optionen LF (= Linefeed) oder CRLF (Carriage Return4/Linefeed). Meist wird heute die Option LF

gesetzt, was von den meisten E-Mail-Programmen korrekt interpretiert wird. Die Option CRLF führt dagegen meist zu einem zweifachen Zeilenumbruch.

In die Rubrik _Anzeigeeinstellungen für E-Mails_ fällt auch die Entscheidung, ob der Versand von Dateianhängen gestattet werden soll. Der Standard ist hier _Ja_, denn gelegentlich werden auch Systemnachrichten mit einem Anhang versendet.

**■**

**■ 8.5■Test der Einstellungen**

Um festzustellen, ob die Einstellungen korrekt sind, kann eine Test-E-Mail versendet werden. Hierzu ist lediglich eine gültige Empfängeradresse in das Dialogfeld einzutragen und die Mail zu versenden. Allerdings müssen die Einstellungen zuvor gespeichert werden. Es darf nicht vergessen werden, dass Moodle lediglich eine Web-Applikation ist. Man arbeitet in Formularen innerhalb der Oberfläche eines Webbrowsers (Chrome, Firefox, Opera, Edge bzw. Internet-Explorer etc.) und nicht direkt im System. Erst nach dem Absenden der Daten und deren Verarbeitung durch die Skripte auf dem Webserver sind die Einstellungen gültig.

**Das leidige Thema: „Spam or no Spam“?**

Wenn die Testnachricht versendet wurde, aber scheinbar nicht im Postfach ankommt, so kann das verschiedene Ursachen haben: falsche Zugangs- oder

Serverdaten, ein Schreibfehler etc. Sehr häufig führen jedoch sehr restriktive SPAM-Filter dazu, dass eine Nachricht im Spam- oder Junkmail-Verzeichnis landet. Es lohnt sich in diesem Fall, einen Blick in diese Ordner zu werfen und die Absenderadresse – falls die Nachricht tatsächlich gefiltert wurde – auf eine Whitelist5 zu setzen. Diese Empfehlung sollte auch allen Systembenutzerinnen und Systembenutzern gegeben werden, die sich bei Moodle anmelden.

■

4 Der Begriff kommt aus der Zeit mechanischer Schreibmaschinen, als ein Zeilenwechsel (Drehung der Walze mit dem Papiertransport = Linefeed) und der Wagenrücklauf (Druckposition am Zeilenanfang = Carriage Return) zwei separate, jedoch hintereinander durchgeführte Vorgänge waren.

5 Eine _Whitelist_ ist eine Filterliste, in die speziell erwünschte E-Mail-Adressen eingetragen werden. Damit lassen sich Ausnahmen bei ansonsten pauschalen Sperrregeln festlegen.

![Image 268](index-309_1.jpg)

![Image 269](index-309_2.png)

**286** 8 E-Mail-Kommunikation

**Bild 8.3** Der Test des E-Mail-Ausgangs verlief hier erfolgreich. Zumindest besagt die Meldung, dass die E-Mail vom Ausgangsserver angenommen wurde. Ein Beleg über deren Zustellung ist das aber noch nicht.

**Bild 8.4** Die Testnachricht ist eingetroffen. Damit sind die Einstellungen des Ausgangsservers korrekt. Darüber hinaus funktioniert das Präfix für die Betreffzeile (1), die Einstellung der (noreply)-

Absenderadresse (2) und die „Via-Information“ (3).

8.7 E-Mail-Texte ändern

**287**

**■**

**■ 8.6■E-Mail-Posteingang für Moodle**

Das Moodle-Forum ist eines der wichtigsten Kommunikationswerkzeuge des gesamten Systems. Benutzerinnen und Benutzer können über die Aktivitäten in den Foren per E-Mail informiert werden. Es ist zudem möglich, direkte Antworten per E-Mail zu erlauben. Allerdings muss dies von der Administration in den Server-Einstellungen für die E-Mail-Kommunikation ausdrücklich zugelassen werden.

Die Standardeinstellung ist hier _Nein_! Der Grund sind mögliche SPAM-Angriffe auf das E-Mail-Konto, mit denen der Ablauf der Lehrveranstaltungen gestört und das Forum durch Überflutung mit Müll-Nachrichten faktisch unbrauchbar gemacht werden kann. Solche Angriffe werden oft automatisch von Algorithmen durchgeführt. Allerdings funktionieren SPAM-Filter bei den Betreibern von Mailservern heute bereits sehr gut, sodass derartige Attacken selten sind bzw. schnell gestoppt werden können. Ist diese Funktion deaktiviert, so können Foreneinträge ausschließlich direkt im Moodle-System nach einem Login diskutiert werden.

Damit Moodle eine E-Mail empfangen kann, müssen dem System eine eigene E-Mail- Adresse zugewiesen und damit verbunden die Zugangsdaten zum Posteingangsserver in die Konfiguration eingetragen werden. Dabei kann es sich um einen POP3- oder einen IMAP-Server handeln. Beim POP3-Protokoll werden die E-Mails in der Regel vom Server heruntergeladen und dort anschließend gelöscht. Das IMAP-Protokoll belässt die gelesene E-Mail auf dem Server und gestattet darüber hinaus die Organisation des E-Mail-Eingangs in einer eigenen Verzeichnisstruktur.

Einzutragen sind:

E-Mail-Eingangsserver: Von diesem Server ruft Moodle in regelmäßigen Abständen die elektronische Post ab.

Benutzername

Kennwort

Einstellung einer eventuellen SSL- oder TLS-Verschlüsselung.

Darüber hinaus muss das interne E-Mail-Konto konfiguriert werden. Hierzu werden die beiden Adressteile vor („Name“ des E-Mail-Kontos) und nach dem „@“-Zeichen (E-Mail-Domain) getrennt eingetragen. Damit allerdings eingehende E-Mail-Nachrichten verarbeitet werden können, muss das „Mailverfahren“ mit der ersten Checkbox in diesem Menü aktiviert werden. Dies sind Einstellungen, die als Voraussetzung für weitere Dienste innerhalb des Moodle-Systems genutzt werden. Moodle selbst ist kein Mail-Server!

**■**

**■ 8.7■E-Mail-Texte ändern**

Es ist wichtig, den Benutzerinnen und Benutzern im System bereits frühzeitig die Spielregeln zu erklären! Das Verfahren einer E-Mail-Verifizierung erscheint augenscheinlich ideal, um zu überprüfen, ob beispielsweise bei der Registrierung tatsächlich Fehleingaben

**288** 8 E-Mail-Kommunikation

des Passworts vorlagen (beispielsweise durch aktive Feststelltaste, prellende oder ver-schmutzte Tasten etc.). Die legitime Benutzerin oder der Benutzer werden in ihrem E-Mail-Postfach nachsehen und den Zugang freischalten. So ist es regulär vorgesehen.

Leider ist auch ein anderes Szenario denkbar: Ein Angreifer kann eine solche E-Mail generieren und mit einem eigenen Link auf eine gefälschte Webseite verweisen. Das Fälschen von Webseiten ist leider kinderleicht. In der gefälschten Seite erscheint dann ein Eingabe-formular für die Zugangsdaten, die jedoch keinen Zugang zu Moodle herstellen, sondern einfach nur den Anmeldenamen in Verbindung mit dem Kennwort abschöpfen. Seit Jahren ist diese Form des Angriffs auf Zugangsdaten als _Phishing_ bekannt. Meist werden Bank-kundinnen und Bankkunden angegriffen, aber auch Bildungseinrichtungen sind begehrte Ziele.

Man ist einer Phishing-Attacke jedoch nicht schutzlos ausgeliefert. Es gibt ein paar einfache Anhaltspunkte, die Phishing-Mails entlarven können.

Mäßige oder sogar mangelhafte Rechtschreibung. Phishing-E-Mails sind meist automatisch aus einer anderen Sprache übersetzt worden. Diese Übersetzungsalgorithmen werden zwar immer besser, jedoch entlarven sich nach wie vor die meisten Phishing-Mails durch schlechte Rechtschreibung.

Die Verfasser einer Phishing-Mail wollen Druck erzeugen und die Schockwirkung beim Empfänger ausnutzen, um diesen zu einer übereilten und unüberlegten Handlung zu bewegen. Keine seriöse Administration wird mit rustikalen Drohungen argumentieren.

Bei einer seriösen Benachrichtigung einer Bank wird man grundsätzlich nicht mit einem Link auf eine Login-Seite geführt und zur Eingabe der Zugangsdaten genötigt. Dies ist im Fall der Freischaltung eines gesperrten Moodle-Kontos anders, jedoch liegt hier eine ini-tiierende Handlung vor: Die Benutzerin oder der Benutzer hat definitiv eine Falscheingabe getätigt. Geht ohne eine solche Fehleingabe eine vermeintliche Administrator-E-Mail ein, so ist dies ein Indiz für einen Angriffsversuch. In diesem Fall sollte ein Login über den regulären Weg versucht werden. Auf gar keinem Fall ist bei einer unerwarteten E-Mail dem darin enthaltenen Link zu folgen!

Bewegt man den Mauszeiger über den Link oder die Schaltfläche in der (mutmaßlich gefälschten) E-Mail, wird in der Statuszeile die Zieladresse sichtbar. Die Prüfung der Adresse entlarvt einen Angriff, wenn man beginnend beim ersten „Slash“6-Zeichen die Adresse von rechts nach links liest.

**Erkennung einer gefälschten Link-Adresse**

Link-Adressen werden – beginnend beim ersten „Slash“-Zeichen von rechts

nach links gedeutet. Die Adresse setzt sich zusammen aus der Toplevel- Domain (z. B. .de, .at, .com) und links daneben, durch einen Punkt getrennt, die Domain der Webseite (z. B. srg). Noch weiter links, wieder durch einen Punkt getrennt, wird die Subdomain gesetzt, die nahezu beliebig gestaltet werden kann.

6 Das Zeichen Slash: /

8.8 Mitteilungsverwaltung

**289**

Beispiel für eine korrekte Adresse:

https://moodle. _**srg.at**_/login

Beispiel für eine gefälschte Adresse:

https://moodle.srg.at. _**gauner.com**_/login

Die eigentliche Webadresse (Domain.Topleveldomain) ist fett betont. Der Unterschied ist deutlich zu erkennen.

■

Bekommt man eine E-Mail, wird man diese in der Regel eher für authentisch halten, wenn sie eine persönliche Ansprache sowie einen Bezug zu einem bekannten System enthält. Tatsächlich bietet Moodle entsprechende –in den Sprachpaketen definierte – Systemvariablen an, die in die Nachrichtentexte eingebaut werden können. Die Tabelle 8.1 zeigt eine Auswahl der in Moodle definierten Systemvariablen, die sich für die Verwendung in E-Mails eignen.

**Tabelle 8.1** Systemvariablen für die E-Mail-Personalisierung (Auswahl) Systemvariable

Inhalt

{$a->firstname}

Vorname der Nutzerin bzw. des Nutzers

{$a->lastname}

Nachname der Nutzerin bzw. des Nutzers

{$a->sitename}

Name der Moodle-Seite, wie sie in der Konfiguration vorgegeben wurde –

in den Beispielen: „Moodle-Demo“

{$a->username}

Benutzer- bzw. Zugangsname der Nutzerin bzw. des Nutzers

**Platzhalter funktionieren nicht überall!**

Achtung: Die Belegung dieser Moodle-internen Platzhalter wird innerhalb des Programmcodes vorgenommen. Nicht immer ist jeder Dateninhalt tatsächlich verfügbar. Ist dies nicht der Fall, wird die Variable ausgegeben. Jede automa-tisierte E-Mail sollte grundsätzlich im zugehörigen Kontext getestet werden.

■

**■**

**■ 8.8■Mitteilungsverwaltung**

Wenn E-Mail-Schnittstellen konfiguriert wurden, kann in diesem Abschnitt festgelegt werden, wie sich dieser Dienst auch für die interne Kommunikation einsetzen lässt. Dies betrifft drei verschiedene Fälle:

Umgang mit Anhängen gesendeter E-Mails,

Antworten auf Forenbeiträge und

Umgang mit nicht zustellbaren Mitteilungen.

![Image 270](index-313_1.jpg)

**290** 8 E-Mail-Kommunikation

Die jeweiligen Konfigurationsdialoge werden über eine kleine Schaltfläche in Form eines Zahnrads erreicht. Insbesondere werden die Optionen an dieser Stelle aktiviert oder deaktiviert. Es lassen sich zudem die Absenderadressen überprüfen, ob diese einem im System registrierten Profil zugeordnet werden können.

**Bild 8.5** In den weiteren Mitteilungseinstellungen werden die Optionen aktiviert und bei Bedarf auch eine Überprüfung der Absenderadressen festgelegt.
