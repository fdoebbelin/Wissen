Grundsätzlich betrachtet ist Moodle eine auf PHP und einer MySQL-Datenbank basierende Webserver-Applikation, wie es auch gängige Content-Management- Systeme (CMS) wie z. B.

Joomla!, Drupal, Typo3 oder WordPress darstellen. Das be deutet, dass Moodle zunächst einmal keine ausgesprochen komplizierten Systemvoraussetzungen auf einem Webserver erwartet, die nur von speziellen Web space-Anbietern zu erfüllen wären. Dennoch sind die Installation und (sichere) Konfiguration nicht ganz einfach, was verschiedene Gründe hat:

Die PHP-Konfiguration des Webservers muss verschiedene Erweiterungen umfassen, die meist nicht in der Standardinstallation enthalten oder aktiviert sind. In der Regel zeigen sich Webspace-Anbieter hier allerdings gesprächsbereit und aktivieren diese Erweiterungen recht unbürokratisch.

Moodle benötigt einen Webserver, der mit einem SMTP1-Server kommunizieren kann.

Dies ist nötig, um E-Mails versenden zu können.

Es wird ein ausreichend großes Datenverzeichnis benötigt, welches jedoch nicht von externen Besuchern direkt erreichbar sein sollte.

**■**

**■ 3.1■Systemvoraussetzungen**

Moodle ist OpenSource2-Software! Das bedeutet zugleich, dass Moodle vorzugsweise auf lizenzfreien, offenen Systemen entwickelt wird:

Das favorisierte Betriebssystem der Serverumgebung ist Linux.

1 SMTP ist die Abkürzung für „Simple Mail Transfer Protocol“. Ein Systemdienst, der mit diesem Protokoll arbeitet – der SMTP-Server –, übernimmt die geschriebene E-Mail und leitet sie über verschiedene weitere Server innerhalb des Netzes an das Empfänger-Postfach weiter. Von diesem Postfach rufen sogenannte E-Mail-Clients (z. B. MS-Outlook, Thunderbird etc.) die E-Mail ab.

2 OpenSource – offene Quellen – steht für eine gemeinschaftliche, meist ehrenamtliche Entwicklung von Software.

Ein treibender Gedanke war es, hochwertige Software – unabhängig vom rein kommerziellen Motiv – einer breiten Community zur Verfügung zu stellen. Längst hat sich dabei Software von allerhöchster Qualität etabliert. Das Betriebssystem Linux, der Apache-Webserver sowie die Office-Suite LibreOffice bzw. OpenOffice sind Beispiele für den Erfolg.

**30** 3 Der Moodle-Server

Der favorisierte Webserver ist Apache.

Moodle ist für Datenbanken optimiert, die MySQL oder PostgreSQL unterstützen. MSSQL, MariaDB3 und Oracle-Datenbanken werden allerdings auch unterstützt. Es sollte hier keine Probleme geben.

Ein Sicherungslaufwerk sollte – ohne direkte Zugriffsmöglichkeit aus dem Internet – für die regelmäßige Sicherung der Daten zur Verfügung stehen.

**Grundsätzlich auch MS-Webserver möglich**

Grundsätzlich sollte Moodle auch auf Webservern nutzbar sein, die auf dem kommerziellen MS-Windows-Betriebssystem basieren. Hier sollte mit den

Administratoren Kontakt aufgenommen werden, da sich die Konfiguration

von der Linux-Umgebung unterscheidet. Das betrifft auch die Verwendung

der _.htaccess_-Datei, mit deren Hilfe auf Linux-Systemen Verzeichnisse des Webservers u. a. mit Passwörtern geschützt werden können.

■

Moodle definiert Anforderungen an den Webserver und dessen Nebensysteme. Vor allem betrifft das die PHP-Umgebung und den Datenbank-Server.

**Tabelle 3.1** Mindest-(!)-PHP-Versionen für ältere Moodle-Versionen (Quelle: Moodle-Dokumentation)

Moodle-Version

PHP-Mindest-Version4 Datenbank

Moodle 1.0 bis 1.4

PHP 4.0.1

k. A.

Moodle 1.5

PHP 4.0.1

MySQL 3.23, PostgreSQL 7.4

Moodle 1.6

PHP 4.3.0

MySQL 4.1.12, PostgreSQL 7.4

Moodle 1.7

PHP 4.3.0

MySQL 4.1.12, PostgreSQL 7.4,

MS SQL- Server 2005

Moodle 1.8

PHP 4.3.0

MySQL 4.1.12, PostgreSQL 8,

MS SQL-Server 2005

Moodle 1.9

PHP 4.3.0

MySQL 4.1.16, PostgreSQL 8, MSSQL 9.0,

Oracle 9.0

Moodle 2.0

PHP 5.2.8

MySQL 4.1.16, PostgreSQL 8r, MSSQL 9.0,

Oracle 9.0, SQLite 3 (experimentell)

Moodle 2.1 und 2.2

PHP 5.3.2

MySQL 5.0.25 (InnoDB Storage Engine

empfohlen), PostgreSQL 8.3, MSSQL 9.0,

Oracle 10.2, SQLite 2.0

3 Der finnische Softwareentwickler Ulf Michael Widenius war maßgeblich an der Entwicklung von Datenbanksyste-men beteiligt. Die Zugangssprache MySQL – dies ist eine Abkürzung für „My Standard Query Language“ – gehört zu diesen Projekten, an denen Widenius beteiligt war. My ist der Name einer seiner Töchter, die er an dieser Stelle ehrte. Allerdings liegen die Markenrechte von MySQL mittlerweile bei der Firma Oracle. Eine kompatible Weiter -

entwicklung ist MariaDB. Auch hier war wieder eine der Töchter Widenius’ Patin für die Namensgebung des Datenbanksystems.

4 Wie bereits im Text erwähnt, gibt es in der Entwicklung von PHP verschiedene Versionssprünge, die keine Abwärtskompatibilität vorsehen. Aktuell gilt dies für den Sprung auf die PHP-Version 7.x.

3.1 Systemvoraussetzungen

**31**

Moodle-Version

PHP-Mindest-Version4 Datenbank

Moodle 2.3 und 2.4

PHP 5.3.2

MySQL 5.1.33 (InnoDB Storage Engine emp-

fohlen), PostgreSQL 8.3, MSSQL 2005,

Oracle 10.2

Moodle 2.5

PHP 5.3.3

MySQL 5.1.33 (InnoDB Storage Engine emp-

fohlen), PostgreSQL 8.3, MSSQL 2005,

Oracle 10.2, MariaDB 5.2

Moodle 2.6

PHP 5.3.3

MySQL 5.1.33 (InnoDB Storage Engine emp-

fohlen), PostgreSQL 8.3, MSSQL 2005,

Oracle 10.2, MariaDB 5.3.5

Moodle 2.7 bis 2.9

PHP 5.4.4

MySQL 5.5.31, PostgreSQL 9.1, MSSQL

2008, Oracle 10.2, MariaDB 5.5.31

Moodle 3.0

PHP 5.4.4

MySQL 5.5.31, PostgreSQL 9.1, MSSQL

2008, Oracle 10.2, MariaDB 5.5.31

Moodle 3.0.1

PHP 7.1.x

MySQL 5.5.31, PostgreSQL 9.1, MSSQL

2008, Oracle 10.2, MariaDB 5.5.31

Moodle 3.1

PHP 5.4.4 und PHP 7.0, MySQL 5.5.31, PostgreSQL 9.1, MSSQL

_keine_ PHP 7.1.x-Unter-

2008, Oracle 10.2, MariaDB 5.5.31

stützung

Moodle 3.2

PHP 5.6.5, PHP 7.0.x

MySQL 5.5.31, PostgreSQL 9.1, MSSQL

und 7.1.x werden unter-

2008, Oracle 10.2, MariaDB 5.5.31

stützt

Moodle 3.3

PHP 5.6.5, PHP 7.0.x

MySQL 5.5.31, PostgreSQL 9.3, MSSQL

und 7.1.x werden unter-

2008, Oracle 10.2, MariaDB 5.5.31

stützt

Moodle 3.4

**PHP 7.0.0** (!), 7.1.x und MySQL 5.5.31, PostgreSQL 9.3, MSSQL

13.11.2017

7.2.x werden unterstützt 2008, Oracle 10.2, MariaDB 5.5.31

Moodle 3.5

PHP 7.0.0, 7.1.x und

MySQL 5.5.31, PostgreSQL 9.3, MSSQL

17.05.2018

7.2.x werden unterstützt 2008, Oracle 10.2, MariaDB 5.5.31

Moodle 3.6

PHP 7.0.0, 7.1.x bis

MySQL 5.6, PostgreSQL 9.4, MSSQL 2008,

03.12.2018

7.3.x werden unterstützt Oracle 11.2, MariaDB 5.5.31

Moodle 3.7

PHP 7.1.0, 7.2 und 7.3.x MySQL 5.6, PostgreSQL 9.4, MSSQL 2008,

20.05.2019

werden unterstützt

Oracle 11.2, MariaDB 5.5.31

Moodle 3.8

PHP 7.1.0, 7.2 und 7.3.x MySQL 5.6, PostgreSQL 9.4, MSSQL 2012,

18.11.2019

werden unterstützt

Oracle 11.2, MariaDB 5.5.31

**Eigenschaften verschiedener Moodle-Versionen**

Für jede Moodle-Version gelten andere Systemvoraussetzungen und jede

Moodle-Version bringt neue Leistungsmerkmale mit sich. In den sogenannten _Release Notes_ der Moodle-Dokumentation sind die Details vermerkt. Sie sind für ältere Versionen nicht sofort und einfach im Menü zu finden. Sie lassen sich jedoch direkt über die Web-Adresse aufrufen. Wichtig hierbei:

**32** 3 Der Moodle-Server

Die Platzhalter X und Y müssen durch die gewünschte Versionsnummer

ersetzt werden!

**Für Moodle 3.x:**

https://docs.moodle.org/dev/Moodle_X.Y_release_notes [Enter]

**Für Moodle 2.x:**

https://docs.moodle.org/XY/de/Installation_von_Moodle [Enter]

■

**■**

**■ 3.2■Webserver-Hardware**

Unabhängig davon, ob man einen eigenen Webserver betreiben oder sich Webspace bei einem Provider anmieten möchte, muss man sich über das Teilnehmervolumen im Moodle-System im Klaren sein. Universitäten und Institutionen mit voraussichtlich mehreren tausend Usern brauchen hochleistungsfähige Maschinen, zu deren Qualitätsmerkmalen auch _Ausfallsicherheit_ und _Skalierbarkeit_ gehören. Das dafür erforderliche Know-how bringen in der Regel die in solchen Institutionen vorhandenen IT-Abteilungen und deren Mitarbeiterinnen und Mitarbeiter mit.

Die wesentliche Anforderung an die Hardware ist der Speicherplatz. Auf der Festplatte werden 160 MB als Minimum empfohlen. Für ein praktisch einsetzbares System reicht dies allerdings bei Weitem nicht aus. Die offiziellen Moodle-Dokumentationen empfehlen, mindestens fünf Gigabyte Festplattenspeicher zu reservieren. Es sollte allerdings an die Zukunft gedacht werden, in der sich zunehmend mehr multimediale Lehrmittel etablieren werden.

Diese Materialien benötigen große Speicherreserven! Das Linux-Betriebssystem unterstützt sehr flexible Dateiformate, mit denen Datenträgergrößen über mehrere physische Speichermedien dynamisch erweitert werden können. So gibt es den _**L**ogical **V**olume **M**anager_ (LVM), mit dessen Hilfe „logische Partitionen“ über mehrere physische Laufwerke hinweg definiert werden können.

Ein zusätzlicher Speicherplatz, der nicht direkt für den Betrieb des Moodle-Systems verwendet wird, sollte in gleicher Größe für Datensicherungen zur Verfügung stehen. Nichts wäre besonders im Bildungssystem ärgerlicher, als würden persönliche Daten von Lehrenden und Lernenden oder auch Unterrichtsmaterialien ver loren gehen. Darüber hinaus kann Datenverlust zu rechtlichen Problemen führen, wenn beispielsweise prüfungsrelevante Abgaben für einen bestimmten Termin festgelegt wurden und die Unterlagen infolge einer Störung verloren gehen. Regelmäßige Datensicherungen – das bedeutet in der Regel mindestens einmal täglich – sind für ein Moodle-System ausgesprochen wichtig.

3.2 Webserver-Hardware

**33**

Maßgeblich für die Geschwindigkeit des Moodle-Systems ist neben einer ausreichend schnellen Netzanbindung5 vor allem der Arbeitsspeicher (RAM). Für ein einfaches Testsystem wird möglicherweise die Mindestanforderung von 256 MB RAM ausreichend sein, wie es in der Moodle-Dokumentation empfohlen wird. Es sei allerdings darauf hingewiesen, dass selbst Desktop-Computer mit einem der artig geringen Arbeitsspeicher heute keinesfalls mehr zeitgemäß sind. Die Moodle-Dokumentation empfiehlt als „Faustformel“ 1 GB

RAM pro zehn bis 20 gleichzeitig auf das System zugreifende Benutzer vorzusehen.

**User-Zahl für den _gleichzeitigen_** **Zugriff**

Es ist zu beachten, dass in der Regel nicht alle im System angemeldeten

Benutzerinnen und Benutzer zur gleichen Zeit auf das System zugreifen werden.

Für die technischen Grenzen ist jedoch nur die Zahl der _zeitgleich aktiven_ Benutzerinnen und Benutzer relevant. Damit kann die Zahl der im Moodle

angemeldeten Personen erheblich größer geplant werden. Wie das Verhältnis genau zu dimensionieren ist, hängt vom Volumen der Nutzung ab.

■

Eine gern gestellte Frage nach der Anzahl der Benutzer und deren gleichzeitiger Präsenz im System lässt sich natürlich nicht pauschal beantworten. Es gibt keine Faustformel, mit der seriös das System anhand der maximal regis trierten User-Zahl kalkuliert werden kann.

Zwei Beispiele sollen dies verdeut lichen:

Im ersten Fall wird eine Schule mit 600 Schülerinnen und Schülern angenommen. Der Schwerpunkt liegt im Präsenzunterricht und Moodle soll lediglich die Lehre unterstützend eingesetzt werden. Das bedeutet, dass neben der Bereitstellung von Lehrmaterialien und der kontrollierten Abgabe von Hausaufgaben auch einige vertiefende Informationen für den Unterrichtsstoff angeboten werden. In diesem System ist die durchschnittliche Verweildauer eher überschaubar.

Im zweiten Fall soll ein auf direkten Online-Unterricht spezialisiertes Schulungsunterneh-men angenommen werden. Die Lehrinhalte werden ausschließlich über das Internet angeboten (Download möglich), jedoch in Form von virtuellen Klassenräumen online auch zwischen den Teilnehmerinnen und Teilnehmern des Kurses diskutiert. In diesem Fall muss nicht nur von einer sehr hohen aktiven Teilnehmerdichte im System ausgegangen werden, es müssen auch Ressourcen für die Kollaborationsmodule – sofern diese auf dem eigenen System betrieben werden – kalkuliert werden.

5 Eine ausreichend schnelle Anbindung an das Internet bieten nahezu alle gängigen Provider. Bei Abschluss eines Vertrags sollte die Übertragungsrate sowie eine Verfügbarkeitsklausel (Ausfallsicherheit) berücksichtigt werden.

Darüber hinaus nimmt die Verbreitung von Lichtwellenleiter-Anschlüssen mittlerweile stark zu. Diese lassen in Verbindung mit einer festen IP-Adresse auch den direkten Anschluss eines hauseigenen Webservers zu, auf dem das Moodle-System installiert wird. Alternativ zur festen IP-Adresse können auch Dienste eines dynamischen DNS

(Domain Name Services) eingekauft werden, um den Webserver gezielt im Internet erreichbar zu machen. Der Betrieb eines eigenen Servers (Hardware) erfordert umfassendes Know-how zur IT-Sicherheit.

**34** 3 Der Moodle-Server

**Lieber „klotzen“ als „kleckern“**

Arbeitsspeicherbausteine (RAM-Module) sind heute nicht mehr teuer. RAM-Bausteine sind bereits ab 5 € bis 10 € pro Gigabyte erhältlich. Für Server empfiehlt es sich allerdings auf Qualität zu achten, denn diese Geräte laufen im Gegensatz zu Desktop-Computern permanent. Eine Kühlung ist durchaus empfehlenswert.

Auch die Speichertaktfrequenz ist zu beachten. Diese sowie die übrigen Daten des bzw. der erforderlichen RAM-Module (Speichertyp/Formfaktor etc.) sind dem Datenblatt des Computer-Mainboards zu entnehmen. Auf keinen Fall sollte die Aufrüstung des Arbeitsspeichers von Laien vorgenommen werden.

■

Die folgende Tabelle gibt eine Orientierungshilfe für die Dimensionierung des Serverspei-chers, wie er in seiner Hardware auszustatten oder beim Provider zu be stellen ist (unverbindliche Empfehlung).

**Tabelle 3.2** Kalkulationshilfe zur Hardware-Planung (Speicherplatz zzgl. zum Betriebssystem) Systemgröße (User)

Speicherplatz (Platte) Speicher (Backup) RAM-Speicher

10 (Testumgebung)

1 GB

1 GB

1 GB bis 4 GB

50 (kleine Schule)

5 GB bis 10 GB

5 GB bis 10 GB

4 GB bis 16 GB

100 (mittlere Schule)

10 GB bis 50 GB

10 GB bis 50 GB

8 GB bis 32 GB

**■**

**■ 3.3■Webserver-Software**

Neben der Hardware-Ausstattung eines Servers benötigt dieser auch eine passende Software-Umgebung. Zu empfehlen ist für Moodle grundsätzlich ein Server auf der Basis von Linux. Auf diesem System wird Moodle entwickelt. Das System läuft allerdings auch auf (kommerziellen) Windows-Servern. Hier sind entsprechende Lizenzkosten zu kalkulieren.

Auch weitere Betriebssysteme wie Solaris oder Mac OS können geeignet sein, was allerdings individuell zu testen ist.

3.3 Webserver-Software

**35**

**3.3.1■Webserver**

Kern der Installation ist zunächst einmal ein geeigneter _Webserver_. Kostenlos6 verfügbar (keine Lizenzkosten) ist der _Apache-Webserver,_ der neben dem Internet Information Server7

(IIS) von Microsoft weltweit eine dominante Rolle in der Bereit stellung von Internet-Publikationen spielt. Daneben gibt es verschiedene weitere Webserver-Lösungen, die jedoch meist noch nicht offiziell mit einem Moodle-System getestet wurden. Für den Einsatz in Produktiv-Systemen ist hier Vorsicht geboten.

**3.3.2■PHP-Versionen und PHP-Erweiterungen**

PHP8 ist eine auf dem Server laufende Skriptsprache. Das bedeutet, dass auf dem Webserver ein sogenannter _PHP-Parser_ 9 aktiv sein muss, der in der Lage ist, PHP-Code zu interpretieren.

**3.3.2.1■PHP-Sprung auf Version 7**

PHP wurde seit der Einführung im Jahr 1995 diverse Male aktualisiert und über arbeitet.

Ende November 2019 wurde die Version PHP 7.4.0 freigegeben. Das Problem bei Sprachen – vor allem bei Programmiersprachen – ist nun, dass die darauf basierende Verstän-digung nur dann funktioniert, wenn beide Seiten mit dem gleichen Wortschatz arbeiten.

Menschen sind in der Lage zu „improvisieren“. Computer können das nicht. Im Gegenteil sogar beinhalten Programmiersprachen feste Regeln von Anweisungen und Definitionen, die nur wenig Interpretationsspielraum zulassen. Anders als bei der menschlichen Kommunikation können mit der Verabschiedung neuer „Sprach-Versionen“ durchaus Definitionen entfallen. Das bedeutet: Computer erkennen einen Code nicht mehr, der in einer früheren Version absolut gültig oder zumindest noch „geduldet“10 war.

Moodle betrifft dies nun direkt! Seit 2004 waren PHP-Versionen 5.x (x steht für verschiedene Überarbeitungen im Laufe der Zeit) quasi der Standard in der Web-Entwicklung auf Seiten des Webservers. Mittlerweile ist Version 7.x gültig und hat die 5er-Versionen völlig 6 Wird beim Betriebssystem (Linux) und beim Webserver (Apache) von „kostenlos“ gesprochen, so sind damit eventuelle Lizenzkosten gemeint. Bei kommerziellen Betriebssystemen fallen durchaus bereits bei der Anschaffung Kosten an. Grundsätzlich wird eine saubere betriebswirtschaftliche Kalkulation jedoch auch die Administration und die technische Wartung berücksichtigen, was sich insbesondere in Personalkosten oder in Entgelten des Providers niederschlägt.

7 Der Internet Information Server™ (IIS™) ist eine Marke von Microsoft.

8 PHP ist eine (rekursive) Abkürzung für _**P**_ HP _**H**_ ypertext _**P**_ reprocessor. Diese Form der Abkürzungen, welche die Abkürzung ihrerseits in der ausgeschriebenen Form enthalten, ist insbesondere in der Entwicklerszene quelloffener Software häufig zu finden. Über Sinn und Unsinn bzw. über die Philosophie derartiger Schreibstile kann nur spekuliert und leidenschaftlich diskutiert werden.

9 PHP unterscheidet sich damit deutlich von einer anderen gängigen Skriptsprache, die im Webdesign zum Einsatz kommt: JavaScript. JavaScript wird im Browser – dem Darstellungsprogramm für Webseiten auf dem PC – ausgeführt. Aus Sicherheitsgründen hat somit JavaScript keinen direkten Zugriff auf serverseitige Datenbanken.

PHP hingegen hat diese Möglichkeiten.

10 In Programmiersprachen werden Syntax-Änderungen meist nicht spontan und ohne Vorwarnung umgesetzt. Die Entwickler müssen allerdings beachten, dass verschiedene Code-Elemente als „veraltet“ oder „unerwünscht“

gekennzeichnet sind, wenn die Software auch künftig funktionsfähig bleiben soll.

**36** 3 Der Moodle-Server

abgelöst. Es gibt keine gesicherte Abwärtskompatibilität mehr! Das hat einerseits gute Gründe, führt aber auch zu Kompatibilitätsproblemen mit älteren Internet-Publikationen, u. a. bei Moodle!

**PHP 5.x und PHP 7.x sind grundlegend verschieden!**

Bei der Installation von Internet-Software, die auf PHP basiert, müssen unbedingt die Systemvoraussetzungen beachtet werden! Für PHP 5.x entwickelte Lösungen werden meist nicht mehr auf PHP 7.x funktionieren! Eine Entscheidung zugunsten der veralteten Plattform ist aus Sicherheitsgründen

nicht sinnvoll!

■

Der wichtigste Unterschied zwischen PHP 5.x und PHP 7.x ist vor allem im Zugriff auf Datenbanken zu sehen, die nicht zuletzt für den Betrieb eines Moodle-Systems unabdingbar sind. Obwohl die PHP-Erweiterung _mysql_ und der darin enthaltene Funktionsumfang bereits mit der Version PHP 5.x als „veraltet“ eingestuft wurde, setzen viele Entwickler bis zuletzt auf die ihnen vertrauten Verfahren zur Kom munikation mit Datenbanken. Parallel dazu gab es aber bereits mit der Version PHP 5.1 die Alternative, _PHP Data Objects_ (PDO) zu verwenden. Beide Verfahren erfüllen zwar den gleichen Zweck (die Kommunikation mit einer Datenbank), jedoch ist deren Syntax (Schreibweise) vollkommen verschieden.

Versionsunterschiede gibt es auch in anderen Bereichen, sodass es kaum wirtschaft lich sinnvoll ist, ältere Installationen 1 : 1 auf neue Plattformen zu migrieren. Der sinnvolle Ansatz wird im Fall von Moodle darin zu sehen sein, Kursdaten aus älteren Umgebungen zu exportieren und in aktuelle Systeme zu importieren. Ganz ohne Kompromisse ist aber auch dies in den meisten Fällen nicht zu erreichen.

**Migration oder Neu-Installation?**

Diese Frage stellt sich häufig, wenn man von einem Moodle-System spricht, das derzeit noch auf einem veralteten Server läuft: In der Regel wird allein aus Sicherheitsgründen der Umstieg auf eine neue Plattform anzustreben

sein. Die veraltete Installation in neue Systeme zu migrieren ist allerdings nur selten wirklich umsetzbar, weil Moodle und deren Erweiterungen (Plugins) nicht immer zeitnah und schon gar nicht parallel entwickelt werden.

■

**3.3.2.2■PHP-Erweiterungen für Moodle**

Neben verschiedenen Standard-Funktionen und Programmbibliotheken sieht PHP auch eine Reihe von Erweiterungen vor, die zusätzliche Leistungsmerkmale bieten. Moodle ist hier sehr anspruchsvoll und verlangt durchaus die Aktivierung einer Reihe von Erweiterungen des PHP-Parsers.

3.3 Webserver-Software

**37**

**Tabelle 3.3** PHP-Erweiterungen für ein Moodle-System11

Name

Notwendigkeit Bedeutung/Aufgabe

ctype

erforderlich

Überprüfung von Zeichen, ob es sich dabei um alpha numerische

Zeichen handelt.

cURL

erforderlich

„Client for Uniform Resource Locator“ – Werkzeug zum Download

von Daten, deren Ursprung über Webadressen angesprochen

wird.

dom

erforderlich

Unterstützung des „Document Object Model“ für den Zugriff auf

XML-Dokumente.

gd

erforderlich

Bibliothek mit Programmfunktionen, die es gestattet, dynamisch

Grafiken zu erzeugen und zu bearbeiten.

iconv

erforderlich

Konvertierung zwischen verschiedenen Zeichensätzen – ein

Computer kennt keine Buchstaben, sondern nur dafür vor-

gesehene Codes. Die Zuordnung zu Zeichensätzen erzeugt das,

was Menschen letztlich auf dem Bildschirm sehen.

json

erforderlich

PHP-Erweiterung für JavaScript Object Notation (JSON) – hier

handelt es sich um den PHP-seitigen Gegenpart einer direkten

Kommunikation zwischen Webserver und Browser, ohne eine

Webseite für die inhaltliche Aktualisierung neu aufbauen zu

müssen.

intl

Empfehlung

Internationalisierungsmodul für PHP.

mbstring

Empfehlung

Unterstützung von Zeichenketten, deren einzelne Zeichen in

mehreren Byte codiert werden (Multibyte String).

openssl

Empfehlung

Ver- und Entschlüsselung.

pcre

erforderlich

„Perl Compatible Regular Expressions“ – die Erweiterung bietet

u. a. Funktionen zur Suche nach bestimmten Ausdrücken. Diese

orientieren sich an den Funktionen der Programmiersprache

Pearl.

simplexml erforderlich

Erweiterung für die Auswertung von Informationen in einem

XML-Dokument.

soap

Empfehlung

SOAP steht für Simple Object Access Protocol – ein Protokoll,

welches zum (XML-)Datenaustausch dient.

spl

erforderlich

SPL steht für Standard PHP Library – in aktuellen PHP-Ver sionen

ab 5.0 ist diese Bibliothek grundsätzlich in PHP vorhanden.

tokenizer

Empfehlung

Verschiedene PHP-Operationen werden Parser-intern durch

„ Token“ beschrieben. In der Regel wird der normale Program-

mierer damit nur selten in direkten Kontakt kommen, es sei denn,

er muss Warnungen oder Fehlermeldungen interpretieren.

_(Fortsetzung nächste Seite)_

11 Quelle der Erweiterungsliste: Moodle-Dokumentation – zusätzlich: freie Erklärung der Erweiterungen.

**38** 3 Der Moodle-Server

**Tabelle 3.3** PHP-Erweiterungen für ein Moodle-System _(Fortsetzung)_ Name

Notwendigkeit Bedeutung/Aufgabe

xmlrpc

Empfehlung

XML-RPC steht für Extensible Markup Language Remote

Procedure Call. Es handelt sich um ein – in XML-Paketen über-

tragenes – Protokoll zum Aufruf von Prozeduren/Unterprogram-

men über ein Netzwerk. SOAP gilt als eine Weiterentwicklung von

XML-RPC.

xml

erforderlich

XML steht für Extensible Markup Language. Es handelt sich um

ein einfaches Protokoll zur (textbasierten) Übertragung von

Daten. Die Informationen werden zwischen einem Start-Tag (zeigt

den Beginn der Information an) und einem Schluss-Tag gesetzt.

Die Syntax zwischen den kommunizierenden Partnern orientiert

sich an den Festlegungen des Programmierers.

zip

erforderlich

PHP-Erweiterung zum Packen bzw. Entpacken „gezippter“

Archive. ZIP ist auch auf Windows-Computern einer der am

weitesten verbreiteten Standards zur Kompression von Dateien.

Fehlende Erweiterungen müssen unter Umständen nachträglich installiert werden. So kann beispielsweise das PHP-Modul des Apache-Webservers mit folgender Kommandozeile (auf einem Linux-System) installiert werden:

sudo apt-get install libapache2-mod-php [Enter]

Der Linux-Befehl _sudo_ – meist gefolgt von der Eingabe des Administrator-Passwortes –

bewirkt die Ausführung der Kommandozeile mit den Rechten des Superusers (root). Es ist somit kein erneutes Login im System zum Wechsel des Benutzers erforderlich.

Besitzt das Betriebssystem eine grafische Benutzeroberfläche – so, wie es im Ex perimentalsystem der Fall ist – kann auch ein grafischer Paketmanager wie zum Beispiel _synaptic_ verwendet werden. Sowohl _apt-get_ als auch _synaptic_ erkennen Zusammenhänge zu möglicherweise zusätzlich benötigten Programmpaketen und bieten diese ebenfalls zur Installation an. Derartige Tools erleichtern auch die Analyse des Systems. Dazu werden Stichwörter in eine Suchfunktion eingetragen und dann die Ergebnisliste untersucht. Ist ein erforderliches Paket noch nicht installiert, wird es vorgemerkt. Sobald alle erforderlichen PHP-Erweiterungen sowie die sonstigen noch benötigten Pakete überprüft wurden, wird mit einem Klick auf _Anwenden_ die Installation ausgeführt.

**3.3.2.3■php.ini im System finden**

Neben der gezielten Installation eventuell fehlender Programmpakete müssen die PHP-Erweiterungen zusätzlich auch _aktiviert_ werden! Dies geschieht durch eine im Grunde genommen recht einfache Bearbeitung der Datei _php.ini_. Für den Laien besteht die Schwierigkeit vor allem darin, diese Datei zu finden. Folgende Voraussetzungen müssen zur Bearbeitung der Datei _php.ini_ erfüllt sein:

Die Administration muss in der Lage sein, die Datei im System aufzufinden, um sie be -

arbeiten zu können.

Es muss ein geeigneter Editor verwendet werden.

Die Datei ist mit Administratorrechten zu öffnen und zu speichern.

![Image 4](index-62_1.png)

3.3 Webserver-Software

**39**

Allein der erste Punkt wird gelegentlich für Schwierigkeiten sorgen, denn auf einem Computer existieren Tausende von Dateien in unzähligen Verzeichnissen und Unterverzeichnissen. Auch für den eingeweihten IT-Kenner ist es nicht immer ganz einfach, die Datei zu finden, denn das Betriebssystem Linux wird in verschiedenen Distributionen angeboten und nicht alle Systeme setzen in den Details auf die gleiche Verzeichnisstruktur.

Natürlich gibt es Hilfe bei der Suche. Im Windows Explorer existiert zum Beispiel ein Suchfeld, in das einfach der Name der gesuchten Datei eingegeben werden kann. Es ist zu beachten, dass auch die Unterverzeichnisse durchsucht werden. Zeit spart dabei, wer ungefähr eine Vorstellung hat, auf welchem Laufwerk die Datei _php.ini_ installiert ist. Das gilt übrigens grundsätzlich, also auch für die Suche in einem Linux-System.

**Bild 3.1** Auf einem Windows-System eine Datei zu finden, ist nicht schwierig. Im Windows-Explorer gibt es ein Suchfeld.

Wer ein Testsystem auf einem Windows-Computer betreiben möchte, welches in einem _lokalen_ XAMPP12-Serversystem installiert werden soll, findet die Datei _php.ini_ sehr schnell: Mit der Installation des XAMPP-Programmpakets wird ein Verzeichnis auf dem Laufwerk C:\ mit dem Namen _xampp_ angelegt. In diesem Verzeichnis existiert nun ein Unterverzeichnis mit dem Namen _php_. Darin befindet sich die Datei _php.ini_. Der vollständige Suchpfad lautet also bei einer XAMPP-In stallation auf einem MS-Windows-System:

C:\xampp\php\php.ini

12 XAMPP ist eine Abkürzung. Dabei steht X für ein nahezu beliebiges Betriebssystem (Windows, Linux oder Mac OS X). A steht für den Webserver Apache2, M ist das Kürzel für die MariaDB-Datenbank und PP steht für die Interpreter der Programmiersprachen Pearl und PHP.

![Image 5](index-63_1.png)

**40** 3 Der Moodle-Server

**Achtung: XAMPP ist nicht für Live-Systeme vorgesehen!**

Mit XAMPP kann wirklich jeder einen voll funktionsfähigen Webserver auf dem eigenen Computer installieren. Auch die in diesem Werk vorgestellten Moodle-Installationen können auf einer XAMPP-Umgebung umgesetzt und studiert

werden. Allerdings – so einfach und komfortabel ein XAMPP-Server-System auch zu installieren ist – ist dieser Server ohne professionelle Konfiguration nicht für öffentlich zugängliche Live-Systeme geeignet. XAMPP ist als Schulungs- bzw.

Trainingsumgebung gestaltet worden. Das bedeutet, dass grundsätzlich kein Passwortschutz existiert, und wenn doch, dann nur aus gesprochen rudimentär.

Datenbanken und Server-Dateien sowie die Daten verzeichnisse sind also angreifbar, um nicht zu sagen „offen wie das (sprichwörtliche) Scheunentor“! Für eigene Studien und Übungszwecke ist XAMPP allerdings ein wunderbares und außer-dem zu realen Serverumgebungen kompatibles Instrument. Es wird deswegen auch bei der Beschreibung eines eigenen Testsystems vorgestellt.

■

Vergleichbare Möglichkeiten findet man auch in einem Linux-System. Auf einer grafischen Oberfläche gibt es je nach Distribution und installierter Oberfläche (z. B.: GNOME, KDE) dem Explorer in dessen Grundfunktion ähnliche Werkzeuge mit einer Suchfunktion. In professionellen Serverumgebungen wird allerdings meist auf der Kommandozeile gearbeitet. Das Kommando lautet _locate_.

**Bild 3.2** Die Datei php.ini ist in einer XAMPP-Testumgebung direkt zu finden. Der Pfad heißt: _C:\xampp\php\php.ini_

![Image 6](index-64_1.png)

![Image 7](index-64_2.png)

3.3 Webserver-Software

**41**

**Bild 3.3** Auch in einem Linux-System kann in einem grafischen Assistenten nach einer Datei gesucht werden.

**Bild 3.4** 

Linux wird meist mit der Shell,

der Kommandozeile, asso ziiert

und ist deswegen unter IT-Laien

eher berüchtigt als berühmt.

Dennoch führt ein sehr einfacher

Befehl in der Shell schnell zum

Ziel: locate php.ini Enter

Etwas komplizierter wird es möglicherweise, wenn preisgünstige Standard-Web space-Pakete bei einem großen Provider angemietet werden. Das Problem ist dabei: Die Datei _php.ini_, die zur Aktivierung von PHP-Erweiterungen bearbeitet werden muss, liegt meist außerhalb des Zugriffsbereichs des Kunden. Hinzu kommen möglicherweise Probleme bei der Einrichtung eines Datenverzeichnisses, wie es Moodle erwartet.

**Öffentlicher Webspace ist ein eigenes Thema**

Die Nutzung eines angemieteten Webspaces in einem Rechenzentrum eines

öffentlichen Internet-Dienstleisters ist für kleinere Anbieter von Bildungs-dienstleistungen (freie Fachtrainer, kleine Schulen etc.) ein durchaus

geeigneter und vor allem kostengünstiger Weg. Dieses Thema wird deswegen an späterer Stelle in diesem Kapitel eingehender behandelt.

■

**42** 3 Der Moodle-Server

**3.3.2.4■php.ini bearbeiten**

Es sei angenommen, die für die Aktivierung von PHP-Erweiterungen wichtige Datei php.ini sei im System gefunden worden. Nun gilt es, diese zu bearbeiten. Gleich vorweg eine Ent-warnung: Es ist nicht nötig, sich mit einer komplizierten Programmiersprache vertraut zu machen! Das Wichtigste ist bereits in die Datei hinein geschrieben worden. Es sind nur Kleinigkeiten zu bearbeiten. Dazu benötigt man einen Text-Editor.

**Achtung: Ein Text-Editor ist kein Textverarbeitungsprogramm!**

Es ist keinesfalls eine gebräuchliche Textverarbeitungssoftware wie MS-Word oder LibreOffice Writer für die Bearbeitung der Steuerdateien (z. B. php.ini oder später auch .htaccess) zu verwenden. Diese Programme bilden den Text mit zusätzlichen Informationen – unter anderem für die Formatierung der

Zeichen, Absätze und Seitenlayouts – in den Dateien ab. In der Software-

Entwicklung und in der Administration von Internet-Programmen wird jedoch reiner Text benötigt. Für deren Bearbeitung gibt es eine breite Vielfalt – zum großen Teil kostenloser – sehr guter Programme.

■

Geeignete Editoren sind unter anderem:13

**Für Linux (Kommandozeile):**

ed (ein Klassiker aus „alten“ UNIX-Zeiten)

vi (sehr häufig verwendeter Editor in der Shell)

joe

nano

**Für Linux mit grafischer Benutzeroberfläche:**14

gedit (wird mit der grafischen Oberfläche „GNOME“ geliefert)

Kate (Editor für die KDE-Oberfläche)

KWrite (ehemals DER Standard-Editor der KDE-Oberfläche)

VS Code bzw. Visual Studio Code – ein Microsoft-Editor, der auch für das Linux-Betriebssystem verfügbar ist.

Bluefish – der Editor ist auch für MS-Windows und OS X erhältlich.

**OS X (Apple/Mac)**

Verschiedene unter Linux/UNIX bekannte Editoren für die Kommandozeile15

TextEdit

13 Die Aufzählung erhebt keinen Anspruch auf Vollzähligkeit, bietet jedoch gewiss Werkzeuge für jeden Anspruch.

14 Für das Betriebssystem Linux existieren eine Vielzahl grafischer Benutzeroberflächen, die sich im Layout etwas voneinander unterscheiden und auch verschiedene Standard-Tools mit sich bringen. Die bekanntesten Oberflächen sind KDE und GNOME.

15 Das Betriebssystem OS X für Apple-Computer wie z. B. MacBook ist dem UNIX-System und damit auch Linux sehr nahe. Die Anordnung der Verzeichnisse ist in einer vergleichbaren Struktur realisiert wie bei Linux/UNIX und auch viele Kommandos der Kommandozeile belegen die enge Verwandtschaft der Betriebssysteme. Allerdings ist Mac OS X kein Linux!

3.3 Webserver-Software

**43**

VS Code bzw. Visual Studio Code – ein Microsoft-Editor, der auch für das Mac-Betriebssystem verfügbar ist

Bluefish – der Editor ist auch für Linux und MS-Windows erhältlich.

**MS-Windows**

notepad – der „klassische“ Windows-Editor, der nicht mit dem ähnlich klingenden Programm „Wordpad“ zu verwechseln ist, ist eher nicht zu empfehlen. Zwar erfüllt dieses einfache Programm alle Minimalanforderungen, ist jedoch sehr unkomfortabel in der Benutzung.

notepad++ – hier darf man sich nicht von der Ähnlichkeit im Namen zum vorangehenden Programm täuschen lassen! notepad++ ist ein sehr guter und brauchbarer Editor, der unter anderem so wichtige Funktionen wie Syntax-Highlighting16 bietet.

Atom – ebenfalls ein sehr guter Editor, der mit farblich hervorgehobenen Elementen Pro-grammierfehler zu vermeiden hilft.

VS Code bzw. Visual Studio Code – hierbei handelt es sich um einen sehr leistungsfähi-gen Editor aus dem Hause Microsoft. Der Editor ist auch für OS X und Linux verfügbar.

Bluefish – der Editor ist auch für Linux und OS X erhältlich.

**Welcher Editor ist der beste?**

Es spielt grundsätzlich keine Rolle, welcher Editor – ob einer der hier Genannten oder ein anderes Programm – verwendet wird. Wichtig ist lediglich, dass der Editor den jeweils verwendeten Zeichensatz (z. B. UTF-8) versteht und die Datei auch in diesem Zeichensatz speichern kann. In der Regel kann das auch der ganz einfache Windows-Editor „notepad“ (ohne „++“). Wichtig ist, dass der verwendete Editor zu einem vertrauten Werkzeug wird. Es gibt also keinen

„guten“ und auch keinen „schlechten“ Editor, sondern nur das Werkzeug,

welches der jeweilige Benutzer bzw. die jeweilige Benutzerin bevorzugt.

■

16 Die farbliche Hervorhebung von Kommandos und deren Argumenten erleichtert die Arbeit eines Programmierers ganz wesentlich und hilft, Fehler infolge banaler Schreibfehler zu vermeiden. Fast jeder moderne Editor, der als Programmierwerkzeug eingesetzt wird, bietet das sogenannte _Syntax Highlighting_.

![Image 8](index-67_1.png)

![Image 9](index-67_2.jpg)

**44** 3 Der Moodle-Server

**Bild 3.5** Obwohl der Editor Visual Studio Code ein Produkt der Firma Microsoft ist, wird er auch für andere Betriebssysteme – hier am Beispiel von Ubuntu-Linux – angeboten. Dies gilt auch für verschiedene andere Editoren!

**Bild 3.6** Unten rechts ist die Programmverknüpfung zu Visual Studio Code im Anwendungs-verzeichnis der Linux-Oberfläche zu sehen. Softwareinstallationen auf einem Linux-Computer sind nicht mehr unbedingt komplizierter als auf einem Windows-PC!

![Image 10](index-68_1.png)

3.3 Webserver-Software

**45**

Sind alle erforderlichen PHP-Erweiterungen (in der richtigen Version) im System installiert, so müssen sie lediglich in der Datei _php.ini_ aktiviert werden. Die Datei _php.ini_ ist die zentrale Steuerdatei des PHP-Parsers. Es gibt allerdings – wie bereits beschrieben – keinen allgemein verbindlichen Speicherort. In den in diesem Werk beschriebenen Testsystemen findet man die Datei _php.ini_ in den folgenden Verzeichnissen:

XAMPP-Umgebung auf einem MS-Windows-Betriebssystem:

C:\xampp\php\php.ini

XAMPP (Moodle Installer Package17, ebenfalls auf einem MS-Windows-System): C:\Users\Nutzer\Desktop\Moodle_3-9_XAMPP\server\php\php.ini

Linux (Ubuntu-Linux 18.04.3 LTS): /etc/php/phi.ini

Die Aktivierung der geforderten Erweiterungen ist nun sehr einfach: Es wird lediglich das Semikolon gelöscht, welches sich am Beginn der Code-Zeile befindet. Ein Semikolon leitet einen einzeiligen Kommentar ein. Alles, was dem Semikolon folgt, wird also vom System ignoriert. Löscht man aber das führende Semikolon, so wird die Code-Zeile aktiv gesetzt.

**Bild 3.7** PHP-Erweiterungen werden in der Datei php.ini aktiviert, in dem das Semikolon am Beginn der Zeile gelöscht wird. Mit einem vorangestellten Semikolon wird ein Eintrag „aus kommentiert“.

Er ist damit nicht aktiv.

17 In diesem Fall wurde das Moodle-Installer Package für Windows mit der (hier: noch) Alpha-Version 3.9 verwendet.

Dieses erzeugt auf dem Windows-PC ein nahezu autarkes „to-go“-System. Es unterscheidet sich also von einer separaten XAMPP-Server-Installation, auf der Moodle ebenfalls installierbar ist.

**46** 3 Der Moodle-Server

**Ganz wichtig: Als Systemverwalter arbeiten!**

Die Datei php.ini ist eine Systemdatei! In einem Linux-System muss sie also mit den Rechten des Systemverwalters bearbeitet werden, sonst lässt sie

sich nicht speichern. In Beispiel (Bild 3.7) wurde das Editor-Programm Gedit verwendet. Damit es sicher mit Administratorrechten arbeitet, wurde der

Editor über die Kommandozeile mit einem vorangestellten sudo-Kommando

gestartet:

sudo gedit /etc/php/php.ini [Enter]

■

In der Datei _php.ini_ sind noch weitere wichtige Konfigurationen vorzunehmen. Dies betrifft die Möglichkeit, über die Moodle-Oberfläche Dateien auf das System hochzuladen, ohne dazu beispielsweise ein FTP-Programm nutzen zu müssen. Der Dateiumfang für Lehrmaterialien (E-Books, Video-Dateien etc.) kann durchaus beachtliche Größen umfassen.

Damit auch große Dateien im Moodle-System gespeichert werden können, müssen mindestens zwei Werte in der Datei _php.ini_ bear beitet werden:

_upload_max_filesize:_ maximale Größe einer einzelnen hochzuladenden Datei.

_post_max_size:_ maximale Größe einer Variablen im $_POST[]-Array des Webservers, welches von PHP zur Übernahme von Dateien mittels eines Web-Formulars verwendet wird.

Zusätzlich können Anpassungen in folgenden Parametern der Datei _php.ini_ sinnvoll sein:

_max_execution_time:_ zeitliche Begrenzung der Ausführung eines PHP-Skripts. Der Grenzwert ist möglicherweise bei sehr großen zulässigen Dateigrößen und einer hohen Benutzerzahl, die gleichzeitig auf den Server zugreifen dürfen, nach oben anzupassen.

_max_input_time:_ Zeit, mit der sich ein Skript mit einem Eingabeprozess be fassen darf. Bei größeren Dateien, mehreren gleichzeitigen Server-Zugriffen und langsamen Kommunika-tionswegen kann es sinnvoll sein, diesen Wert nach oben zu korrigieren.

_memory_limit:_ Teil des für PHP reservierten Arbeitsspeichers. Hier sollte die Großzügig-keit nicht übertrieben werden. Zu klein sollte dieser Wert jedoch auch nicht bemessen werden. Heute werden oft schon 128M (entspricht 128 Mbyte) in der Grundeinstellung festgelegt. Dieser Wert sollte in der Regel ausreichen und ist nur zu erhöhen, wenn die Performance in der serverseitigen Bearbeitung der PHP-Skripte zu gering ist.

Welche Werte verwendet werden, muss aus den Erfahrungen heraus ermittelt werden. Insbesondere die zeitlichen Grenzen und die Reservierung von Arbeitsspeicher hängen von der Auslastung des gesamten Servers und nicht zuletzt von dessen Systemressourcen ab.

Die Festlegung der maximal hochladbaren Dateigröße kann bereits mit 15 Mbyte bis 20 Mbyte vernünftig definiert werden. In der Praxis sind aber auch andere Werte wie zum Beispiel 50 Mbyte und mehr denkbar. Es kommt hier vor allem darauf an, welche Art von Unterrichtsmaterialien eingesetzt werden. Wird nur mit reinen Texten, überschaubaren PDF-Dateien und kleineren Präsentationen gearbeitet, dann sollte ein kleiner Grenzwert für die Dateigröße völlig ausreichen. Wird das Lernsystem jedoch zur Ausbildung von Infor-matikern oder Personen eingesetzt, die große Dateipakete als Archiv verwenden bzw. mit hochauflösendem Foto- und Videomaterial arbeiten, so ist die Festlegung der Grenzwerte unbedingt mit den Lehrenden zu klären und gegebenenfalls sehr großzügig zu bemessen.

Doch Achtung: Es muss auch für ausreichend großen Speicherplatz auf dem System und auf

![Image 11](index-70_1.png)

3.3 Webserver-Software

**47**

den Backup-Medien gesorgt werden! Mit den minimalen Systemvoraussetzungen kann eine solche Lernplattform dann nicht mehr betrieben werden.

**Server-Neustart erforderlich!**

Jede Veränderung am Webserver, dem PHP-Parser oder dem Datenbank-

management erfordert einen Neustart des Webservers. Auch dieser wird in

einem Linux-System über die Kommandozeile durchgeführt:

sudo /etc/init.d/apache2 restart [Enter]

■

Nach jeder Änderung des Webservers ist dessen Neustart erforderlich. Auf einer XAMPP-Test umgebung ist das sehr komfortabel über das XAMPP Control Panel möglich: Der Server wird einfach gestoppt und gleich darauf neu gestartet. Auf einem Linux-System arbeitet man mit einem Befehl auf der Kommandozeile (siehe Kasten).

**Bild 3.8** Das XAMPP Control Panel bietet Schaltflächen, mit denen gezielt Serverdienste gestoppt und neu gestartet werden können.

**3.3.3■Datenbanken**

Die einfachste Form einer Datenbank ist wohl der klassische Karteikasten. Auf den Karten stehen die eigentlichen Informationen – die „Daten“. Damit man sich in der Fülle dieser vielen Daten zurechtfinden kann, wird eine gewisse Ordnung benötigt. Bei den Kartei kästen waren es Regeln, nach denen diese selbst und die darin gespeicherten Daten organisiert wurden. Auch gab es möglicherweise Verzeichnisse, in denen strukturierte Informationen erfasst wurden, die das Auffinden der rich tigen Karteikarte erleichtern. Natürlich bedurfte es in der analogen „Papierzeit“ auch ein gewisses Maß an persönlicher Arbeitsleistung die Karteikarten zu sortieren und beispielsweise Daten bestimmter Jahrgänge oder Wohnge-biete auf dem neuesten Stand zu halten.

**48** 3 Der Moodle-Server

In der modernen IT werden Daten längst elektronisch erfasst und verwaltet. Der Datenbestand wird auf Speichermedien abgelegt. Dazu ist es erforderlich, jedem einzelnen Datensatz, den man sich als Zeile einer Tabelle vorstellen kann, eine bestimmte Struktur zu geben. Dazu gehören unter anderem die Breite der Datenfelder, die Art, wie die Daten gespeichert werden (z. B. Zeichenketten bzw. Strings, ganze Zahlen, Gleitkommazahlen usw.), aber auch der zu verwendende Zeichensatz.

Die Struktur, mit welcher der Datenbestand gespeichert wird, legt ein _Datenbankmanage-mentsystem_ (DBMS) an. Es koordiniert auch die Vorgänge beim Ergänzen oder Löschen von Daten. Besonders wichtig ist die Aufgabe eines DBMS, wenn gleich mehrere Benutzer auf die Datenbank zugreifen wollen. In einem Lern managementsystem wie Moodle ist dies obligatorisch! Das DBMS muss also eine entsprechende Leistungsfähigkeit ermöglichen, da sonst die Arbeit mit dem Gesamtsystem für eine große Zahl von Benutzern mit extremen Wartezeiten verbunden ist und somit praktisch unmöglich wäre.

Bei den Datenbanken MySQL und MariaDB – beide unter dem leitenden Einfluss des gleichen Entwicklers, Michael Widenius, entwickelt – organisieren Speichersubsysteme den effizienten Zugriff auf Daten. Solche _Engines_ sind u. a. MyISAM, MERGE und nicht zuletzt InnoDB, was derzeit quasi dem Standard entspricht.

Datenbank-Systeme wurden und werden von verschiedenen Anbietern entwickelt und vertrieben. Moodle ist nicht nur auf eine Technologie festgelegt, sondern unterstützt alle gängigen DBMS. Allerdings müssen die jeweiligen Entwicklungsstände (Versionen) beachtet werden. Welche Datenbanken von Moodle unterstützt werden, zeigt Tabelle 3.1. Grundsätzlich sollten allerdings bei der Gestaltung der Serverumgebung die jeweiligen Release Notes des gewünschten Moodle-Pakets beachtet werden.

**3.3.4■Webserver auf Linux**

Über den Apache-Webserver wurden bereits eine Reihe von – sehr umfangreichen – Fach-büchern geschrieben. Darin wird die Konfiguration des Servers in den verschiedenen Konfigurationsdateien sowie dessen Absicherung gegen Hackerangriffe ausführlich erläutert.

Dieser Abschnitt des Buchs will diesen Werken keine Konkurrenz machen, wohl aber der interessierten Leserin bzw. dem interessierten Leser ein Beispiel – hier auf einem Desktop-Betriebssystem18 Ubuntu 18.04.3 – für die Installation und die Grundkonfiguration des Webservers anbieten.

**3.3.4.1■Prüfung der Systemvoraussetzungen**

Für dieses Beispiel steht ein Linux-Betriebssystem (in einer „VirtualBox“) zur Verfügung.

Aus dem Betriebssystem wurden für die Präsentation alle Programmteile des Apache2-Webservers, der Datenbanken und der PHP-Elemente entfernt.

18 Professionelle Webserver werden auf speziell für Server-Einsätze konfigurierte Betriebssysteme installiert. Die Wahl eines Desktop-Betriebssystems für die Illustration dieses Buchs begründet sich mit der Verfügbarkeit einer grafischen Benutzeroberfläche, die einem reinen Server-Betriebssystem fehlt, um die optimale Leistung den jeweiligen Diensten zur Verfügung zu stellen. Für den Einstieg erweist sich die grafische Oberfläche jedoch als verständlicher und einfacher zu handhaben.

3.3 Webserver-Software

**49**

Auf der anderen Seite soll auf dieser Maschine später ein Moodle-System installiert werden.

Ein Blick in die Release Notes, Abschnitt „Server Requirements“ beschreibt für Moodle 3.8

die groben Anforderungen an den Webserver:

PHP 7.1.0 als Minimum.

PHP-Erweiterung _intl_ ist erforderlich.

Bei den Datenbanken wird unter anderem MariaDB 5.5.31 gefordert.

Alternative Datenbanken sind: PostgreSQL 9.4 (11.x empfohlen), MySQL 5.6, Microsoft SQL-Server 2012 oder Oracle Database 11.2

Fehlende Software – sei es der komplette Apache-Webserver, eine oder mehrere PHP-Erweiterungen oder ein Datenbank-Server – können in einem Linux-System mit mittlerweile recht komfortablen Werkzeugen installiert werden. Das gilt sowohl für rein textbasierende Oberflächen (Terminal, Shell) als auch für Betriebssysteme mit grafischer Oberfläche. In den folgenden Abschnitten werden Beispiele für beide Umgebungen vorgestellt.

**3.3.4.2■Software-Installation auf der Konsole**

Die Installation von Programmpaketen ist auch ohne eine grafische Benutzeroberfläche möglich. In der Tat verzichtet man beim Betrieb eines Servers auf diesen Geräten meist auf eine grafische Benutzeroberfläche, um die verfügbare Rechenleistung der Maschine maximal den Serverdiensten zur Verfügung zu stellen. Man arbeitet direkt auf der Konsole.19 In größeren Serverfarmen werden die einzelnen Geräte ohnehin in System-Racks verbaut. Den klassischen „Computer am Arbeitsplatz“, bestehend aus Tastatur, Maus und Monitor darf man sich also nicht vorstellen. Stattdessen erfolgt die Administration von zentralen War-tungsplätzen aus.

Das in diesem Buch als Beispiel verwendete Betriebssystem Ubuntu-Linux gibt es auch als Server-Version! Wer sich für die Installation dieser Variante entscheidet, kann jedoch trotzdem jedes Softwarepaket installieren. Zum Editieren der Konfigurationsdateien eignen sich Konsolen-Editoren wie beispielsweise _nano,_ _joe_ oder _vi_ etc.

Sehr beliebt zur Installation oder Aktualisierung von Software über einen Kommandozei-lenbefehl ist _apt-get_. APT Steht für _**A**dvanced_ _**P**ackaging_ _**T**ool_. Das Programm ist ursprünglich mit der Debian-Distribution entwickelt worden. Da die Installation von Programmen auf einem Linux-System in der Regel Administratorrechte erfordert, muss apt-get entweder als Superuser (root) oder mit dem vorangestellten Befehl _sudo_ 20 ausgeführt werden. Der Befehl _sudo_ fordert die Eingabe des Administrator-Passworts und bewirkt die Ausführung des folgenden Befehls mit den entsprechenden Rechten des Systemverwalters.

19 Andere Begriffe: Terminal, Shell

20 Voraussetzung ist, dass _sudo_ auf dem Betriebssystem vorhanden ist. Es erfordert eine Datei _/etc/sudoers,_ die jedoch nicht mit einem einfachen Texteditor und schon gar nicht von Laien bearbeitet werden sollte!

**50** 3 Der Moodle-Server

**Software-Installation erfordert zumeist Administratorrechte**

Es ist nicht immer zwingend erforderlich, sich als Standardbenutzer vom

System ab- und als Superuser erneut anzumelden, um ein neues Programm

zu installieren, wenn hierzu Administratorrechte gefordert sind. Wird das Kommando _sudo_ dem Installationsbefehl vorangestellt, so wird dieser Befehl mit Administratorrechten ausgeführt. Selbstverständlich ist die Eingabe des gültigen Administrator-Passworts dazu die Voraussetzung.

■

Mit _apt-get_ können zu gleicher Zeit mehrere Programmpakete installiert werden. Die Namen dieser Pakete werden dem Befehl als _Argument_ 21 übergeben. Darüber hinaus benötigt dieses Programm ein Kommando, welches bestimmt, wie die Programmpakete zu behandeln sind (Installation, Update oder Entfernen aus dem System). Mithilfe zusätzlicher Optionen können zum Beispiel die Antworten auf Rückfragen automatisiert werden.

sudo apt-get [Optionen](Optionen) Kommando Paketname1 Paketname2 ...

**Tabelle 3.4** Optionen für apt-get (Auswahl)

Option Bedeutung

-b

Kompilierung des Programm-Quelltextes nach dem Download

-c

Vorgabe einer Konfigurationsdatei

-d

Es werden lediglich die Paketdateien heruntergeladen, nicht jedoch direkt installiert.

-f

Die Nachinstallation der Pakete, die in Abhängigkeit zum gewünschten Programm stehen, sowie die eventuelle Deinstallation fehlerhafter Pakete werden ausgeführt.

-h

Ausgabe eines Hilfetextes zu apt-get. Die gleiche Funktion ist mit dem Kommando help zu erreichen.

-s

Reine Simulation, keine Installation

-u

Ausgabe der Liste aller aktualisierten Programme

-y

Automatische Beantwortung von Zwischenfragen mit Ja (Yes). Ausnahme: Kritische Änderungen im System müssen weiterhin manuell bestätigt werden.

**Tabel e 3.5** Kommandos für apt-get (Auswahl)

Kommando Bedeutung

install

Lädt das gewünschte Programm herunter und führt die Installation aus. Es können mehrere Programme mit einem Befehl installiert werden.

update

Es werden alle Programmpaketquellen neu eingelesen und die entsprechenden Paketlisten im System aktualisiert.

remove

Remove deinstalliert das bzw. die bezeichneten Programmpaket(e).

clean

Löschen der heruntergeladenen Installationsdateien aus dem Archiv. Damit kann Festplattenspeicher freigegeben werden.

21 Als „Trennzeichen“ zwischen den Argumenten dient das Leerzeichen.

![Image 12](index-74_1.png)

3.3 Webserver-Software

**51**

Kommando Bedeutung

help

Ausgabe eines Hilfetextes zu apt-get. Die gleiche Funktion ist mit der Option -h zu erreichen.

upgrade

Die auf dem System installierten Programme werden auf den aktuellsten Stand gebracht. Es erfolgt keine nachträgliche Installation zusätzlicher oder Deinstallation überflüssiger Pakete.

dist-upgrade

Die auf dem System installierten Programme werden auf den aktuellsten Stand gebracht. Eventuell erforderliche Pakete werden zusätzlich installiert, nicht mehr erforderliche Pakete werden entfernt.

Der Apache-Webserver lässt sich zum Beispiel mit dem folgenden Befehl auf der Konsole installieren:

sudo apt-get -y install apache2 [Enter]

Obgleich die Konsole eine rein textgesteuerte Benutzeroberfläche ist, gibt es mit _Aptitude_ eine Alternative zum manuellen Tippen eines jeden Kommandos. Es handelt sich bei Aptitude um eine strukturierte Anordnung von Textelementen, die ein Menü und eine Über-sichtsliste darstellen. Aptitude bietet unter anderem die Möglichkeit, Programme zu suchen und zu installieren. Allerdings ruft Aptitude letztlich auch wieder _apt-get_ auf und dient lediglich der Vereinfachung der Vorgänge. Diese begründet sich zum Beispiel damit, dass die konkreten Namen der Programmpakete nicht bekannt sein müssen, sondern aus der Vorschlagliste ent nommen werden können.

**Bild 3.9** Das Programm „Aptitude“ läuft direkt im Terminal, ohne eine grafische Oberfläche vorauszusetzen. Es bietet gegenüber der manuellen Texteingabe einen gewissen Komfort bei der Installation von Programmen im Linux-System.

**52** 3 Der Moodle-Server

Programme auf der Kommandozeile lassen sich meist nicht mit der Maus22 steuern. Es gibt stattdessen Tastencodes, die auch durchaus in ihrer Handhabung als komfortabel empfun-den werden können.

**Linux ist „Case-sensitiv“: Groß- und Kleinschreibung beachten!**

Die Steuerung von Aptitude erfolgt u. a. mit Buchstabentasten. Hier macht die Groß- und Kleinschreibung allerdings Unterschiede. Wenn ein Befehl

einmal nicht funktioniert, sollte zuerst geprüft werden, ob die „Feststelltaste“

(Caps Lock) aktiviert wurde.

■

Aptitude kann sowohl direkt über Tastencodes als auch über ein Menü gesteuert werden, das mit der Tastenkombination **Strg**+**T** aufgerufen wird. Navigiert wird mit den Cursortasten (Auf- und Abwärts) bzw. über längere Abschnitte hinweg seitenweise mit **Bild↑** und **Bild↓**. Ein Programm wird zur Installation mit der Taste [**+**] vorgemerkt. Zur Deinstallation wird die Taste [**-**] auf dem markierten Eintrag gedrückt.

Um also die Datenbank _mariadb_ zu installieren, soll zunächst einmal danach gesucht werden. Dazu wird [**/**] – mit der Kombination **Umsch**+[**7**] – gedrückt.23 Dies öffnet einen einfachen Suchdialog mit einer Eingabezeile und den aktivierbaren Feldern **OK** und **Abbrechen**.

Zwischen diesen Feldern kann mit der Tabulator-Taste gewechselt werden. Die Auswahl erfolgt mit der Eingabetaste **Enter**.

Anschließend werden, wie beschrieben, die gewünschten Pakete markiert. Eine grüne Markierung bedeutet, dass die Installation möglich ist. Eine rote Markierung weist auf Probleme hin. Diese Probleme können mögliche Kollisionen mit bereits vorhandenen Programmen oder nicht auflösbare Abhängigkeiten sein. Mit der Taste [**G**] werden die Programmpakete heruntergeladen und installiert. Aptitude wird mit der Taste [**Q**] (= quit) verlassen. Allerdings erfolgt eine Rückfrage, ob das Programm wirklich geschlossen werden soll.

**Tabelle 3.6** Aptitude-Codes in der Aktionsspalte (erste Spalte)

Code

Bedeutung

p

Paket restlos entfernen (p = purge)

d

Löschen (d = delete)

i

Installieren

u

Aktualisieren (u = upgrade)

r

Neu-Installation (r = reinstall)

B

Broken

A

(in zweiter Spalte) bedeutet automatisch installiert

22 Eine Maussteuerung ist möglich, wenn zum Beispiel Aptitude in einem Terminal-Fenster einer grafischen Oberfläche ausgeführt wird.

23 Achtung: Es wird von einer Tastatur mit deutschem Layout ausgegangen! Auf Tastaturen mit z. B. US-Layout sind die Tasten anders belegt.

![Image 13](index-76_1.png)

3.3 Webserver-Software

**53**

**Bild 3.10** Mit den Cursortasten wird in der Auswahlliste navigiert. Mit „+“ wird ein Paket zur Installation markiert.

**3.3.4.3■Einfacher mit grafischer Oberfläche**

Nicht immer kann eine grafische Benutzeroberfläche zur Verwaltung des Servers verwendet werden. In einem solchen Fall kommt man um die gerade beschriebenen Tools nicht herum. Für den Aufbau eines eigenen Experimentalsystems oder für ein kleineres Produk-tivsystem24 kann man sich die Arbeit jedoch einfacher gestalten.

In den folgenden Beispielen werden fehlende Programmpakete mithilfe der _synaptic_-Paketverwaltung installiert. Das ist ein sehr einfach zu handhabendes grafisches Tool zur Auflistung bereits installierter Programme sowie zur Ergänzung weiterer Programme.

**Synaptic ist nicht Teil des Systems?**

In diesem Fall ist der Zugriff auf die Konsole sicher der einfachste und direk-teste Weg, um Synaptic zu installieren. Achtung: Es werden Administratorrechte benötigt, weswegen der Befehl mit dem vorangestellten Kommando

„sudo“ ausgeführt wird:

sudo apt-get -y install synaptic [Enter]

■

Zur Erinnerung: Die zu installierende Moodle-Version (3.8) fordert:

PHP 7.1.0 als Minimum.

PHP-Erweiterung _intl_ ist erforderlich.

Bei den Datenbanken wird unter anderem MariaDB 5.5.31 gefordert.

Alternative Datenbanken sind: PostgreSQL 9.4 (11.x empfohlen), MySQL 5.6, Microsoft SQL-Server 2012 oder Oracle Database 11.2.

24 Ein Server in einer Produktivumgebung sollte aus Gründen der Sicherheit – sowohl des Servers als auch der darauf arbeitenden Benutzerinnen und Benutzer – grundsätzlich von einem Profi installiert und verwaltet werden.

![Image 14](index-77_1.jpg)

**54** 3 Der Moodle-Server

Als Webserver soll Apache2 zum Einsatz kommen, der in Linux-Umgebungen quasi der Standard ist. Dieser wird zuerst installiert. Wie auch bereits beim Einsatz von _Aptitude_ (im Terminal) erläutert, ist es sinnvoll, die angebotene Liste zunächst auf die gewünschte Software einzugrenzen.

Das Paket _apache2_ ist sehr einfach zu finden. Das Feld in der linken Spalte wird nun mit der Maus angeklickt und im sich öffnenden Kontextmenü „ _Zum In stallieren vormerken_“ ausgewählt. Da möglicherweise weitere Programmpakete erforderlich sind, von denen der Apache-Webserver abhängig ist, werden diese ebenfalls zur Installation vorgeschlagen. Mit einem Klick auf _Vormerken_ werden auch diese zur Installation angemeldet.

Schaut man nun in die Paketliste von Synaptic, so fällt auf, dass nicht alle Programmpakete installiert werden, die entfernt mit dem Apache2-Webserver zu tun haben. Das System wird also nicht überfrachtet, allerdings ist durchaus zu überprüfen, ob nicht die Installation weiterer Pakete sinnvoll wäre, beispielsweise die Dokumentation oder spezielle Module wie etwa das PHP-Modul für den Apache-Webserver (libapache2-mod-php). Auch hier kann das System hinterfragen, ob weitere Pakete installiert werden sollen, zu denen Abhängigkeiten bestehen. Dies wird man in der Regel bestätigen.

Im oberen Teil der Programmoberfläche gibt es nun die Schaltfläche _Anwenden_. Ein Klick auf _Anwenden_ löst den Download und die Installation aller vorgemerkten Pakete aus. Auch für den umgekehrten Fall, dass Pakete zu deinstallieren sind, startet _Anwenden_ diese Aktion.

**Bild 3.11** Das gewünschte Programmpaket zu suchen, vereinfacht und beschleunigt die Installation, denn die angebotene Liste mit Software kann sehr lang sein.

![Image 15](index-78_1.png)

![Image 16](index-78_2.png)

![Image 17](index-78_3.png)

3.3 Webserver-Software

**55**

**Bild 3.12** An dieser Stelle wird noch keine Installation gestartet, sondern das gewünschte Programmpaket zunächst nur für die Installation „vorgemerkt“. Die eigentliche Installation wird ausgeführt, wenn alle Installations- sowie unter Umständen auch Aktualisierungs- oder Deinstallationswünsche platziert wurden.

**Bild 3.13** 

Ein ausgewähltes Softwarepaket kann unter

Umständen vom Vorhandensein weiterer Pakete

abhängig sein. Darum muss sich heute zum Glück

kein Linux-Benutzer mehr kümmern. Die Installa-

tion der Abhängigkeiten wird vom System auto-

matisch vorgeschlagen.

**Bild 3.14** Auch die zur Installation vorgemerkten Paketabhängigkeiten werden in Synaptic für die Installation in der Liste erfasst. Allerdings werden nur die Pakete automatisch vorgemerkt, die wirklich benötigt werden.

![Image 18](index-79_1.png)

![Image 19](index-79_2.png)

![Image 20](index-79_3.png)

**56** 3 Der Moodle-Server

**Bild 3.15** Möglicherweise werden weitere Pakete im System benötigt. Hier fällt ein interessantes Modul für den Apache-Webserver ins Auge, welches für den Betrieb eines Moodle-Systems wichtig erscheint: libapache2-mod-php (und dessen Abhängigkeiten).

**Bild 3.16** Die zu installierenden bzw. zu deinstallierenden Pakete werden in einer Zusammenfassung aufgelistet. Mit Klick auf _Anwenden_ wird die Operation bestätigt und ausgeführt.

**Bild 3.17** So sieht das gewünschte Ergebnis aus, wenn alle Pakete wunschgemäß installiert wurden.

![Image 21](index-80_1.png)

![Image 22](index-80_2.jpg)

3.3 Webserver-Software

**57**

**Bild 3.18** Die Paketliste von Synaptic zeigt die auf dem System installierten Pakete mit einer grünen Checkbox am Zeilenanfang. Bei Bedarf kann über dieses Feld die Deinstallation vor gemerkt werden.

Auf die gleiche Weise werden nun die übrigen Systemvoraussetzungen für die Moodle-Installation geschaffen. So ist der PHP-Parser auf der Serverseite unbedingt erforderlich, damit die Moodle-Skripte überhaupt ablaufen können. Mit dem Apache-Webserver wurde lediglich – und das in einem zweiten Auswahlschritt – das erforderliche Modul installiert.

Aus diesem Grund muss über die Paketsuche geprüft werden, ob die PHP-Module auf dem Server bereits installiert sind und ob sie dem geforderten Mindeststandard entsprechen.

**Bild 3.19** Der PHP-Parser wurde nicht automatisch installiert! Er muss also zusätzlich vor gemerkt und installiert werden. Die Version PHP 7.2 entspricht den Mindestanforderungen.

Weitere Programmpakete sollten bei der Installation berücksichtigt werden. Dies sind u. a.:

php-curl

php-gd

php-intl

php-json

php-mbstring

php-soap

php-xml

**58** 3 Der Moodle-Server

**3.3.4.4■Datenbankserver**

Neben dem Webserver und dem PHP-Parser wird eine Datenbank für das Moodle-System benötigt. Hier soll die lizenzfreie Datenbank _MariaDB_ als Datenbankserver installiert werden. Für die Verwaltung der Datenbank bietet sich das Werkzeug _phpMyAdmin_ an, welches ebenfalls als Programmpaket installiert werden kann.

Alle genannten Programmpakete können in einem einzigen Durchgang durch „Anwenden der Auswahl“ installiert werden. Die Installation der Datenbank erfordert die Vergabe eines Passworts. Dieses sollte nicht zu einfach zu erraten sein, besonders dann nicht, wenn die Datenbank über öffentliche Netzwerke zugänglich ist. Ein sicheres Passwort wird niemals in einem Wörterbuch zu finden sein. Es sollte Groß- und Kleinbuchstaben sowie Ziffern und Sonderzeichen enthalten. Eine gute Möglichkeit, selbst ein solches Passwort mit einem hohen Sicherheitsniveau zu erzeugen, ist die Verwendung eines Merksatzes. Ein Beispiel: Merksatz: „ _**M**ein_ _**e**rstes_ _**A**uto_ _**w**ar_ _**e**in_ _**V**W_- _**K**äfer **B**aujahr **71!**_ “

Daraus werden die jeweils ersten Buchstaben jedes Wortes, die Zahl und das Satzzeichen gewählt. Das so entstandene Passwort lautet:

_MeAweVKB71!_

Es ist kompliziert für Hacker-Programme zu knacken und doch einfach zu merken.

**Konfiguration und Aktivierung der Module**

Mit der Installation der Programmpakete wird vorerst eine Grundinstallation durchgeführt. Bevor nun Moodle installiert werden kann, müssen möglicherweise in der Konfigurationsdatei des Webservers – _httpd.conf_ – zusätzlich erforderliche Module _aktiviert_ werden.

■

Nach der Installation muss geprüft werden, ob der Server funktioniert. Auf dem eigenen Computer wird in der Adresszeile des Webbrowsers – in diesem Beispiel wird Firefox verwendet, es kann sich aber auch um nahezu jeden anderen Browser handeln – die folgende Adresse eingegeben:

localhost [Enter]

Wenn die Installation korrekt verlaufen ist, sollte sich die _Apache2 Default Page_ öffnen. Das ist nicht nur eine Kontrollseite, die aus dem Stammverzeichnis des Webservers an den Browser gesendet wird, sie bietet auch wichtige Informationen zum Standort der wichtigsten Konfigurationsdateien.

**Konfigurationsdateien sind vom System abhängig**

Die Entwickler der verschiedenen Linux-Distributionen variieren ihre Strategien zur Konfiguration der Server. Welche und wie viele Konfigurationsdateien verwendet werden, ist immer anhand der jeweiligen Server-Dokumentation zu prüfen!

■

![Image 23](index-82_1.png)

3.3 Webserver-Software

**59**

_„localhost“_ steht als Synonym für die IP-Adresse 127.0.0.1. Das ist vereinbarungsgemäß grundsätzlich die Netzwerkadresse des eigenen Computers und funktioniert auch dann, wenn gerade weder ein WLAN noch ein Draht gebundener Netzwerkanschluss verfügbar ist. Man nutzt gewissermaßen sein eigenes kleines „lokales Insel-Internet“. Auch diese IP-Adresse kann in die Adresszeile eingegeben werden und sollte zum gleichen Ergebnis führen.

**Bild 3.20** Die Apache2 Default Page ist weit mehr als eine Kontrollseite zur Überprüfung der Serverfunktion! Sie enthält wichtige Informationen zu den Standorten und den Aufgaben der Konfigurationsdateien des Servers.

![Image 24](index-83_1.jpg)

**60** 3 Der Moodle-Server

**Bild 3.21** phpMyAdmin ist die bekannteste Administrationsoberfläche für MySQL und MariaDB.

Sie läuft direkt im Webbrowser.

Ebenso sollte die Funktion der Datenbank-Administrationsoberfläche getestet werden: localhost/phpmyadmin [Enter]

Über diese Oberfläche werden Datenbanken angelegt und können gezielt verwaltet werden.

Unter anderem lassen sich mithilfe von _phpMyAdmin_ auch fehlerhafte Daten korrigieren.

Vor allem ist es sinnvoll, mithilfe eines solchen Verwaltungstools wie phpMyAdmin eine Datenbank speziell für Moodle anzulegen. Zwar ist grundsätzlich auch das Installationsskript dazu in der Lage, jedoch ist dies bezüglich der Systemsicherheit sehr kritisch. Das ist besonders deswegen zu berücksichtigen, weil der Zugriff auf die Datenbank mit der Installation nur dem Systemverwalter erlaubt ist.

Für die Verwaltung der Datenbanken muss der erste Login mit dem Account des Systemverwalters erfolgen. Der Benutzername ist also „root“. Das Passwort entspricht dem, welches auch im Linux-System dem Superuser zugewiesen wurde.

Da diese Zugangsdaten universelle Rechte im System eröffnen, versteht es sich von selbst, dass sie niemals in einer Webplattform, die aus dem Internet zugänglich ist, verwendet werden sollten. Darüber hinaus sind die Rechte auch innerhalb des Datenbankmanage-mentsystems durchaus sensibel zu betrachten und unbedingt auf den zur Erfüllung der Aufgaben notwendigen Umfang zu beschränken. Um beides zu erreichen, wird in der Administration der Datenbank ein neuer Systembenutzer angelegt, der neu auf eine bestimmte Datenbank zugreifen darf. Dieser soll hier schlicht und einfach „moodle“ heißen. Es empfiehlt sich jedoch, in einem Live-System mit öffentlichem Zugriff einen neutralen Benutzernamen zu vergeben, der nicht unmittelbar mit Moodle in Zusammenhang gebracht werden kann. Öffent liche Webspace-Anbieter verwenden meist Datenbank- und Benutzernamen, die aus beliebigen Buchstaben- und Zahlenfolgen gebildet werden. Das erschwert Angriffe auf das System.

![Image 25](index-84_1.jpg)

![Image 26](index-84_2.jpg)

3.3 Webserver-Software

**61**

**Bild 3.22** Mit dem regulären Benutzer-Account ist es nicht möglich, sich bei der lokalen MySQL-bzw. MariaDB-Datenbank anzumelden. Dies erfordert die Rechte des Systemverwalters „root“ oder eines Benutzers, der Zugriff auf eine oder mehrere Datenbanken hat. Letzterer existiert jedoch noch nicht.

**Safety first!**

Datenbanken – noch dazu die einer Lernmanagement-Plattform wie Moodle –

sind ausgesprochen sensible Angriffsziele für Hacker. Sie enthalten nicht nur meist urheberrechtlich geschütztes Material, sondern vor allem auch sehr persönliche Daten und Leistungsnachweise. Der Schutz dieser Datenbanken

beginnt mit der sorgsamen Konfiguration der Zugangsdaten und der Zugriffsrechte.

■

**Bild 3.23** 

Wenn „root“ tatsächlich der einzige Benutzer bleibt,

der Zugriff auf die Datenbank hat, so ist dies ein

eklatantes Sicherheitsproblem!

![Image 27](index-85_1.jpg)

![Image 28](index-85_2.jpg)

**62** 3 Der Moodle-Server

**Bild 3.24** Mit phpMyAdmin (und den Rechten des Systemverwalters) kann man sowohl neue Datenbanken im System als auch Benutzer-Accounts mit eingeschränkten Rechten erstellen. Beides dient unter anderem der Sicherheit.

**Bild 3.25** Der Systemverwalter vergibt einen Namen für den neuen Systembenutzer und ein Passwort. Auch wenn hier für das Beispiel der Name „moodle“ gewählt wird, sollte aus Sicherheitsgründen ein „neutraler“ Name und ein sicheres Passwort gewählt werden. Beide Daten werden später für die Moodle-Installation benötigt!

![Image 29](index-86_1.jpg)

3.3 Webserver-Software

**63**

**Bild 3.26** Der Systemuser „moodle“ – hier wurde er so genannt, die Namensvergabe ist frei-bleibend im Ermessen des Administrators – braucht nicht alle Rechte. Eine möglichst genaue Einschränkung steigert die Sicherheit des gesamten Systems!

Mit dem Account des neuen Datenbank-Systembenutzers kann zugleich eine leere Datenbank mit dessen Namen eingerichtet werden. Dies sollte man tun, falls noch keine Datenbank für Moodle existiert. Wichtig ist, sich die Zugangsinformationen zu notieren, denn sie werden später bei der Installation der Moodle-Software be nötigt.

Im Fall dieses _Beispielsystems_ 25 sind das nun:

Adresse der Datenbank: _**localhost**_ (oder eine bekannte IP-Adresse bzw. der URL)

Name der Datenbank: _**moodle**_

Benutzername für die Datenbank: _**moodle**_

Passwort für den Datenbank-Zugriff: _**moodle**_

Es versteht sich von selbst, dass derartige einfache Zugangsdaten für ein Live-System tabu sind. Sie würden einem Angreifer wie ein ausgebreiteter „roter Teppich“ erscheinen. Zudem entsprechen solch banalen Zugangsdaten nicht dem „Stand der Technik“, wie er in der Datenschutzgrundverordnung (DSGVO) gemeint ist. Im Fall eines Datenmissbrauchs würde dies als grobe Fahrlässigkeit gewertet werden.

Obwohl nun eine Datenbank und ein Benutzer speziell für das Moodle-System existieren, kann es bei der Installation trotzdem zu weiteren Hürden kommen. Verantwortlich dafür ist die Art und Weise, wie die Daten einer Zeile physisch gespeichert werden. Hier gibt es bei-25 Wichtig: Wie beschrieben sind die hier gezeigten Einstellungen auf keinem Fall für ein Live-System geeignet!

**64** 3 Der Moodle-Server

spielsweise dynamische Verfahren und Datenkompression. Da es zwei Dateiformate des Speicher-Subsystems _InnoDB_ gibt, welches für Moodle favorisiert wird, kann es bei der Installation von Moodle bei der finalen Systemprüfung zu einer ärgerlichen Meldung kommen. Die Dateiformate der InnoDB-Engine heißen _Antelope_ und _Barracuda_.

**Tabelle 3.7** Wesentliche Unterschiede des „Antelope“- und „Barracuda“-Formats in MySQL

(Quelle: _https://mariadb.com/kb/en/innodb-row-formats-overview/#redundant-row-format,_ Zugriff: 04. 01. 2020)

Zeilenformat

Antelope Barracuda Beschreibung

REDUNDANT

Ja

Ja

Kompatibel zu älteren MySQL-Versionen

COMPACT

Ja

Ja

Speicherersparnis von bis zu 20 % im Vergleich zum

redundanten Format

DYNAMIC

Nein

Ja

Ähnlich wie das „COMPACT“-Format, jedoch mit

erweiterten Speichereigenschaften für große

Variablenlängen

COMPRESSED

Nein

Ja

Bietet zusätzlich zu den Eigenschaften des

„ DYNAMIC“-Formats Datenkompression

Wenn Moodle während der Installation einen Fehler bzw. nicht erfüllte Voraussetzungen meldet, hilft es, die Datei _/etc/mysql/my.cnf_ zu bearbeiten. Das Moodle-Projekt beschreibt die dazu notwendigen Schritte in den Dokumentationen (die Meldungen beim abschließenden Systemcheck enthalten einen direkten Link).

Sinnvoller erscheint es jedoch, bereits vor der Installation die soeben erzeugte (noch leere) Datenbank über phpMyAdmin mithilfe von SQL-Kommandos zu konfigurieren. Dies löst in der Regel die Probleme und sollte auch für Moodle-Adminis tratoren der erste Schritt sein, um ihr System auf einem öffentlichen Webhoster zu installieren.

**Konfiguration des InnoDB-Datei-Formats in phpMyAdmin**

� Wahl des Registers SQL

� Eingabe dreier Befehlszeilen (Achtung: Abschluss mit einem Semikolon!):

� SET GLOBAL innodb_file_format = barracuda;

� SET GLOBAL innodb_file_per_table = 1;

� SET GLOBAL innodb_large_prefix = ‘on‘;

� Mit OK bestätigen

■

![Image 30](index-88_1.png)

3.3 Webserver-Software

**65**

**Bild 3.27** Schon ärgerlich: Bei einem öffentlich angemieteten Webspace ist hier eine Mail an den Support erforderlich. Bei einem eigenen Server genügt es, die Datei _/etc/mysql/my.cnf_ zu bearbeiten.

**3.3.4.5■Anpassung älterer Systeme für das Upgrade**

Wer ein Upgrade von einer älteren Moodle-Version mit bereits bestehender Datenbank durchführen muss und direkten Zugriff auf die Interna des Systems hat, kann durchaus auch direkt die Konfiguration der Datenbank bearbeiten. Dies passiert im hier gezeigten Testsystem in der Datei _my.cnf_, die sich im Verzeichnis _/etc/mysql/_ befindet. Die Änderungs- bzw. Aktualisierungsschritte sind in der Moodle-Dokumentation beschrieben:

[_https://docs.moodle.org/38/de/MySQL_Unicode_Unterstützung_](https://docs.moodle.org/38/de/MySQL_Unicode_Unterstützung)

Der Grund dafür sind Änderungen beim Standard-Zeichensatz, mit denen die Daten in die Datenbank gespeichert werden. Der Aufruf der Datei zur Bearbeitung muss mit Systemverwalterrechten erfolgen:

sudo gedit /etc/mysql/my.cnf [Enter]

In die Datei werden folgende Zeilen eingetragen bzw. entsprechende Einträge korrigiert:

[client]

default-character-set = utf8mb4

[mysqld]

![Image 31](index-89_1.png)

**66** 3 Der Moodle-Server

innodb_file_format = Barracuda

innodb_file_per_table = 1

innodb_large_prefix

character-set-server = utf8mb4

collation-server = utf8mb4_unicode_ci

skip-character-set-client-handshake

[mysql]

default-character-set = utf8mb4

Wichtig ist: Nachdem die Datei _/etc/mysql/my.cnf_ editiert wurde (mit Systemverwalterrechten!), muss der MySQL-Server (bzw. der MariaDB-Server) neu gestartet werden. Erst dann wird die neue Konfiguration wirksam.

In dem hier verwendeten Ubuntu-Linux-System erledigt man dies am einfachsten mit Systemverwalterrechten auf der Kommandozeile:

sudo /etc/init.d/mysql restart [Enter]

Danach muss dafür gesorgt werden, dass die Datensätze auch tatsächlich in das neue Format konvertiert werden. Hierzu wird im Moodle-Stammverzeichnis auf dem Webserver im Unterverzeichnis /admin/cli/ die Datei mysql_collation.php gesucht und mit der Option

- -collation=utf8mb4_unicode_ci mit dem php-Kommando ausgeführt:

sudo php /var/www/html/moodle/admin/cli/mysql_collation.php

--collation=utf8mb4_unicode_ci [Enter]

**Bild 3.28** Der PHP-Konvertierungsbefehl erzeugt in der Kommandozeile eine sehr lange Liste mit Informationen zu jeder einzelnen Tabellenspalte, die entweder konvertiert wurde oder in der keine Konvertierung erforderlich war. Es empfiehlt sich, diese Liste Zeile für Zeile zu untersuchen, wenn Fehler gemeldet wurden (errors ungleich Null).

**3.3.4.6■Das Moodle-Datenverzeichnis**

Das Moodle-Datenverzeichnis ist vorgesehen, um alle verwendeten Kurs- und Unterrichtsmaterialien zu speichern. Dieses Verzeichnis sollte nicht über einen Zugriff aus dem Internet erreichbar sein, sich also nicht im direkten Webspace des Moodle-Systems befinden.

![Image 32](index-90_1.png)

3.3 Webserver-Software

**67**

Allerdings muss der Webserver direkten Zugriff auf dieses Verzeichnis haben. Nur so können die PHP-Skripte des Moodle-Systems die geforderten Inhalte bereitstellen. Das ist kein Widerspruch, denn der PHP-Parser ist eine im Auftrag des Webservers auf dieser Maschine laufende Instanz, die durchaus als „Bote“ zwischen dem systeminternen und dem öffentlich zugäng lichen Bereich agieren kann.

**Sicherheit der Dokumente und Bilder**

Dokumente, Videos, Bilder und Präsentationen etc., die als Kursinhalte oder aber als persönliche Daten in das System hochgeladen werden, sind vor

dem allgemeinen öffentlichen Zugriff zu schützen. Sie sollen ausschließlich in der vorgesehenen Weise für die jeweiligen Kurse zur Verfügung gestellt werden. Um einen direkten Zugriff auf diese Inhalte aus dem Internet ohne Benutzung der Moodle-Plattform zu vermeiden, muss das Moodle-Datenverzeichnis außerhalb des öffentlich zugänglichen Webspaces platziert und dem Webserver darauf Schreib- und Leserechte eingeräumt werden. Ist dies nicht möglich, müssen die Zugriffsrechte für das Verzeichnis restriktiv

eingeschränkt werden.

■

**Bild 3.29** Der eigentliche Webspace ist hier im Verzeichnis /var/www/html/ hinterlegt.

Das Verzeichnis /var/www/moodledata/ ist nicht direkt über einen Webbrowser zugänglich.

Im Fall dieses Testsystems wurde ein Parallelverzeichnis zum öffentlich zugäng lichen Webspace für das Moodle-Datenverzeichnis gewählt. Dieses muss nun allerdings auch vom Webserver und von dessen Diensten erreichbar sein. Dazu benötigen der Besitzer des Verzeichnisses – wenn es nicht gerade bereits _root_ ist – und die Benutzergruppe des Webservers entsprechende Zugriffsrechte. Für alle anderen Benutzer werden keine Rechte vergeben!

**68** 3 Der Moodle-Server

**Rechte für die Benutzergruppe?**

Unter IT-Experten wird zum Teil heftig diskutiert, ob der Zugriff auf das Moodle- Datenverzeichnis nicht ausschließlich dem Webserver und dem

Systemverwalter erlaubt werden soll. Der _chmod_-Befehl müsste dann den Wert 0700 übergeben, wodurch nicht nur der öffentliche Zugriff vollkommen untersagt wird, sondern auch der von Mitgliedern der Benutzergruppe des

Webservers.

Praktisch ist es jedoch sinnvoll, einen oder mehrere Moodle-Administratoren zu bestimmen, die auf dieses Verzeichnis Zugriff haben, um eventuell kritische Inhalte zu entfernen oder um ein komplettes manuelles Backup durchzuführen.

Aus diesem Grund wird hier _chmod_ mit dem Wert 0770 verwendet.

■

Um einer Benutzergruppe Zugriff auf das Moodle-Datenverzeichnis zu erlauben, wird folgender Befehl26 verwendet:

sudo chgrp -cR www-data /var/www/moodledata/ [Enter]

Nun werden für das Moodle-Datenverzeichnis mithilfe des Befehls chmod die Rechte vergeben. Sowohl der Besitzer (hier: der Systembenutzer _www-data_ = der Dienst des Webservers) als auch die Benutzergruppe _www-data_ (ihr können neben dem Webserver auch andere Benutzer angehören, die Administrationsaufgaben wahrnehmen) bekommen alle Rechte (oktaler Wert „7“). Öffentliche (andere) Benutzer sollen dagegen überhaupt keinen Zugriff auf dieses Verzeichnis erhalten (oktaler Wert „0“). Daraus ergibt sich die folgende Kommandozeile:

sudo chmod -R 0770 /var/www/moodledata/ [Enter]

**Systemänderungen nur mit Superuser-Rechten!**

Änderungen des Benutzerstatus und der Zugriffsrechte für ein Verzeichnis oder eine Datei erfordern die Rechte des Systemverwalters. Deswegen

muss die Befehlszeile mit dem Kommando „sudo“ eingeleitet werden. Es

wird nach dem Absenden des Befehls zusätzlich das Passwort des System-

verwalters abgefragt.

■

26 _Achtung:_ Dieser Befehl funktioniert nur dann, wenn das Moodle-Datenverzeichnis tatsächlich in genau diesem Pfad platziert wurde und die Benutzergruppe auch _www-data_ heißt.

![Image 33](index-92_1.jpg)

3.3 Webserver-Software

**69**

**Bild 3.30** 

Das Moodle-Datenverzeichnis ist

öffentlich nicht direkt erreichbar. Ledig-

lich der Webserver als Systembenutzer

und Mitglieder der Webserver-Benutzer-

gruppe dürfen darauf zugreifen.

**3.3.4.7■Systemsicherheit und Benutzerrechte für den Webserver**

Im Fall eines eigenen Testsystems erscheint die Installation zunächst recht einfach, denn schließlich passiert ja alles auf dem „eigenen Computer“. Es muss jedoch beachtet werden, dass ein Linux-System sehr streng und restriktiv mit den User-Rechten umgeht. So kann jedes Verzeichnis im Besitz eines bestimmten Benutzers oder einer Benutzergruppe sein.

Der Zugriff wird hier streng nach den jeweiligen Rechten zum Lesen, zum Schreiben und –

wo es der Programmtypus vorsieht – zum Ausführen geregelt.

Wichtig ist in diesem Zusammenhang, dass unter einem Benutzer nicht zwingend ein Mensch zu verstehen sein muss. Auch einer Software bzw. einem Serverdienst kann ein Benutzer-Account im System zugewiesen werden. So existieren auch ein Benutzer und eine eigene Benutzergruppe für den Apache-Webserver. Der Systembenutzer, welcher den Dienst des Apache-Webservers im System verkörpert, heißt _www-data_. Die Verzeichnisse des Webservers gehören dem Systemverwalter (root) und zu dessen gleichnamiger Gruppe. Dies muss berücksichtigt und in der Regel angepasst werden, damit Dateien entweder aus der Ferne per FTP – zum Beispiel mit einem Programm wie FileZilla – oder eben lokal mit den üblichen Kopier verfahren zwischen verschiedenen Ordnern in das Webserver-Stammverzeichnis geschrieben werden können. Der Superuser-Account sollte aus Sicherheitsgründen nicht für Fernzugriffe vorgesehen werden.

**Wie kommen die Dateien ins Webserver-Verzeichnis?**

Wer bereits eine XAMPP-Installation ausprobiert hat, wird sich über diese Frage wundern. Wer allerdings auf einem Linux-System arbeitet, wird schnell feststellen, dass eine Übertragung der Moodle-Dateien mit „Copy and

Paste“ in das Webserver-Verzeichnis (meist) nicht sofort funktioniert. Das liegt daran, dass der eigene Benutzer-Account im System nicht mit dem des System benutzers des Webservers (www-data) identisch ist.

Benutzer lassen sich in einem Linux-System allerdings auch zu _Gruppen_ zusammenfassen. Mit dem Beitritt zur Gruppe des Webserver-Benutzers

lassen sich die Zugriffsprobleme lösen und dabei die Systemsicherheit

bewahren.

■

![Image 34](index-93_1.png)

**70** 3 Der Moodle-Server

Mit einem ersten Experiment soll das Problem27 verdeutlicht werden: Obwohl der Benutzer

„moodle2“ auf dem System existiert und ein FTP-Server28 läuft, scheitert die Übertragung des (hier noch) gezippten Moodle-Pakets. Es wird ein _kritischer Datenübertragungsfehler_ gemeldet. Viel aussagekräftiger ist aber die Meldung in der Zeile zuvor: _553 . . . Permission_ _denied!_ Der Zugriff auf das Zielverzeichnis wird verweigert.

**Bild 3.31** Die Übertragung mit dem FTP-Programm – hier FileZilla – scheitert, weil der Benutzer keine passenden Zugriffsrechte – in diesem Fall Schreibrechte – auf das Zielverzeichnis /var/www/

html hat.

Das Ergebnis ist durchaus zum aktuellen Stand der Server-Konfiguration korrekt und sinnvoll. Es geht schließlich um die Sicherheit des Systems und aller damit arbeitenden Benutzerinnen und Benutzer. Natürlich muss das System die Bearbeitung durch legitimierte Benutzer gestatten. Die dazu erforderlichen Voraussetzungen sollen in den nächsten Schritten geschaffen werden. Dazu sei zunächst einmal das Webserver-Stammverzeichnis näher betrachtet, in das letztlich die Moodle-Dateien hineingeschrieben werden sollen. Streng genommen sind die Besitzverhältnisse und die vergebenen Rechte interessant. Der „Besit-27 Warum treten derartige Probleme nicht bei einem öffentlichen Webspace-Anbieter auf, der meist ähnliche Plattformen nutzt? Die Antwort ist einfach: Dort kümmert sich ein professioneller Systemverwalter um die

„ Kleinigkeiten“, die hier nachfolgend beschrieben werden.

28 Ist kein FTP-Server auf dem Linux-System installiert, so kann dieser mit der Paketverwaltung _Synaptic_ oder direkt auf der Kommandozeile mit dem Befehl sudo apt-get install ftpd [Enter} nachträglich installiert werden.

![Image 35](index-94_1.png)

3.3 Webserver-Software

**71**

zer“ des Verzeichnisses ist „root“, der _Superuser_ des Systems. Das Verzeichnis ist der Gruppe des Systemverwalters zugewiesen. Bedauerlicherweise ist der Benutzer „moodle2“

nicht Mitglied der Gruppe „root“ und natürlich – der Name sagt es bereits – nicht der Sys-temverwalter29 mit dem _Namen_ „root“.

**Bild 3.32** 

Das Webserver-Stammverzeichnis gehört

dem Systemverwalter (root). Nur dieser

darf Dateien in das Verzeichnis schreiben

oder löschen. Mitglieder der Gruppe

„root“ und alle anderen Benutzerinnen

und Benutzer dürfen lediglich die Dateien

lesend öffnen und sie nicht verändern!

In den Foren des Internets kursieren nun verschiedene – zum Teil sehr abenteuerliche –

„Lösungen“ des Problems. So wird beispielsweise vorgeschlagen, allen Benutzern und Benutzergruppen alle Rechte zuzuweisen. Gewiss: Damit gibt es keine Probleme mehr, die Daten in das Webserver-Stammverzeichnis zu schreiben. Leider kann das auch jeder x-beliebige Spaßvogel oder jeder kriminelle Cracker aus dem Internet ebenso. Von „Sicherheit“

könnte man in diesem Fall nicht mehr sprechen.

**Sicherheitsrisiko: Alle Rechte für jeden**

Im eigenen Interesse und im Interesse der Systemsicherheit sowie der

Sicherheit aller Benutzerinnen und Benutzer gilt: _Finger weg_ von Ratschlägen, Rechte mit 0777 oder „rwxrwxrwx“ zu vergeben. Beides würde bedeuten,

dass jeder das Recht hat, Dateien zu lesen, zu schreiben und auszuführen!

Damit steht das betroffene Verzeichnis Angreifern offen wie das sprichwörtliche Scheunentor!

■

Es gibt einen Weg, der in diesem Fall drei Schritte umfasst:

Änderung der Gruppe von „root“ nach „www-data“

Zuweisung von Schreibrechten auf das Verzeichnis und alle Unterverzeichnisse für diese Gruppe

Zuordnung aller berechtigten Benutzer (hier moodle2), die schreibenden Zugriff auf das Webserver-Stammverzeichnis haben dürfen, zur Gruppe „www-data“

29 Hier ist der Systemverwalter des Betriebssystems gemeint. Andere Benutzer können mit Systemverwalterrechten auf der Kommandozeile arbeiten, wenn sie das Kommando _sudo_ dem eigentlichen Befehl voranstellen. Sie müssen jedoch zusätzlich das Passwort des Systemverwalters kennen.

**72** 3 Der Moodle-Server

Mit dem ersten Schritt – dem Wechsel der Gruppe, die besondere Rechte und Privilegien in dem betreffenden Verzeichnis genießt – werden keinesfalls die Rechte des Eigentümers (des Systemverwalters „root“) beschnitten und es werden dessen Rechte auch nicht auf die Mitglieder der Gruppe übertragen. Der sinngemäße Befehl auf der Kommandozeile – dieser muss mit dem vorangestellten Kommando _sudo_ ausgeführt werden, da die Gruppenände-rung Administratorrechte erfordert – heißt _chgrp_ 30.

Die vollständige Befehlszeile, um dem Webserver-Stammverzeichnis _/var/www_ die Benutzergruppe _www-data_ zuzuordnen, lautet wie folgt:

sudo chgrp -cR www-data /var/www [Enter]

Die dabei verwendeten Optionen „-c“ und „-R“ erläutert die Tabelle 3.8.

**Tabelle 3.8** Optionen für den Befehl _chgrp_ (Gruppenwechsel) Option Bedeutung

-c

„Changes“ – Bezeichnung der zu verändernden Dateien oder Verzeichnisse, denen die Gruppe zugeordnet werden soll

-f

Unterdrückung von Fehlermeldungen

-R

Rekursive Bearbeitung von Verzeichnissen sowie Einbezug von Unterverzeichnissen und deren Dateien

-v

Detaillierte Ausgabe aller Aktivitäten auf der Kommandozeile

Der zweite Schritt ist nun die Veränderung der Zugriffsrechte für die Mitglieder dieser Gruppe. Mitglieder der Gruppe _www-data_ müssen auch Dateien bearbeiten und in das Verzeichnis hineinschreiben können. Sie zu lesen genügt allein dem Webserver, um die ange-forderten Daten an den Webbrowser zu senden. Das Design einer Webseite ist ohne Schreibrechte allerdings nicht möglich.

Die Zugriffsrechte auf Dateien und/oder Verzeichnisse werden mit dem Kommando _chmod_ festgelegt. Die Rechte werden für bis zu vier Benutzertypen definiert:

Besitzer der Datei bzw. des Verzeichnisses – dies ist ein Benutzer bzw. _**U**_ ser, Abkürzung: _**u.**_

Gruppe mit Rechten auf diese Datei bzw. das Verzeichnis – Abkürzung steht _**g**_ für _**G**_ roup.

Andere Benutzer – Abkürzung _**o**_ für _**o**_ ther

Alle – Abkürzung: _**a**_ für _**a**_ ll

Die Abkürzungen für die verschiedenen Rechte, wie sie im chmod-Befehl verwendet werden, lauten:

**r** für _**r**ead_: Recht zum Lesen

**w** für _**w**rite_: Recht zum Schreiben

**x** für _e**x**ecute_: Recht zum Ausführen

Damit den Benutzertypen Rechte zugewiesen werden können, bedarf es noch eines Operators. Hier werden „+“ zum Zuweisen bzw. zum Ergänzen eines Rechts und „–“ zum Entziehen eines Rechts verwendet. Das Gleichheitszeichen (=) weist ebenfalls ein oder mehrere Rechte zu, allerdings werden alle nicht bezeichneten Rechte entzogen, auch dann, wenn sie 30 _chgrp_ steht als Abkürzung für Change Group – Gruppenwechsel.

3.3 Webserver-Software

**73**

bereits vor Ausführung des Befehls vorhanden waren. Tabelle 3.9 zeigt die Abkürzungen zusammengefasst in einer Übersicht.

**Tabelle 3.9** Argumente für den chmod-Befehl im „symbolischen Modus“

Benutzergruppen

Rechte

Operatoren

**Benutzergruppe Code Recht**

**Code Operator Bedeutung**

Besitzer

u

Lesen

r

+

Hinzufügen

Gruppe

g

Schreiben

w

–

Entziehen

Andere

o

Ausführen

x

=

Bezeichnete Rechte gesetzt, alle

anderen entzogen

Alle

a

Für den hier beschriebenen Webserver ist es erforderlich, dass die Gruppe _www-data_ sowohl lesenden als auch schreibenden Zugriff auf das Webserver-Stammverzeichnis hat. Sollen beispielsweise auch ZIP-Archive entpackt werden, wird zudem ein Recht zum Ausführen benötigt.

**Auch _chmod_** **verwendet Optionen in der Befehlszeile**

Wie bereits beim Befehl _chgrp_ gesehen, werden auch beim _chmod_-Befehl Optionen verwendet, um die Reichweite und den Umfang der auszugebenden

Informationen festzulegen. Es handelt sich um die gleichen Optionen, wie sie bereits in Tabelle 3.8 aufgeführt wurden.

■

Neben der _symbolischen_ Schreibweise des Befehls kann auch die sogenannte _oktale_ Schreib-weise31 verwendet werden, die in der Regel von Profis bevorzugt wird. Die Kombinationen aller möglichen Rechte können somit in einer einzigen Ziffer von 0 bis 7 dargestellt werden.

Für alle drei Benutzergruppen (Besitzer, Gruppe und Andere) lassen sich somit mit einer dreistelligen Oktalzahl32 alle Rechte vollständig zuweisen.

**Tabelle 3.10** Rechte-Berechnung in Oktalwerte

Bit

Recht

Recht erteilt = 1 Stellenwert Summanden

0

Ausführen

0

* 1

0

1

Schreiben

1

* 2

2

2

Lesen

1

* 4

4

Oktalwert zur Beschreibung der Rechtekombination (Summe)

**6**

31 Der Hintergrund ist technischer Natur. Für jede Benutzergruppe werden die Rechte durch jeweils ein Bit symbolisiert. Ein gesetztes Bit (1) bedeutet Recht erteilt. Eine Null steht entsprechend für Recht nicht erteilt.

Für jede Benutzergruppe ergibt sich somit eine Kombination aus drei Bit. Alle möglichen Kombinationen lassen sich durch eine einzige oktale Ziffer (Zahlensystem von 0 bis 7) ausdrücken.

32 Zur Kennzeichnung einer Zahl als Oktalzahl wird in der Informatik eine führende Null geschrieben. Damit kann die Zahl eindeutig von Zahlen anderer Zahlensysteme (Dezimal, Hexadezimal etc.) unterschieden werden.

![Image 36](index-97_1.png)

**74** 3 Der Moodle-Server

Die Rechtevergabe (Lesen und Schreiben) für die Gruppe _www-data_ auf das Webserver-Stammverzeichnis sieht in der _Symbolschreibweise_ folgendermaßen aus: sudo chmod -R g+rw /var/www [Enter]

In entsprechend gewandelter Form kann der Befehl auch in _oktaler Schreibweise_ geschrieben werden. Hierbei wird das Gesamtbild der Rechte aller drei Benutzergruppen betrachtet:

Der Besitzer (root) darf alles: 7

Die zugewiesene Benutzergruppe (www-data) soll im Verzeichnis lesen und schreiben dürfen. Allerdings wird für ein Verzeichnis auch das Recht zum „Ausführen“ benötigt, um in dieses zu wechseln: 7

Alle übrigen Benutzer dürfen die Inhalte des Verzeichnisses lesen und ausführen: 5

Der chmod-Befehl sieht in oktaler Schreibweise nun so aus:

sudo chmod -R 0775 /var/www [Enter]

**Bild 3.33** 

Mitglieder der Gruppe www-data haben

nun Schreib- und Leserechte auf die

Inhalte des Webserver-Stammverzeich-

nisses. Allerdings müssen die berech-

tigten Benutzer auch dieser Gruppe

angehören.

Im Testsystem für dieses Buch heißt der reguläre Benutzer „moodle2“. Dieser Benutzer soll nun Mitglied der Gruppe _www-data_ werden, welche Zugriff auf das Stammverzeichnis des Webservers haben darf. Das kann mit einer einfachen Kommandozeile erledigt werden.

Doch Achtung: Alle administrativen Vorgänge, die Benutzer und Benutzergruppen betreffen, erfordern Rechte des Systemverwalters. Darum muss auch hier das Kommando „sudo“

vorangestellt und der Befehl noch mit der Eingabe eines Passworts freigegeben werden.

sudo usermod -aG www-data moodle2 [Enter]

Ist auf dem Linux-System ein ftp-Server installiert, was durchaus zu empfehlen ist, wenn die Moodle-Dateien über ein Netzwerk oder sogar via Internet verwaltet werden sollen, so wird auch hier der Upload scheitern, wenn die Benutzerdaten nicht denen entsprechen, wie sie der Zugriff auf das Verzeichnis erwartet.

„usermod“ kann frei als Benutzer-Modifizierung gedeutet werden. Gemeint sind die Deklarationen der Eigenschaften wie zum Beispiel Gruppenzugehörigkeiten, die mit einem Benutzer verbunden werden. Auch neue Passwörter können mit diesem Kommando gesetzt werden.

![Image 37](index-98_1.png)

3.3 Webserver-Software

**75**

**Bild 3.34** Das Webserver-Stammverzeichnis kann von Mitgliedern der Gruppe _www-data_ erreicht werden und der Benutzer (hier moodle2) ist Mitglied dieser Gruppe. Auch wurden die Zugriffsrechte für die Gruppenmitglieder angepasst. Nun ist auch die Übertragung der Moodle-Dateien per FTP

(hier mithilfe von FileZilla) erfolgreich.

Ganz wichtig sind auch die beiden Optionen „ _-a_“ _**und**_ „ _-G_“, die unbedingt gemeinsam verwendet werden müssen. Der Option „-G“ folgt der Name der Gruppe bzw. die Liste von Gruppen, welcher der Benutzer angehört oder nicht mehr angehören soll. Das Problem ist: Wird diese Option alleine verwendet, so überschreibt der Befehl die vorherigen Deklarationen. Möglicherweise ist der Benutzer dann plötzlich nicht mehr Mitglied anderer wichtiger Gruppen, denen er zuvor angehörte. Dies verhindert die Option „-a“, die dafür sorgt, dass neue Deklarationen an die bestehende Liste angehängt werden, ohne vorherige Einträge zu löschen.

**3.3.4.8■Der Cron-Job**

Regelmäßige, periodisch ablaufende Prozesse lassen sich sowohl in MS-Windows- als auch in UNIX-ähnlichen Betriebssystemen (Linux, OS X) automatisiert starten. In der MS-Windows-Umgebung gibt es einen speziellen Verwaltungsassistenten, die _Aufgabenplanung_.

UNIX, Linux etc. sehen mit _cron_ ein Standardprogramm vor, das sehr einfach über eine tabellarisch gestaltete Konfigurationsdatei – die _crontab_ – gesteuert werden kann.

![Image 38](index-99_1.png)

![Image 39](index-99_2.png)

**76** 3 Der Moodle-Server

Die Idee der _crontab_ ist ebenso einfach wie genial: Es wird tabellarisch der konkrete Zeitpunkt und die auszuführende Aktion in jeweils eine Tabellenzeile ein getragen. Das Linux-System arbeitet diese Tabelle unentwegt durch und startet die jeweils definierten Prozesse pünktlich zur festgelegten Zeit. Neben einmaligen festen Terminen lassen sich durch Setzen eines Platzhalters – * (= Asterisk) – regelmäßige Wiederholungen programmieren.

Auch Moodle benötigt den regelmäßigen Start gewisser Aufgaben, sei es für das Aufräumen des Systems oder für die Kommunikation, zyklisch gestarteter Hintergrundprozesse. Um die Details kümmert sich ein PHP-Skript, das Bestandteil der Moodle-Installation ist. Für dessen Ausführung zu sorgen, ist allerdings Aufgabe des Systemverwalters.

**Ausführung des „cron-Skripts“ im Browser verhindern!**

Das Skript . . ./moodle/admin/cli/cron.php sollte aus Sicherheitsgründen nicht über den Webbrowser ausführbar sein. Dies kann der Moodle-Administrator direkt in seiner (Moodle)-Verwaltungs-Oberfläche festlegen. Sollte es dennoch erforderlich sein, das Skript über den Webbrowser oder sogar auf diesem Weg von einem entfernten Rechner innerhalb des Netzes zu starten, lässt sich hierzu ein Passwort festlegen.

■

**Bild 3.35** Blick in die Verwaltung des (zu diesem Zeitpunkt noch zu installierenden) Moodle-Systems: Der Start des Skripts cron.php wird hier ausschließlich über die Kommandozeile bzw. dem Systemdienst cron zugelassen.

**Bild 3.36** Bei richtiger Sicherheitskonfiguration sollte der Versuch, ein Kommandozeilenskript wie zum Beispiel cron.php zu starten, unter Ausgabe einer banalen Meldung verweigert werden!

![Image 40](index-100_1.png)

3.3 Webserver-Software

**77**

Die Konfiguration eines sogenannten „cron jobs“, der zeitlich gesteuerten Ausführung eines Kommandozeilen-Befehls, erfolgt wie bereits erwähnt über die Systemtabelle „crontab“.

Das Editieren der Tabelle – natürlich sinnvollerweise mit Systemverwalterrechten – erfolgt mit einem sehr einfachen Kommandozeilen-Befehl:

sudo crontab -e [Enter]

Es wird der bevorzugte Kommandozeilen-Editor gestartet. Das Verfahren ist allerdings einem direkten Editieren einer Tabelle, die letztlich nicht einmal „crontab“ heißt, vorzuzie-hen. Gespeichert wird die Eingabe nämlich zunächst in einer temporären Datei. Wenn der Editor geschlossen wird, prüft das Programm „crontab“, ob die Schreibweise korrekt ist. Ist dies nicht der Fall, wird eine Korrektur ange boten oder die Daten werden nicht gespeichert.

Theoretisch darf übrigens jeder Benutzer im System eine eigene crontab editieren. Diese trägt auch dessen Namen. Für die zeitliche Steuerung von Moodle-Prozessen sollte es allerdings unbedingt ein Benutzer sein, der die entsprechenden Rechte im Moodle-System besitzt. Deswegen wurde der crontab-Befehl in diesem Fall mit einem einleitenden sudo-Kommando gestartet. Man findet die Datei später im Verzeichnis _/var/spool/cron/_

_crontabs/_.

**Bild 3.37** Beispiel einer für den Start des Moodle-cron.php-Skripts editierten crontab: Das cron.php-Skript wird minütlich gestartet.

Die Struktur der Tabelle sieht zuerst die Zeitangabe für das Ereignis vor. Hierbei werden –

jeweils getrennt durch ein Leerzeichen – folgende Daten eingetragen: Minute (m, Zahl von 0 bis 59), Stunde (h, Zahl von 0 bis 23), Tag (dom, Zahl von 1 bis 31), Monat (mon, Zahl von 1 bis 12) und Kalendertag (dow, Zahl von 0 bis 7, wobei sowohl 0 als auch 7 für Sonntag stehen). Ein Asterisk (*) kann als Platzhalter verwendet werden. Der Ausdruck */1 in der Minutenspalte steht für eine Ausführung im Minutentakt.

![Image 41](index-101_1.jpg)

**78** 3 Der Moodle-Server

Nach einem weiteren Leerzeichen folgt dann der Befehl, wie er auch in die Kommandozeile geschrieben wird. Allerdings wird hier kein „sudo“ geschrieben, weil der cron-Job ohnehin in diesem Fall mit Systemverwalterrechten laufen soll.

Das Kommando wird zweckmäßigerweise mit dem vollen Pfad des ausgeführten Programms geschrieben. Hier ist es _/usr/bin/php_. Nach einem weiteren Leerzeichen wird das auszuführende Skript – ebenfalls mit dem vollen Pfad innerhalb des Systems – als Argument übergeben. In der Moodle-Dokumentation wird emp fohlen, das Skript recht häufig, nämlich im Minutentakt auszuführen. Je nachdem, wie intensiv das Moodle-System genutzt wird und welche Ansprüche an dessen Reaktionszeit gestellt werden, kann das Intervall auch verlängert werden.

Die komplette crontab-Zeile lautet somit:

*/1 * * * * /usr/bin/php /var/www/html/moodle/admin/cli/cron.php

**Bild 3.38** Die crontab-Tabellen der Benutzer – einschließlich des Systemverwalters root – werden im Verzeichnis /var/spool/cron/crontab/ gespeichert. Sie sollten nicht über beliebige Editoren, sondern stets mit dem crontab-Kommando bearbeitet werden.

**Backup des moodledata-Verzeichnisses anlegen!**

Wenn die crontab bereits bearbeitet wird, bietet es sich an, auch gleich die Datensicherung für das _moodledata_-Verzeichnis zu programmieren. Je nachdem, wie intensiv das System genutzt wird und wie kritisch ein defekter Datenträger angesehen wird, kann die Sicherung täglich oder mehrmals täglich erfolgen.

Das Zielverzeichnis sollte sich – wenn möglich – auf einem anderen physischen Laufwerk befinden als die Dateien des Webservers. Für eine tägliche Daten-sicherung33 um 2 Uhr in der Nacht kann in die crontab-Tabelle folgende Zeile geschrieben werden:

* 2 * * * cp -u /var/www/moodledata/. /home/moodle2/backup

■

33 Als Datenquelle soll das im Testsystem verwendete Verzeichnis /var/www/moodledata/ verwendet werden.

Zielverzeichnis soll hier willkürlich das Verzeichnis /home/moodle2/backup/ sein.

![Image 42](index-102_1.png)

3.3 Webserver-Software

**79**

**Bild 3.39** Auch in Windows-Systemen lassen sich regelmäßige Prozesse automatisieren und zeitlich exakt gesteuert ausführen. Dies erledigt dort die „Aufgabenplanung“.

**3.3.5■Moodle auf einem öffentlichen Webspace?**

Wer nicht gerade ein MOOC34-Projekt plant, sondern möglicherweise eine Schulungsplatt-form für die Mitarbeiter eines kleinen bzw. mittelständischen Unter nehmens aufbauen will, der kann durchaus Moodle auf den Systemen eines öffentlichen Webhosters installieren.

Diese Anbieter haben verschiedene Vorteile:

Sie sind extrem kostengünstig: Für wenige Euro im Monat bieten diese Produkte quasi ein vollständiges Webserver-Paket.

Die Server sind meist vorkonfiguriert, d. h. es läuft ein Webserver (wahlweise auf Linux oder MS-Windows) und es existiert ein funktionsfähiger Datenbankserver.

Eine Domain (z. B. srg.at) ist meist im Preis inbegriffen.

Oft ist auch ein Zertifikat (http**s**:\\) im Grundpreis enthalten, um eine sichere Kommunikation zwischen Client und Webserver zu ermöglichen.

Die Serverinstallation ist in der Regel gegen Angriffe gesichert.35

Es gibt professionellen Support.

34 MOOC = Massive Open Online Course

35 _Achtung:_ Das gilt nicht für die eigenen Installationen auf diesem System! Somit sind in den hier gemeinten Paketen auch keine Moodle-Administration und kein Support enthalten.

![Image 43](index-103_1.jpg)

**80** 3 Der Moodle-Server

Trotz aller Vorteile funktioniert eine Moodle-Installation nicht immer problemlos. Zu den häufigsten Problemen zählen hierbei:

Probleme mit der PHP-Version und der Freigabe der Erweiterungen

Einrichtung eines Moodle-Datenverzeichnisses

Aktivierung des _cron_-Dienstes

**3.3.5.1■Übertragung der Moodle-Dateien**

In der Regel ist es unkritisch, das Moodle-Paket auf den Webspace des öffentlichen Webhosters zu übertragen. Es gibt allerdings unter Umständen bereits hier die ersten Einschränkungen. So kann es vorkommen, dass die maximale Größe einer hochzuladenden Datei begrenzt wird. Im Fall des hier als Beispiel gewählten Anbieters ist der Upload einer Datei über dessen Webspace-Explorer – eine Oberfläche, die in jedem Browser funktioniert und keinerlei Installation auf dem eigenen PC erfordert – auf maximal 50 MB pro Datei limitiert.

Das Moodle-Installations paket umfasst in „gezippter“ Form jedoch über 67 MB. Es ist also deutlich zu groß und kann damit nicht ohne Weiteres über die Weboberfläche hochgeladen werden.

An dieser Stelle bietet sich die Verwendung eines FTP-Programms wie _FileZilla_ oder _WinSCP_

an. Nach dem Entpacken auf dem Webspace des Webservers – dieser befindet sich nun tatsächlich auf einem öffentlichen System – sollte das ursprüngliche ZIP-Archiv wieder gelöscht und der davon belegte Speicher wieder freige geben werden.

**Bild 3.40** Das Moodle-(ZIP)-Archiv wurde in den dafür vorgesehenen Ordner kopiert und entpackt.

Aufgrund der Größe der ZIP-Datei konnte die Weboberfläche des Anbieters nicht verwendet werden.

![Image 44](index-104_1.png)

3.3 Webserver-Software

**81**

**3.3.5.2■Datenbank für den öffentlichen Webspace**

**Nur eine Datenbank im Tarif?**

Einen vollwertigen öffentlichen Webspace inkl. einer eigenen Domain, PHP-Unterstützung und einer Datenbank bekommt man heute bereits für weniger

als 10 € im Monat. Grundsätzlich ist natürlich vor der Wahl des Produkts zu prüfen, ob dieser Webserver die Voraussetzungen für den Betrieb von Moodle erfüllt. Ist nur eine einzige Datenbank im Angebot enthalten, so ist das für ein kleines Moodle-System nicht zwingend ein K. o.-Kriterium. Jede Tabelle

innerhalb der Datenbank kann durch ein sogenanntes Präfix eindeutig einer Nutzung zugeordnet werden und so können mehrere Seiten gemeinsam diese

(eine) Datenbank nutzen. Kommt es jedoch auf eine möglichst gute Perfor-

mance für bereits mittlere Systeme an, so ist von einem solchen Minimal -

system abzu raten. Moodle sollte grundsätzlich exklusiv eine eigene Datenbank nutzen.

■

Auch die Datenbank ist bei diesem öffentlichen Anbieter sehr schnell eingerichtet und konfiguriert. Idealerweise kann Moodle exklusiv eine eigene Datenbank verwenden. Müssen sich mehrere Web-Publikationen eine gemeinsame Datenbank teilen, so ist dies technisch zwar möglich, aber aus verschiedenen Gründen nicht empfehlenswert. Der wichtigste Grund ist die System-Performance. Jeder Zugriff auf die Datenbank fordert Rechenzeit und bremst damit das System. Zudem expandiert eine gemeinsam von mehreren Publikationen genutzte Datenbank sehr rasch. Die zunehmende Größe bremst ebenfalls die Verarbeitungsgeschwindigkeit.

**Bild 3.41** Hier kann man sehr entspannt arbeiten: Für jede Publikation kann eine exklusive Datenbank erstellt werden.

![Image 45](index-105_1.png)

![Image 46](index-105_2.png)

**82** 3 Der Moodle-Server

**Bild 3.42** Das war es auch schon mit der Datenbank-Einrichtung: Als Typ und Version wird der aktuellste Stand gewählt. Das Passwort sollte möglichst sicher sein und darf deswegen ruhig etwas länger gestaltet werden.

**Bild 3.43** In dieser Übersicht sind alle wichtigen Zugangsdaten zusammengefasst, die für die Installation des Moodle-Systems benötigt werden. Das Passwort sollte man sich allerdings merken.

![Image 47](index-106_1.png)

3.3 Webserver-Software

**83**

**3.3.5.3■Webserver und Moodle-Datenverzeichnis**

Das Moodle-Datenverzeichnis wird oft als Sorgenkind einer Moodle-Installation auf einem Pauschal-Webspace betrachtet. Das liegt daran, dass ein Verzeichnis zu wählen ist, welches nicht direkt über das Internet erreichbar sein darf und dennoch dem Webserver Zugriffsrechte einräumt.

Im Beispiel wurde in einem Verzeichnis _/eem-moodle/_ ein Unterverzeichnis _/eem-moodle/_

_moodle/_ eingerichtet. In diesem Verzeichnis befinden sich die Dateien des Moodle-Pakets.

Es wird künftig das Stammverzeichnis des Moodle-Systems werden.

Neben dem Moodle-Verzeichnis wird nun ein neuer Ordner erzeugt: _moodledata_. Er ist also nicht über den Webbrowser erreichbar und erfüllt damit die Voraussetzungen für die Moodle- Installation. In diesem Fall gibt es sogar einen direkten Pfad, der in das Moodle-Installationsskript eingetragen werden kann.

Kann der Dateipfad nicht ermittelt werden oder muss aus einem besonderen Grund das Moodle-Datenverzeichnis direkt in das Moodle-Stammverzeichnis platziert werden, gibt es auf einem Linux-System eine Alternative: die (versteckte) Systemdatei _.htaccess_ 36, _die in_ _das Datenverzeichnis (z. B.: **moodledata**) hineingeschrieben wird_. Sie muss folgenden Inhalt haben:

order deny, allow

deny from all

Achtung: Wichtig ist, dass diese Datei mit einem Texteditor verfasst wird. Auf keinen Fall sollte eine Textverarbeitungssoftware wie MS-Word oder LibreOffice verwendet werden.

Diese erzeugen formatierten Text, der hier unbrauchbar ist. Wird eine solche Datei auf einem Windows-Computer erstellt, sollte ein „Dummy-Text“ vor dem Punkt geschrieben und der Dateiname auf dem Server wieder korrigiert werden. Der Grund: MS-Windows sieht den Ausdruck .htaccess als eine reine Dateinamenerweiterung, der jedoch ein Dateiname zu fehlen scheint. Während alle anderen Betriebssysteme bereits in diesem Schriftzug einen gültigen Datei namen erkennen, kann MS-Windows den Namen mit dem führenden Punkt nicht deuten.

**Bild 3.44** Hier ist die Arbeit mit einem öffentlichen Webspace – zumindest bezogen auf das Moodle-Datenverzeichnis – leicht: Der absolute Pfad ist in den Details des Ordners ablesbar.

36 Ganz wichtig: Die Datei hat keinen Namen im Sinn einer Windows-Struktur! _Der führende Punkt ist Teil des Namens_ und bewirkt, dass die Datei als „versteckt“ gekennzeichnet wird. Verschiedene Programme wie WinSCP blenden sie deswegen aus. _.htaccess_ kann mit der Tastenkombination **Strg**+**Alt**+**H** eingeblendet werden.

![Image 48](index-107_1.png)

**84** 3 Der Moodle-Server

**3.3.5.4■PHP-Erweiterungen ohne Zugriff auf php.ini**

Etwas aufwendiger ist es, fehlende PHP-Erweiterungen zu aktivieren. In vielen Fällen hat der Kunde eines öffentlichen Webspaces keinen direkten Zugriff auf die dazu erforderliche Datei _php.ini_. Das hat auch durchaus gute Gründe, denn solcher Webspace ist für einen breiten Kundenkreis entwickelt worden, der meist keinerlei IT-Ausbildung besitzt und dennoch möglichst funktionsreiche Webseiten erstellen möchte. Die Kunden besitzen hier zwar einen eigenen und individuell gestaltbaren Webspace, teilen sich jedoch meist die Rechenleistung des Webservers mit anderen Benutzern. Der Zugriff auf das Betriebssystem wird unterbunden, um ungewollten Schaden zu vermeiden.

Man muss also eine _eigene_ Datei _php.ini_ erzeugen und diese dann in das Stammverzeichnis der Moodle-Installation kopieren. Bedauerlicherweise genügt dies noch nicht, denn eine Datei _php.ini_ oder wie in diesem Fall ein Systemlink auf die Datei aus dem Stammverzeichnis muss sich auch in jedem einzelnen Unterverzeichnis befinden. Unnötig, darauf hinzuweisen, dass dies mithilfe eines gewöhn lichen FTP37-Programms oder gar über eine Web-Oberfläche zum Datei-Upload eine müßige, zeitraubende und vor allem fehlerträchtige Angelegenheit ist. Es gibt jedoch eine Alternative, wenn man eine Kommandozeile benutzen kann. Das ist bedauerlicherweise nicht so einfach wie bei einem lokalen Zugriff auf einen eigenen Computer.

Mit dem Programm _PuTTY_ 38 gibt es jedoch eine Lösung. Dieses Programm stellt eine verschlüsselte Verbindung zum eigenen Webspace über das Internet her und öffnet ein Terminal, also eine Kommandozeilenoberfläche. Der Dialog auf dieser Oberfläche startet mit der Eingabe der Zugangsdaten. Diese müssen unter Um ständen zuvor in der Administrationsoberfläche des jeweiligen Anbieters festgelegt worden sein.

**Bild 3.45** 

In der Regel erfordert die Kontaktaufnahme

zum eigenen Webspace mithilfe von PuTTY

lediglich die Server-Adresse – diese liefert

der Anbieter – und die persönlichen

Zugangsdaten, die in der sich öffnenden

Konsole eingegeben werden müssen.

37 FTP steht für File Transfer Protocol. Es ist ein bedeutender Übertragungsstandard für Dateien über das Internet bzw. innerhalb von IP-Netzwerken allgemein.

38 PuTTY kann kostenlos über die Entwicklerseit[e _www.putty.org_ her](http://www.putty.org)untergeladen werden. Der Begriff TTY ist übrigens eine sehr alte Abkürzung für **T**ele**ty**pewriter (Fernschreibmaschine).

![Image 49](index-108_1.png)

3.3 Webserver-Software

**85**

**php.ini zuerst vorbereiten!**

Die Datei _php.ini_ wird mit den gewünschten Einstellungen am besten offline in einem Texteditor bearbeitet und dann über die Weboberfläche des Anbieters oder mit einem FTP-Programm (z. B. FileZilla oder WinSCP) in das Moodle-Stammverzeichnis des Webservers kopiert. Anschließend ist ein Neustart des Webservers erforderlich!

■

Nach der Anmeldung mit den persönlichen Zugangsdaten werden die beiden folgenden Kommandozeilen eingegeben. „stammverzeichnis“ steht hier für den jeweils individuellen Pfad zum Moodle-Stammverzeichnis. Darin sollte sich bereits die bearbeitete Datei _php.ini_ befinden. Damit werden _Systemlinks_ in alle Unterverzeichnisse geschrieben.

cd stammverzeichnis [Enter]

find -type d -exec ln -s $PWD/php.ini {}/php.ini \; [Enter]

Es muss darauf hingewiesen werden, dass die Ausführung der zweiten Kommandozeile zumindest eine Fehlermeldung verursachen wird, die jedoch zu ignorieren ist. Der Fehler entsteht, weil der Befehl versucht, auch im Stammverzeichnis einen _Systemlink zur php.ini_ anzulegen. Dies ist jedoch weder möglich noch nötig, weil die Datei bereits existiert.

Sollte sich herausstellen, dass Einstellungen zu ändern oder weitere Freigaben zu aktivieren sind, so genügt es, ausschließlich die Datei _php.ini_ im Moodle-Stammverzeichnis zu bearbeiten. Die Änderungen werden aufgrund der Systemverlinkungen automatisch auch in den Unterverzeichnissen wirksam.

**Bild 3.46** Ein symbolischer Systemlink auf die Datei php.ini (aus dem Moodle- Stammverzeichnis) wird in jedes Unterverzeichnis kopiert. Die Fehlermeldung ist in diesem Fall zu ignorieren.

**86** 3 Der Moodle-Server

**■**

**■ 3.4■Moodle einer Domain zuweisen**

Im Internet hat jede Webseite eine Adresse in Klarschrift, den sogenannten URL39. Eine solche Adresse besteht aus mindestens drei Teilen, die von rechts nach links gelesen werden:

Die Toplevel-Domain steht beispielsweise für das Land (.de, .at etc.) oder (ursprünglich40) für eine besondere Nutzergruppe (.org, .com, .info etc.).

Die Domain ist die persönliche Wunschadresse der eigenen Publikation.

Die Subdomain (meist www) erlaubt es, verschiedene Web-Publikationen zu einer einzigen Domain zu erstellen. So kann eine Schule durchaus eine reguläre Webseite mit den klassischen Informationen und zusätzlich eine Moodle-Plattform auf einer gemeinsamen Domain betreiben.

Die Zuordnung dieser Adresse zu einer im Netzwerk gültigen IP-Adresse übernimmt der Anbieter des Webspaces bzw. letztendlich die jeweils zuständige Institution. Die Zuordnung der Subdomain zu einem Stammverzeichnis auf dem Webserver muss der Seitenbetreiber in der Regel selbst erledigen. Dies ist allerdings relativ einfach:

Zuerst wird ein Name für die Subdomain gewählt. Dieser sollte nicht zu kompliziert sein.

Man denke daran, dass die Adresse oftmals per Hand in die Adresszeile des Webbrowsers eingetragen wird. Im schlimmsten Fall passiert dies auf einem Smartphone mit kleinem Display und nicht am PC mit einer Tastatur. Der Name sollte zudem aussagekräftig sein. Oft wurde für Lernplattformen als Subdomain verwendet:

moodle

elearning bzw. e-learning

lms41

Im zweiten Schritt wird die neu angelegte Subdomain dem Verzeichnis des Webservers zugeordnet, in das die Moodle-Dateien hineinkopiert werden (das Stammverzeichnis!). Dies wird zumeist durch einen Navigationsassistenten erleichtert, in dem das Verzeichnis per Mausklick ausgewählt wird. Ist dies erledigt, sollte der Moodle-Installationsdialog über das Internet aufrufbar sein, wenn in den Web browser eine Adresse nach diesem Schema eingegeben wird:

Subdomain.eigeneDomain.toplevelDomain

z. B.: moodle.e-emotion.net

39 URL steht für **U**niform **R**essource **L**ocator

40 Man ist heute recht liberal in der Vergabe von Internet-Adressen, auch wenn sie nicht immer wirklich zur Toplevel-Domain passen.

41 LMS als Abkürzung für **L**ern-**M**anagement-**S**ystem

![Image 50](index-110_1.png)

![Image 51](index-110_2.png)

3.4 Moodle einer Domain zuweisen

**87**

**Bild 3.47** Es wird ein aussagekräftiger Name für eine Subdomain gewählt. Damit können unter einer einzigen Domain diverse voneinander unabhängige Internet-Publikationen angeboten werden.

**Bild 3.48** Die Subdomain wird nun einem Ordner auf dem Webserver zugewiesen, auf dem sich die Startseite der Publikation – meist die Datei index.php – befindet.

**88** 3 Der Moodle-Server

**■**

**■ 3.5■Bei Upgrade/Update zu beachten**

Nichts ist ärgerlicher und – im Wirkbetrieb einer Schule bzw. Hochschule auch rechtlich –

katastrophaler als ein Datenverlust bei einer Systembeschädigung. Diese können vielfältige Ursachen haben:

Defekter Datenträger

Folgen eines Hackerangriffs

Unzuverlässiger Dienstleister

„Menschliches Versagen“

Werden Leistungen von _Students_ rein online in einer digitalen Lernumgebung erbracht, so haben auch diese rechtlich verbindliche Relevanz. Letztlich geht es auch um die Karriere und um die Anerkennung von Abschlüssen für die Lernenden. Es ist deswegen unabdingbar, für eine nahezu zuverlässige Verfügbarkeit der Daten zu sorgen und dies im Schadensfall auch nachweisen zu können.

Moodle bietet systemintern bereits einige Optionen zur Erstellung von Sicherheitskopien.

Diese können auch von einzelnen _Teachern_ bei Bedarf genutzt werden, beispielsweise um die eigenen Kurse auf einem individuellen Datenträger zu sichern. Es ist aber auch sinnvoll, über das Moodle-System hinaus Sicherheitskopien auf der Ebene des Betriebssystems anzufertigen. Nicht zuletzt sind solche Backups sehr wichtig, wenn das Moodle-System erweitert oder aktualisiert werden soll. Auch bei einem direkten Umbau der Server-Plattform gehört ein Backup des Gesamtsystems zum guten Ton.

**3.5.1■Datenbank sichern**

Die Datenbank ist das zentrale Element von Moodle. Hier werden die Daten der Benutzerinnen und Benutzer, die Kursdetails und die darin erreichten Fortschritte und vieles mehr gespeichert. Die Inhalte der Datenbank lassen sich auch außerhalb des Moodle-Systems in der Verwaltungsoberfläche wie zum Beispiel in _phpMyAdmin_ gezielt sichern. Das betrifft sowohl einzelne Tabellen der Datenbank als auch die gesamte Datenbank. Die Aufteilung einer Tabelle ist meist zu emp fehlen, da oft die maximale Größe eines Tabellenimports stark begrenzt ist. Die Einstellung der maximal möglichen Upload-Größe wird in der Datei _php.ini_ 42 festgelegt. Der Standardwert liegt meist bei nur 2 Mbyte. Für die meisten kleinen Datenbanken ist dieser Wert ausreichend. Spätestens jedoch dann, wenn es darum geht, umfangreiches Lehrmaterial über die Moodle-Oberfläche in das System hochzuladen, wird die Grundeinstellung in der Datei _php.ini_ Probleme bereiten. Hier sind sowohl Anpassungen bei der maximalen Dateigröße als auch in der zuläs sigen Ausführungszeit eines Skripts erforderlich, denn mehrere gleichzeitige Zugriffe auf den Server in Verbindung mit der Übertragung großer Dateien können eine gewisse Zeit in Anspruch nehmen. Läuft diese ab, kommt es zu einer Fehlermeldung!

42 Die Details wurden im Zusammenhang mit der Einrichtung und der Konfiguration des Webservers beschrieben.

3.5 Bei Upgrade/Update zu beachten

**89**

**Upload-Größen können ein Streitthema werden**

Laufen sowohl das Moodle-System als auch der Webserver auf der gleichen

Maschine, wird es allein für einen praxistauglichen Betrieb von Moodle sinnvoll sein, die Upload-Größen zu erhöhen. Bei Datenbanken ist man in der Regel bemüht, diese in ihrer Größe nicht zu sehr zu eskalieren, damit die Performance, also die Verarbeitungsgeschwindigkeit, nicht unzumutbare Dimensionen annimmt. Denkbar ist es aber, Datenbank und Moodle auf getrennten Servern zu installieren.

■

Zu verändern sind folgende Werte:

upload_max_filesize

post_max_size

Optional:

max_execution_time

max_input_time

memory_limit

Der eigentliche Export der Datenbank über die Oberfläche _phpMyAdmin_ erfordert gültige Zugangsdaten. Darüber hinaus ist die gesamte Prozedur fast ausschließlich mit sorgfältig gesetzten Mausklicks zu erledigen. Der Export einer Datenbank sollte nach der _angepassten_ _Eingabemethode_ erfolgen. Damit werden alle Optionen dargestellt und der Export kann optimal eingestellt werden. Für eine vollständige Sicherheitskopie der Datenbank werden sowohl die Struktur als auch die Daten aller Tabellen markiert.

**Eine Datenbank für verschiedene Web-Publikationen?**

Wie erwähnt, ist es sinnvoll, eine für das Moodle-Lernmanagementsystem

exklusiv reservierte Datenbank zu betreiben. Rein technisch ist es allerdings bei kleinen Systemen aufgrund billiger Pauschalangebote für Webspace möglich, in einer einzigen Datenbank Tabellen verschiedener Systeme zu speichern.

So kann neben Moodle möglicherweise auch eine WordPress-Plattform in der Datenbank enthalten sein. Die Tabellen unterscheiden sich in ihrem Tabellen-Präfix voneinander. Sinnvoll ist eine solche Kombination nicht!

■

Wird entgegen der Empfehlung eine Datenbank für mehrere Websysteme (neben Moodle zum Beispiel Joomla!, Typo3, WordPress etc.) genutzt, so müssen die Tabellen tatsächlich einzeln markiert und damit für den Export selektiert werden. Das ist sehr aufwendig und birgt das Risiko eines Fehlers in sich. Werden Daten vergessen, wird es schwierig, ein zerstörtes System wieder zu reaktivieren.

![Image 52](index-113_1.jpg)

**90** 3 Der Moodle-Server

**Bild 3.49** In der Datenbank-Verwaltungsoberfläche – hier phpMyAdmin – werden alle Tabellen der Datenbank (moodle) mit ihrer Struktur und den Dateninhalten ausgewählt.

Eine weitere wichtige Einstellung betrifft das Ausgabeformat. Es ist auf jedem Fall der Zeichensatz der Datei zu beachten. Diese Einstellung muss später beim Import der Datenbank bekannt sein, da die Inhalte sonst nicht lesbar sind. In einem Moodle-Produktivsystem kann die Datenbank mit der Zeit eine recht beachtliche Größe annehmen. Es ist deswegen sehr zu empfehlen, die exportierten Daten zu komprimieren. Zur Auswahl stehen folgende Optionen:

Keine Kompression der Datei

ZIP-Kompression

GZIP-Kompression

Im Wesentlichen können die übrigen Einstellungen zumeist übernommen und der Export durch einen Klick auf die OK-Schaltfläche abgeschlossen werden.

Der Import einer auf diese Weise gesicherten Datenbank ist sehr einfach: Im Register

„Importieren“ der _phpMyAdmin_-Oberfläche wählt man die zu importierende Datenbank bzw. das ZIP- oder GZIP-Archiv und lädt dieses über das Webformular hoch. Spätestens an dieser Stelle wird man mit der maximalen Dateigröße konfrontiert. Die Größe der Daten-bankdatei muss innerhalb des Grenzwerts liegen.

![Image 53](index-114_1.jpg)

3.5 Bei Upgrade/Update zu beachten

**91**

**Bild 3.50** Die Kompression der Datenbank ist zu empfehlen, weil sehr häufig Restriktionen in der Dateigröße für den Upload von Datenbanken definiert werden. Unter Umständen muss die Datenbank sogar in mehrere Teile gesplittet oder die Datei _php.ini_ geändert werden.

**3.5.2■Sicherheitskopie des Moodle-Datenverzeichnisses**

Den Inhalt des Moodle-Datenverzeichnisses sichert man am einfachsten automatisch auf der Ebene des Betriebssystems. Die hierzu eingesetzten Werkzeuge sind bereits aus der Konfiguration des Servers bekannt:

MS-Windows: _Aufgabenplanung_

Linux etc.: _cron_

Im Normalfall wird es ausreichen, lediglich einmal am Tag eine komplette Sicherung des Moodle-Datenverzeichnisses durchzuführen. Bild 3.51 zeigt eine Konfiguration der _crontab_.

Hier wird die Sicherung des Moodle-Datenverzeichnisses jeweils in der Nacht um 02:00 Uhr ausgeführt. In die _crontab_ wird ein Kopierbefehl (cp) programmiert. Damit wird der Inhalt des gesamten Moodle-Datenverzeichnisses inklusive aller Unterverzeichnisse kopiert.

![Image 54](index-115_1.png)

**92** 3 Der Moodle-Server

**Wichtig!**

Es ist wichtig, die Sicherheitskopien auf ein eigenes physisches Laufwerk durchzuführen. Bei besonders sensiblen Daten ist auch eine örtliche/räumliche Trennung der Speicherorte zu empfehlen, um auch im Fall eines Brands oder eines Einbruchs keine Daten zu verlieren.

■

**Bild 3.51** Die crontab sieht zwei programmierte Aufgaben vor: Die erste (weiße) Zeile programmiert die Ausführung des Skripts cron.php einmal pro Minute. Die zweite (weiße) Zeile ist ein Kopierbefehl des Moodle-Datenverzeichnisses, der täglich um 02:00 Uhr ausgeführt wird.

**3.5.3■Moodle-Verzeichnis**

In vergleichbarer Weise wie beim Moodle-Datenverzeichnis kann auch das gesamte Moodle-Verzeichnis automatisch gesichert werden. Das hat den Vorteil, dass auch die Skripte aller installierten Erweiterungen gesichert werden. Im Fall einer Zerstörung der Server-dateien kann das Moodle-System so sehr schnell wiederhergestellt werden.

**3.5.4■Backup-Funktionen in Moodle**

An dieser Stelle soll bereits vorgreifend erwähnt werden, dass auch einzelne Kurse in Sicherheitskopien gespeichert werden können. Diese Datensicherungen können Teacher individuell ausführen. Details beschreibt ein späteres Kapitel

