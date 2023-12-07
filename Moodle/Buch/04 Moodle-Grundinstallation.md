Nachdem die Systemvoraussetzungen für Moodle geschaffen wurden, kann das Programmpaket in der gewünschten Version heruntergeladen und installiert werden.

## 4.1 Moodle-Programmpakete

Die Moodle-Programmpakete können aus verschiedenen Quellen bezogen werden. Die individuelle Verbreitung von Moodle ist durchaus legal, denn Moodle ist eine quelloffene Software, die unter der _GNU General Public Licence_ vertrieben wird. Dennoch ist es zu empfehlen, die Installationspakete direkt von der Projektseite [_https://moodle.org_](https://moodle.org) bzw. einer dort empfohlenen Quelle zu beziehen. Damit wird nicht nur sichergestellt, dass es sich um eine originale Version der Projektgruppe handelt, sondern auch die Chance erfolgreicher Updates und Upgrades gesteigert. Über diese Seite wird auch eine Dokumentation – vieles bereits in deutscher Sprache, ganz gewiss jedoch in Englisch – geboten, die oft Detailfragen zu klären hilft.

![Image 55](index-117_1.jpg)

**94** 4 Moodle-Grundinstallation

**Bild 4.1** Die offizielle Moodle-Seite – [_moodle.org_](http://moodle.org) – ist der beste Garant dafür, die stets aktuelle und sicherste Moodle-Version zu beziehen.

Bei der Auswahl des jeweiligen Programmpakets für eine Neuinstallation sollte die Entscheidung in der Regel auf die aktuellste Entwicklungsstufe fallen. Es gibt jedoch eine begründete Ausnahme, die für die Installation einer älteren Version sprechen kann: Es werden dringend Plugins benötigt, die es für eine neuere Version noch nicht oder nicht mehr gibt.

Der Normalfall ist (und sollte es sein), die aktuellste Version zu verwenden. Dies kommt der Kompatibilität zu aktuellen Web-Technologien sowie der Sicherheit des Systems gegen externe Angriffe zugute. Auch die Rechtssicherheit spielt in diesem Zusammenhang eine wichtige Rolle, denn die Datenschutzgrundverordnung ( DSGVO) sieht Sanktionen auch bei unbeabsichtigtem Datendiebstahl vor, wenn die Sicherheitsvorkehrungen nicht dem Stand der Technik entsprechen. Die DSGVO greift deswegen im Zusammenhang mit Moodle, weil die darin aktiven Benutzerinnen und Benutzer (Students, Teacher etc.) sehr persönliche Daten im System hinterlassen.

Alternativen zum direkten Download sind u. a.:

Installation aus den Paketverwaltungen der Linux-Distributionen

Installation von Datenträgern in Fachpublikationen

![Image 56](index-118_1.jpg)

4.2 Moodle in verschiedenen Umgebungen

**95**

**Bild 4.2** Man kann nahezu jede Moodle-Version aus den Archiven herunterladen und an den jeweils verfügbaren Webserver angepasst installieren. Der grundsätzliche Rat ist aber, die jeweils aktuelle Version zu wählen und, falls erforderlich, den dafür nötigen Webserver auf den neuesten Stand der Technik zu bringen.

**■**

**■ 4.2■Moodle in verschiedenen Umgebungen**

Nachdem bekannt ist, woher man Moodle (legal und kostenlos) bekommen kann und welche Voraussetzungen der für dessen Betrieb erforderliche Webserver erfüllen muss, kann es daran gehen, das erste Moodle-System selbst zu installieren. Der einfachste Weg, der allerdings ausschließlich für das Selbststudium und zum Kennenlernen des Systems sinnvoll ist, ist die Installation eines XAMPP-Komplett-Pakets für Windows-Computer. Eine solche Version kann über die Projektseite von Moodle.org heruntergeladen werden. Auch der direkte Download und die Installation in eine bestehende Serverumgebung sind natürlich vorgesehen und unter Profis gängige Praxis. Die Installation von Moodle mit Hilfe des Ver-sionsverwaltungssystems _git_ erleichtert es, Moodle stets auf dem aktuellsten technischen Stand zu halten.

![Image 57](index-119_1.jpg)

**96** 4 Moodle-Grundinstallation

**4.2.1■XAMPP-Moodle-Installer-Package**

Es ist gewissermaßen das „Rundherum-Sorglos-Paket“, welches vom Moodle-Projekt auch für die direkte Verwendung auf MS-Windows- und Apple-Computern angeboten wird. Natürlich kann man mithilfe dieses Pakets ein vollwertiges und zum späteren Live-Einsatz vorgesehenes System aufbauen und konfigurieren. Allerdings sei an dieser Stelle klar betont, dass die _Moodle-Installer-Packages_ zunächst einmal für den Einsatz in _internen, geschlossenen Umgebungen_ vorgesehen sind. So werden, wenn überhaupt, Standardpasswörter in den Server-Umgebungen verwendet. Das System ist damit bei einem direkten öffentlichen Zugriff durchaus an greifbar.

**Zum Lernen und Testen**

Die kompakten _Moodle-Installer-Packages_ eignen sich natürlich ganz hervorragend zum Selbststudium des Systems. Der Vorteil dabei ist, dass man nicht wirklich viel falsch machen kann. Wer eine Sicherheitskopie anfertigt, bevor tiefgreifende Experimente durchgeführt werden, kann sich möglicherweise

viel Arbeit ersparen und sich dennoch weit mehr zu versuchen wagen, als

dies in einem Live-System möglich und erlaubt wäre. Die Moodle-Installer-Packages eignen sich aber auch dazu, neue Versionen des Moodle-Systems

zu testen und sich vor der Umsetzung in der eigenen Produktivumgebung mit eventu ellen Neuheiten vertraut zu machen.

■

Der Download erfolgt mit einem Klick auf eine der unscheinbaren Link-Zeilen. Hier ist darauf zu achten, die richtige Version für das gewünschte Betriebssystem zu wählen.

**Bild 4.3** Das Moodle-Installer-Package kann wahlweise für einen MS-Windows- oder einen Mac-OS-X-Computer bezogen werden. Alle erforderlichen Server-Programme sowie Daten banken sind darin bereits enthalten und vorkonfiguriert.

Das in diesem Beispiel heruntergeladene ZIP-Archiv des Moodle-Installer-Packages für Windows hat eine Größe von ca. 188 MB. Dabei handelt es sich um komprimierte Daten, wohlgemerkt. Entpackt zeigt sich der Inhalt des Pakets mit einem Speicherbedarf von rund

![Image 58](index-120_1.png)

4.2 Moodle in verschiedenen Umgebungen

**97**

680 MB nicht gerade bescheiden auf der Festplatte. Die Größe des Archivs fordert auch beim Entpacken ihren Tribut an Rechenleistung und Zeit. Je nachdem, wie schnell der eigene PC ist, kann es sich durchaus lohnen, während des Entpackens in aller Ruhe eine Tasse Kaffee zu trinken.

**Große ZIP-Archive fordern den Computer!**

Das Entpacken großer ZIP-Archive kann unter Umständen eine gewisse Zeit

beanspruchen. Wie lange der Vorgang dauert, hängt wesentlich von der allgemeinen Leistungsfähigkeit und der Auslastung des eigenen Computers ab.

Es empfiehlt sich deswegen, auch bei längeren Entpackungszeiten Geduld

zu haben und etwas abzuwarten.

■

**Bild 4.4** Das ZIP-Archiv des gepackten Moodle-Installer-Packages hat ein Volumen von stolzen 180 MB. In ein eigenes Verzeichnis entpackt, beansprucht das Paket sogar 680 MB Plattenspeicher!

Mit dem Entpacken liegen nun bereits alle wichtigen Dateien und Verzeichnisse auf dem eigenen Computer vor. Eine kurze Anleitung zum Start und zum Beenden des Servers bietet die mitgelieferte Readme.txt-Datei, die mit einem ganz gewöhnlichen Text-Editor (z. B.

das einfache Programm notepad.exe) gelesen werden kann. Der Server – genauer, der Apache2-Webserver inkl. PHP und die erforderliche Datenbank – wird mit dem Programm _Start Moodle.exe_ aktiviert. Im hier verwendeten Beispiel wurde eine Entwicklungsversion Moodle 3.9 heruntergeladen. Die dazu mitgelieferte (XAMPP)-Server-Version umfasst:

![Image 59](index-121_1.png)

![Image 60](index-121_2.png)

**98** 4 Moodle-Grundinstallation

Apache 2.4.41

PHP 7.3.11

MariaDB 10.4.8

**Bild 4.5** Der Inhalt des Moodle-Pakets: Der gesamte Server – einschließlich der noch zu konfigurie-renden Moodle-Installation – befindet sich im Verzeichnis _/server/._ Der (lokale) Web server wird mit den Programmen _Start Moodle.exe_ und _Stop Moodle.exe_ ein- und ausgeschaltet.

**Bild 4.6**  _Start Moodle.exe_ ist ein kleines Programm, welches auf der Kommandozeile läuft. Seine Aufgabe ist lediglich, den XAMPP-Server zu starten und dessen Dienste zu aktivieren.

Mit dem Start-Programm wird nicht nur der Server selbst aktiviert, sondern dessen aktiver Dienst im MS-Windows-Betriebssystem angemeldet. Hier wird es aus technischen Gründen zu einer Warnung der Windows-Defender-Firewall kommen. Die angebotenen Optionen sollten sehr sorgfältig geprüft werden. Fahrlässig ist es, die Firewall – wenngleich auch nur für den http-Dienst – für den Zugriff aus öffentlichen Netzwerken zu öffnen. In der Regel wird es ausreichen, die Firewall-Einstellungen so anzupassen, dass Mitglieder des privaten Netzwerks auf den Webserver zugreifen können. Zum Testen eines Moodle-Systems und für die Bereitstellung von Schulungssystemen kann dies durchaus sinnvoll sein. Weitere

![Image 61](index-122_1.png)

![Image 62](index-122_2.png)

4.2 Moodle in verschiedenen Umgebungen

**99**

Konfigurationen sind an dieser Stelle zunächst nicht nötig. Mit einer unscheinbaren Meldung in der Kommandozeile teilt der Computer nun mit, dass der Apache-Webserver und die MySQL-Datenbank (richtiger eigentlich: MariaDB) aktiv sind. Mit dem Programm _Stop_ _Moodle.exe_ wird der Server wieder deaktiviert und dessen Dienst abgeschaltet.

**Bild 4.7** 

Wer mit seinem Computer viel

unterwegs ist, zum Beispiel an

wechselnden Arbeitsplätzen

oder häufig im Hotel arbeitet,

sollte diese Einstellung sehr

gewissenhaft wählen.

**Bild 4.8** Der Server läuft! Viel ist davon natürlich nicht zu sehen, denn ein Server ist ein Dienst, der im Hintergrund die von ihm erwarteten Aufgaben erledigt. Dies gilt auch für einen Webserver.

Um die Funktion des neuen (lokalen) Webservers zu testen, kann ein nahezu beliebiger Webbrowser verwendet werden. „Nahezu beliebig“ bedeutet, dass es nach wie vor immer wieder zu kleinen Darstellungsunterschieden kommen kann, wenn zum Beispiel aktuelle HTML5- oder CSS3-Spezifikationen (noch) nicht im Browser umgesetzt werden können.

Neben den Sicherheitsaspekten ist auch dies ein treibendes Argument dafür, die Browser-Software stets auf einem aktuellen Stand zu halten und Updates regelmäßig durchzuführen.

![Image 63](index-123_1.png)

**100** 4 Moodle-Grundinstallation

Für den ersten Versuch, Moodle1 zu starten, wird als „Internet-Adresse“ im Browser lediglich die folgende Zeile eingegeben:

http://localhost [Enter]

**localhost ist „multikulturell“**

_localhost_ ist ein betriebssystemübergreifendes Synonym für den Aufruf eines Dienstes auf dem eigenen Computer. Der Aufruf der Webseite funktioniert

also sowohl auf MS-Windows als auch auf Linux-Computern (egal, welcher

Distribution) und auf Apple OS X.

■

**Bild 4.9** Das Bild zeigt zwei Besonderheiten gegenüber einer „klassischen“ XAMPP-Installation: Anstelle des Verzeichnisses /htdocs/ werden die Dateien der Web-Publikation hier in einem Unterverzeichnis /moodle/ gespeichert. Wichtig ist zudem auch das Verzeichnis /moodledata, auf das noch eingegangen wird.

Bevor Moodle bzw. dessen Installationsskript gestartet wird, soll zunächst noch ein Blick in das „Server-Verzeichnis“ geworfen werden. Es unterscheidet sich ein wenig von einem XAMPP-Server, der unabhängig von Moodle installiert wird.

Im Moodle-Paket wurde der Speicherort für die Webseiten sinngemäß umbenannt: Anstatt des sonst üblichen Verzeichnisses /htdocs2 werden die HTML- und PHP-Dateien etc. in ein Verzeichnis mit dem Namen /moodle gespeichert.

Damit der (Apache-)Webserver die Dateien auch finden kann, reicht es natürlich nicht aus, nur den Namen zu ändern. Der Webserver muss sehr genau wissen, in welchem Verzeichnis er die Moodle-Dateien finden wird. Dazu muss der Pfad zur sogenannten DocumentRoot3

1 Genau genommen, wird nicht „Moodle“ als Lernmanagement-System, sondern zuerst das _Installationsskript_ gestartet, mit dem Moodle individuell installiert und konfiguriert wird.

2 Wer eine vorhandene XAMPP-Installation verwenden möchte, dort jedoch vielleicht ein Verzeichnis mit dem Namen /htdocs vermisst, sollte prüfen, ob es ein Verzeichnis mit dem Namen /www gibt.

3 _DocumentRoot_ bedeutet frei übersetzt: Dokumenten-„Wurzel“. Es handelt sich um das Startverzeichnis, in das die Dateien und Unterverzeichnisse der gesamten Web-Publikation geschrieben werden. Befindet sich in diesem Verzeichnis eine Datei mit dem Namen index.html oder index.php, so wird diese direkt aufgerufen, ohne sie ausdrücklich benennen zu müssen. Die Schreibweise ist tatsächlich zusammenhängend, wobei sowohl das D (in Document) als auch das R (in Root) großgeschrieben werden. Dieser Schreibstil wird als _Camel-Case_ bezeichnet.

4.2 Moodle in verschiedenen Umgebungen

**101**

in eine Konfigurationsdatei mit dem Namen _httpd.conf_ eingetragen werden. Die Datei wird mit einem gewöhnlichen Texteditor4 geöffnet.

**Apache2-Konfigurationsdateien**

Etwas ärgerlich ist es, dass Konfigurationsdateien nicht immer an exakt

definierten Orten zu finden sind. Das wird durch unterschiedliche Distributionen (bei Linux), verschiedene Entwicklungsversionen oder eben auch von der

jeweiligen Umsetzung in Programmpaketen beeinflusst. Beim XAMPP-Server

lassen sich die wichtigsten Konfigurations- und Log-Dateien sehr elegant über das XAMPP-Control-Center auffinden und zur Bearbeitung öffnen (vgl. Bild 4.9).

■

**DocumentRoot finden**

Die Datei _httpd.conf_ kann sehr lang (mehrere hundert Zeilen!) sein. Es ist also sehr mühselig, die zumeist aus Kommentarzeilen bestehende Datei von oben nach unten auf der Suche nach nur einem zu prüfenden oder zu bearbeitenden Parameter durchzulesen. Mit der Tastenkombination **Strg**+[**F**] öffnet sich ein Suchdialog. In diesen wird der gewünschte Begriff eingetragen. Beispiel: _documentroot_. Wird die Suche nicht mit einem direkt am Anfang der Datei gesetzten Cursor durchgeführt, sollten zwei Suchvorgänge mit unterschiedlichen Suchrichtungen durchgeführt werden.

■

Das folgende Listing zeigt einen (stark gekürzten) Auszug aus der Konfigurationsdatei _httpd.conf_. In der ersten Zeile wird das Verzeichnis festgelegt, in dem der Apache-Webserver die Web-Dateien erwartet. Der darauffolgende Deklarationsblock <Directory ...

legt unter anderem fest, ob Regeln und wenn ja welche mit der Datei _.htaccess_ 5 für dieses Verzeichnis definiert werden können.

**DocumentRoot** “C:/Users/nUTZER/Desktop/Moodle_3-9_XAMPP/server/**moodle**“

<Directory “C:/Users/nUTZER/Desktop/Moodle_3-9_XAMPP/server/moodle“> Options Indexes FollowSymLinks Includes ExecCGI

AllowOverride All

Require all granted

</Directory>

4 _Achtung:_ Bitte kein Textverarbeitungsprogramm wie MS-Word oder LibreOffice Writer etc. verwenden!

5 Die Schreibweise der Datei _**.** htaccess_ ist tatsächlich mit einem Punkt beginnend. In einem Windows-Betriebssystem ist es hingegen nicht üblich, eine Datei ohne Dateiname allein durch deren Dateinamenerweiterung zu benennen.

![Image 64](index-125_1.png)

![Image 65](index-125_2.png)

**102** 4 Moodle-Grundinstallation

**Bild 4.10** Wenn die Einstellungen des Webservers stimmen, sollte mit dem ersten Aufruf von

„ localhost“ dieses Bild erscheinen. Es ist die Startseite des Installationsassistenten von Moodle.

An dieser Stelle soll die Beschreibung der Installation zunächst unterbrochen werden, um noch weitere Alternativen als Serverumgebung vorzustellen. Noch einmal der Hinweis: Die hier gezeigte Version dient ausschließlich der eigenen Entwicklungsarbeit von Kursen etc.

und ist nicht für Produktivumgebungen vorgesehen.

**Bild 4.11** Moodle in einer portablen XAMPP-Umgebung bietet die Möglichkeit, bereits sehr frühe Entwicklungsphasen der kommenden Version zu testen. Doch Vorsicht: Alpha- und Beta-Versionen sollten niemals in einer Live-Umgebung unter realen Nutzungsbedingungen ein gesetzt werden.

4.2 Moodle in verschiedenen Umgebungen

**103**

**4.2.2■Moodle in einer Linux-Umgebung**

Lange Zeit galt Linux als das „ominöse Akademiker-System“, wobei der Begriff „Akademiker“ noch weiter auf Informatiker einzugrenzen war. Das hat sich zum Glück gewandelt.

Zwar ist Linux gemessen an den Installationszahlen von Micro soft noch immer sehr klein bei den „Marktanteilen“ aufgestellt, jedoch ist es eine besonders kostengünstige Alternative zum kostenpflichtigen MS-Windows-Betriebssystem. Es kann sich in Komfort und Geschwindigkeit durchaus mit dem kommerziellen Dauerrivalen messen.

Die kommerziellen Betriebssysteme dominieren den Markt nicht zuletzt durch ihre ver-traglich gesicherten Kooperationen mit anderen Software-Herstellern und vor allem auch durch die weite Verbreitung von Microsofts eigener Anwender-Software wie zum Beispiel dem MS-Office-Paket.

Andererseits ist durchaus zu erwähnen, dass eine Reihe von sehr guter Software, die heute auch auf Windows-Computern läuft, ihre Wurzeln in der OpenSource-Welt und auf dem Linux-Betriebssystem hat. Beispiele sind u. a. das beliebte Bildbearbeitungsprogramm GIMP und LibreOffice. Berührungsängste mit Linux sind also unbegründet.

**Linux auch für öffentlichen Webspace**

Bei der Anmietung von öffentlichem Webspace bei großen Providern hat

man zumeist die Wahl des Server-Betriebssystems. Weil Moodle in erster

Linie auf dem offenen Linux-Betriebssystem entwickelt wurde, ist Linux an dieser Stelle meist die erste Wahl. Dies stellt jedoch keine Wertung dar.

Auch kann man heute davon ausgehen, dass das technische Personal bei

den Providern durchaus professionell beide Umgebungen administrieren

kann. Auf einem öffentlichen Webspace hat man – wie noch an späterer

Stelle zu sehen sein wird – kaum direkte Berührung mit dem Betriebssystem.

■

**4.2.2.1■Bezug der Moodle-Paket-Dateien**

Um die direkte Installation auf einem fertig eingerichteten Server durchzuführen, wird zunächst das komplette Moodle-Paket vom Server des Projekts6 herunter geladen. Dieses wird in das Webserver-Verzeichnis kopiert und dort entpackt.

**Aktuellste Version im Download-Bereich des Moodle-Projekts**

Die jeweils aktuellste Version sowie ein Link auf nützliche Zusätze wie zum Beispiel Sprachpakete und Prüfsummen sind grundsätzlich auf der Webseite des Moodle-Projekts zu f[inden:](https://download.moodle.org/releases/latest/)

[_https://download.moodle.org/releases/latest/_](https://download.moodle.org/releases/latest/)

■

6 Moodle wird auch über andere Quellen angeboten, was durchaus erlaubt ist und den GNU-Lizenzbedingungen für quelloffene Software entspricht. Es sei jedoch stets geraten, die Vertrauenswürdigkeit des Anbieters zu prüfen und kritisch zu bewerten.

![Image 66](index-127_1.png)

**104** 4 Moodle-Grundinstallation

Wie bereits angedeutet, kann Moodle neben der offiziellen Internet-Plattform der Projektgruppe auch von Quellen verschiedener Dienstleister bezogen werden. Wer keinen Vertrag mit einem Dienstleister hat, sollte grundsätzlich die originalen Quellen nutzen (siehe Kasten). Auf der Download-Seite für die jeweils aktuelle Version findet man nicht nur die In stallationsdateien in verschiedenen Ausführungen, sondern auch Links auf andere wichtige Informationen und Zusätze:

_Recent Changes log:_ Moodle wird nie fertig! An Moodle wird also permanent gearbeitet.

Wer an der Entwicklung von Moodle intensiver beteiligt ist, braucht deswegen Informationen zu den jeweils umgesetzten Änderungen. Protokolliert wird nicht nur, was getan wurde, sondern auch wer diese Änderungen wann genau ausgeführt hat.

_Upgrading notes:_ Das ist bereits ein Link, der jeden Systemverwalter interessieren muss, der ein bestehendes Moodle-System aktualisiert. Der Text enthält wichtige Informationen und Ratschläge, die vor der Ausführung der System aktualisierung zu beachten sind.

Besonderes Augenmerk sollte auf den Hinweis zu eventuellen Plugin-Updates gelegt werden. Die Entwicklung von Plugins ist leider nicht immer synchron mit der Entwicklung von Moodle insgesamt.

_Requirements:_ Hier werden die Systemvoraussetzungen für die jeweils aktuelle Moodle-Version beschrieben. Wer als Administrator für die Installation und Aktualisierung der Software verantwortlich ist, erfährt über diesen Link unter anderem, ob Aktualisierungen zum Beispiel in der PHP-Version oder bei der Datenbank nötig werden.

_Language Packs:_ Sprachpakete sind für nahezu alle Sprachen verfügbar, be ginnend bei Afrikaans bis hin zu fernasiatischen Sprachen. Doch Achtung: Die Pakete werden meist von automatischen Übersetzungsprogrammen erzeugt. Die Entwicklersprache ist Englisch. So kann es im Einzelfall schon einmal zu „humorvollen Interpretationen“ eines Begriffs kommen.

_[md5] und [sha256]:_ Über diese Links werden Hash-Werte (Prüfsummen) zu den jeweils aktuellen Programmversionen aufgerufen. Diese Prüfsummen sind gewissermaßen Fin-gerabdrücke der Dateien. Wird ein Programmpaket auch nur in einem einzigen Bit verändert, wird der Hashwert vollkommen anders aussehen. Mithilfe dieser Prüfsummen können auch Pakete anderer Quellen verifiziert werden. Der Prüfcode sollte stets gemeinsam mit dem Programm paket heruntergeladen und gespeichert werden. Er gilt nur für genau diese Version!

_Download tgz/zip:_ tgz und zip sind Kompressionsverfahren, welche beide auf Linux unterstützt werden. Auf Windows-Computern ist tgz nur mithilfe einer zusätzlichen Software zu entpacken.

**Bild 4.12** Ist die heruntergeladene Datei ein Original und damit vertrauenswürdig? Mit dem Kommando md5sum (Linux) lässt sich das feststellen. Das Ergebnis muss dem Prüfwert auf der Webseite entsprechen.

![Image 67](index-128_1.jpg)

4.2 Moodle in verschiedenen Umgebungen

**105**

**Hash-Werte verschieden?**

Bereits die Veränderung eines einzigen Bits wird dazu führen, dass der

errechnete Hash-Wert vollkommen anders aussehen wird. Das muss aber

nicht unbedingt bedeuten, dass es sich um eine gehackte Version handelt.

Der Hash-Wert ist immer auf genau eine ganz bestimmte Version bezogen.

Weichen die Werte also voneinander ab, so sollte zuerst geprüft werden,

ob die Version und das letzte Bearbeitungsdatum übereinstimmen.

■

**Bild 4.13** In diesem Fall wird die letzte Version als ZIP-Archiv vom Server des Moodle-Projekts geladen. Dieses Archiv hat eine Größe von 65,8 MB.

**4.2.2.2■Installation mit git-Versionsverwaltung**

„git“ ist ein sogenanntes Software-Konfigurations- und Management-Programm (SCM7).

Dessen Nutzung setzt voraus, dass git auf dem Server-System installiert wurde. Auf einem Linux-System kann man das mit der folgenden Kommandozeile durchführen:

sudo apt-get install git [Enter]

7 SCM = Software Configuration and Management

![Image 68](index-129_1.jpg)

**106** 4 Moodle-Grundinstallation

git ist – wie Linux und Moodle auch – Open-Source-Software, kann frei und legal aus dem Internet heruntergeladen und auch verbreitet werden. Außerdem ist git nicht nur für Linux verfügbar, sondern auch für die anderen wichtigen Betriebssysteme MS-Windows und Apple OS X.

Der Vorteil an git ist, dass alle zeitraubenden Vorgänge mit wenigen Kommandozeilen recht einfach ausgeführt werden. Das umfasst:

Download des aktuellen Programmpakets

Entpacken der Dateien

Installation in die richtigen Verzeichnisstrukturen

Ganz besonders wichtig ist aber: git erleichtert das Update! Eine bestehende Installation kann mit einer einfachen Kommandozeile auf den neuesten Stand gebracht werden: sudo git pull [Enter]

**Bild 4.14** Das Software Konfigurations- und Management-System „git“ leistet dem Moodle-Administrator wertvolle Dienste und ist für alle wichtigen Betriebssysteme kostenlos im Internet verfügbar.

**Natürlich: Systemverwalterrechte sind Voraussetzung!**

Auch beim Einsatz von _git_ muss natürlich beachtet werden, dass nicht jeder x-beliebige User in den Verzeichnissen des Webservers frei agieren darf.

Die Befehle werden somit stets mit den Rechten des Systemverwalters

ausgeführt. Dazu wird das Kommando _sudo_ der Befehlszeile vorangestellt.

■

![Image 69](index-130_1.png)

4.2 Moodle in verschiedenen Umgebungen

**107**

Nachdem _git_ auf dem Rechner installiert wurde und natürlich die erforderlichen Webserver-Voraussetzungen (Installation des Webservers, Anpassung der PHP-Erweiterungen an die Moodle-Anforderungen, Einrichtung eines Moodle-Datenverzeichnisses und einer Datenbank) erfüllt sind, können der Download und die In stallation von Moodle beginnen.

Der erste Schritt ist der Wechsel in das Stammverzeichnis des Webservers. In diesem Fall soll es heißen: /var/www/html/. Es kann natürlich auf anderen Systemen auch anders heißen. Auf einem MS-Windows-Betriebssystem, das mit XAMPP arbeitet, könnte der Pfad beispielsweise mit C:\xampp\htdocs\ definiert sein. Das Kommando cd (= Change Directory) existiert auf allen Betriebssystemen8 in der Kommandozeile. Lediglich die Schreibweise der Pfade unterscheidet sich, wie gerade gesehen.

cd /var/www/html [Enter]

Nun wird mit dem nachfolgenden Befehl das Webserver-Stammverzeichnis als eine Kopie, ein „Clon“ des _git-Servers_, definiert und darin ein neues Verzeichnis mit dem Namen _moodle_ angelegt. Da hier auch gleichzeitig die Dateien vom Server geladen werden, kann dieser Vorgang – abhängig von der Qualität der Internet-Anbindung – ein wenig Geduld beanspruchen.

sudo git clone git://git.moodle.org/moodle.git [Enter]

**Bild 4.15** Bitte keine spontanen Ergebnisse erwarten! Der Download von weit über 60 MB

benötigt seine Zeit. Es handelt sich also nicht um einen Fehler oder einen Systemabsturz!

Wenn die Dateien vollständig heruntergeladen und in das Webserver-Stammverzeichnis kopiert wurden, wird in das Moodle-Verzeichnis gewechselt und darin werden die verfügbaren Varianten des Systems einmal aufgelistet.

cd moodle [Enter]

sudo git branch -a [Enter]

Das Ergebnis ist eine recht lange Liste aus der die – zum Zeitpunkt der Verfassung dieses Buchs – aktuelle Version Moodle 3.8 ausgewählt werden soll, deren Entwicklung git künftig folgen soll:

sudo git branch –track MOODLE_38_STABLE origin/MOODLE_38_STABLE [Enter]

Abschließend wird geprüft, ob die Dateien auf dem aktuellsten Stand sind. Die Installation der Moodle-Pakete mit git ist dann abgeschlossen.

8 Auch ein MS-Windows-Computer erlaubt die Arbeit auf der Kommandozeile! Dazu wird das Programm cmd.exe – als Administrator! – ausgeführt.

![Image 70](index-131_1.jpg)

**108** 4 Moodle-Grundinstallation

sudo git checkout MOODLE_38_STABLE {Enter]

Beim Aufruf der Moodle-Seite im Webbrowser sollte jetzt der Begrüßungsbildschirm des Installationsskripts erscheinen.

**Bild 4.16** Nach dem kurzen Download-Prozess mithilfe von git sollte auch hier die Webseite funktionieren. Als Erstes erscheint die Startseite des Installationsskripts, über das nun Moodle tatsächlich eingerichtet wird.

**4.2.2.3■Updates mit git**

Eine Eigenschaft des Konfigurations- und Management-Systems _git_ ist die Versionsverwaltung. Natürlich funktioniert das nur, wenn in den Moodle-Skripten nicht beliebig der Code geändert wird. Man sollte also konsequent beim git-Verfahren bleiben und keine manuellen Änderungen im Programmpaket vornehmen. Das liegt daran, dass git jede einzelne Datei in Quelle und Ziel vergleicht und so Aktualisierungen erkennen kann. Es werden dann nur diese Dateien heruntergeladen und im System neu installiert.

Es ist dafür lediglich eine – mit Administratorrechten – einzugebende Befehlszeile9 erforderlich:

sudo git pull [Enter]

**Vor jedem Upgrade: Sicherheitskopie!**

Bevor der Befehl ausgeführt wird, sollte auch in diesem Fall eine Sicherheitskopie des Systems erstellt werden. Im idealen Fall werden das Moodle-Datenverzeichnis, aber eben auch das vollständige Moodle-Verzeichnis zeitgesteuert automatisch auf einem separaten physischen Datenträger gespeichert. Im Fall eines Fehlers beim Update lässt sich so das alte lauffähige System wiederherstellen.

■

9 Das Beispiel hier zeigt ein Linux-System. git ist allerdings auch für MS-Windows sowie für Apple OS X verfügbar.

![Image 71](index-132_1.png)

![Image 72](index-132_2.png)

4.3 Installation von Moodle

**109**

**Bild 4.17** Eine einzige Befehlszeile löst viel Aktivität aus: Aktualisierte Dateien werden vom Quell-server geladen und ersetzen die veralteten Versionen auf dem lokalen Verzeichnis.

**Bild 4.18** Es wurden Dateien ersetzt, ergänzt und gelöscht. Das Update ist abgeschlossen.

**■**

**■ 4.3■Installation von Moodle**

Der Server steht und läuft. Die Systemvoraussetzungen sind erfüllt und das _Moodle-Installationspaket_ ist heruntergeladen, entpackt und auf den Webspace kopiert worden. Nun kann also endlich die Installation des Moodle-Systems beginnen. Ganz gleich, wie die Serverumgebung gestaltet und wie die Moodle-Dateien auf das Moodle-Stammverzeichnis kopiert wurden, sollte nach dem Aufruf die Startseite des Installationsskripts erscheinen (vgl.

![Image 73](index-133_1.jpg)

**110** 4 Moodle-Grundinstallation

Bild 4.19 ). Die Installation und Konfiguration des Moodle-Systems beginnt mit der Auswahl der Systemsprache.10

Dieser Entscheidung folgt ein sehr wichtiger Dialog: Es wird die Adresse der Webseite eingetragen. Im Beispiel lautet diese http://localhost/moodle. In der Praxis wird eine gültige Internet-Adresse in dieser Zeile stehen und diese – das ist sehr zu empfehlen, um den Regeln der DSGVO im Sinne des Schutzes der IT-Infrastruktur nach dem aktuellsten technischen Stand zu entsprechen – nicht mit dem unsicheren Protokolls _http_, sondern mit dem verschlüsselten und damit gesicherten Protokoll _https_ 11 eingeleitet. Eine IP-Adresse sollte auch dann verwendet werden, wenn das System nicht nur zum reinen Test auf einem Einzel-Computer verwendet wird, sondern in einem lokalen Netzwerk zum Einsatz kommen soll. Hier wird eine feste (statische) IP-Adresse benötigt, die auch in der Webserver-Konfiguration einzutragen ist. In einem öffentlich zugänglichen Moodle-System sollte der URL als weltweit erreichbare Adresse verwendet werden.

Das Moodle-Datenverzeichnis muss mit dem vollständigen Pfad eingetragen werden. Findet das Installationsskript dieses nicht automatisch, so lassen sich die erforderlichen Daten bei einem öffentlichen Webspace in der Regel aus den Eigenschaften des Ordners ermitteln oder beim Anbieter erfragen. Auf einem lokalen Betriebssystem mit eigener Systemverwalter-Hoheit genügt im Zweifelsfall ein Blick in den Dateimanager.

**Bild 4.19** Die Einrichtung des Moodle-Systems beginnt mit der Wahl der Administrations sprache.

10 Die meisten aktiven Moodle-Installationen werden in englischer Sprache verwaltet. Im Beispiel liegt jedoch eine Version mit deutschem Sprachpaket vor, das an dieser Stelle verwendet werden soll.

11 http _**s**_ steht für Hyper Text Transfer Protocol _**Secure**_. Der Webserver muss dieses Protokoll unterstützen – was in der Regel der Fall ist – und entsprechend konfiguriert werden. Das erforderliche Zertifikat kann über den Internet-Provider erworben werden.

![Image 74](index-134_1.jpg)

![Image 75](index-134_2.jpg)

4.3 Installation von Moodle

**111**

**Bild 4.20** Die Webadresse und die beiden relevanten Speicherorte für das Moodle-System – das Moodle-Stammverzeichnis auf dem Webserver und das Moodle-Datenverzeichnis – werden meist vom Installationsskript automatisch erkannt. Klappt das nicht, können die Pfade direkt eingetragen werden.

**Webadresse „localhost“**

Bei einer lokalen (Test)-Installation wird häufig automatisch die Adresse http://localhost/… voreingestellt. Soll diese Moodle-Installation jedoch bereits innerhalb des lokalen Netzwerks (LAN) zugänglich sein, muss hier die IP-Adresse des Servers innerhalb des LAN eingetragen werden. Bei Installationen im Internet muss dies der URL sein, den auch die Benutzerinnen und Benutzer für den Aufruf von Moodle benutzen. Wird dies nicht berücksichtigt, so ändert sich automatisch die Adresse im Browser auf „localhost“ und es kommt zu

einer Fehlermeldung, dass die Seite nicht erreichbar ist (Fehlercode: 404).

■

**Bild 4.21** Die gewünschte Datenbank kann gewählt werden. Es ist durchaus denkbar, dass ein Webserver mehrere Angebote unterbreitet. Im Beispiel wurde MariaDB gewählt.

![Image 76](index-135_1.jpg)

**112** 4 Moodle-Grundinstallation

**Bild 4.22** Die Zugangsdaten für den Zugriff auf die Datenbank wurden entweder mit Systemverwalterrechten in einem Verwaltungsprogramm wie phpMyAdmin oder über einen Dialog eines öffentlichen Webspace-Anbieters festgelegt. Diese müssen nun in die Moodle-Konfigu ration eingetragen werden.

Mit der Einrichtung der Datenbank wurden folgende Mindestkonfigurationen vorgenommen:

Einrichtung eines Systembenutzers12 für das Moodle-System innerhalb des Datenbank-Management-Systems mit (auf das Notwendigste) eingeschränktem Rechtevolumen.

Damit verbunden: dessen Zugangsdaten.

Festlegung der Zeichensatzgrundeinstellung und Auswahl der Speicher-Engine.

Adresse des Datenbank-Servers.

Name der Datenbank (falls diese bereits angelegt wurde).

Diese Daten werden nun in das vom Installationsskript bereitgestellte Formular eingetragen.

12 Hier werden Zugangsdaten für den Zugriff auf die Datenbank definiert. Dieser User muss nicht zwingend einem Benutzer innerhalb des Betriebssystems entsprechen.

![Image 77](index-136_1.jpg)

![Image 78](index-136_2.jpg)

4.3 Installation von Moodle

**113**

**Bild 4.23** Die Datei config.php muss unter Umständen manuell erstellt und in das Moodle-Stammverzeichnis kopiert werden.

Damit ist die Grundkonfiguration abgeschlossen. Wenn das Moodle-Installationsskript jedoch die Konfigurationsdatei nicht in das Moodle-Stammverzeichnis schreiben kann, muss dies durch einen manuellen Eingriff vorgenommen werden, wie es Bild 4.23 bis Bild 4.25 zeigen.

**Bild 4.24** Um die Datei config.php zu erstellen, wird ein Text-Editor benötigt. Es müssen darüber hinaus Schreibrechte auf das Moodle-Stammverzeichnis vorhanden sein.

Der Inhalt der Moodle-Meldung kann einfach in ein leeres Dokument, das mit einem Text-Editor neu erzeugt wird, hineinkopiert werden. Es wird dann – mit Schreibrechten für das Moodle-Stammverzeichnis – als Datei mit dem Namen _config.php_ gespeichert. Sobald sich die Datei im Moodle-Stammverzeichnis befindet, kann das Installationsskript mit der Anerkennung der Lizenzbedingungen fortgesetzt werden.

![Image 79](index-137_1.png)

![Image 80](index-137_2.jpg)

**114** 4 Moodle-Grundinstallation

**Bild 4.25** Der Inhalt für die Datei config.php wird am einfachsten aus der Meldungsseite des Moodle- Installationsskripts in die PHP-Seite hineinkopiert. Die Daten werden direkt übernommen und entsprechen den zuvor getätigten Eingaben.

**Bild 4.26** Auch kostenlose OpenSource-Software wie Moodle unterliegt Lizenzbedingungen, die zu bestätigen und zu akzeptieren sind.

![Image 81](index-138_1.jpg)

4.3 Installation von Moodle

**115**

**Bild 4.27** Eine wichtige Checkliste! Gibt es hier Fehlermeldungen, sollte die Einhaltung der Systemvoraussetzungen überprüft werden. Insbesondere gilt dies für die Verfügbarkeit der PHP- Erweiterungen.

Es folgt nun ein sehr wichtiger Abschnitt, bei dem im besten Fall nichts weiter zu tun ist, als Zeile für Zeile zu überprüfen. Gibt es an einer Stelle eine Fehlermeldung kann dies bedeuten, dass einzelne Moodle-Inhalte nicht funktionieren oder sogar die Darstellung des Systems im Webbrowser nicht über ein reines unformatiertes „HTML“ hinausreicht.

Ist einer der Installationsschritte nicht erfolgreich, müssen unter Umständen die PHP-Erweiterungen und deren Versionen überprüft werden. Oft genügt es, in der Datei _php.ini_ ein einfaches Semikolon zu entfernen.

![Image 82](index-139_1.jpg)

**116** 4 Moodle-Grundinstallation

**Bild 4.28** Abschließend noch ein wichtiger Schritt: Die Einrichtung des Hauptadministrators.

Die Zugangsdaten sollten unbedingt notiert werden!

Den letzten Installationsschritt stellt nun die Einrichtung des Moodle-Systemverwalters dar.

Dieser ist einzig für die Verwaltung des Moodle-Systems, die Kurse, die Benutzerberechti-gungen, Aktivierung von Plugins usw. zuständig. Der Moodle-Systemverwalter muss nicht zwangsweise auch Verwalter des Betriebssystems sein und ist dies in den meisten Fällen auch nicht. Das kann zu einem administrativen Problem werden, was nur durch eine gute Kommunikation gelöst werden kann.

Die Zugangsdaten sollten notiert und sicher verwahrt werden. Wird die Aufgabe auf eine andere Person delegiert, so sollte mit dem ersten Login dieses Moodle-Administrators aus Sicherheitsgründen die Wahl eines neuen Passworts erzwungen werden. Ebenso kann an dieser Stelle festgelegt werden, wie sich Lernende (Students) und Lehrende (Teacher) im System registrieren können. Dies kann sowohl durch den Administrator als auch persönlich mit Eingabe einer E-Mail- Adresse erfolgen. Letzteres hat den Vorteil, dem Moodle-Administrator Arbeit – in größeren Systemen in durchaus erheblichem Umfang – zu ersparen. Die erste Variante macht es Angreifern schwerer, das System zu überfluten.

Für die Registrierung im System und den Zugang zu Moodle werden durch Aktivierung von Plugins zu einem späteren Zeitpunkt noch weitere Optionen zur Verfügung stehen. Im Einzelfall müssen dafür jedoch die entsprechenden Umgebungsvoraussetzungen (SSO-Server etc.) mit der IT-Abteilung geklärt werden.

![Image 83](index-140_1.jpg)

![Image 84](index-140_2.jpg)

4.3 Installation von Moodle

**117**

**Bild 4.29** Für den Besucher der Moodle-Startseite sollte es eine kurze Beschreibung des Lehrangebots dieser Plattform und des Instituts geben. Unter Umständen kann auch eine kurze Information für die Anmeldung am System bereits hier deponiert werden.

**Bild 4.30** Soll eine Selbstanmeldung möglich sein oder dies nur der Systemverwaltung vorbehalten bleiben?

![Image 85](index-141_1.jpg)

**118** 4 Moodle-Grundinstallation

Sind all diese Schritte durchlaufen, dann ist die Installation einer absolut leeren Lernplattform abgeschlossen. „Absolut leer“ bedeutet:

Es gibt noch keine Lehrenden im System.

Es gibt noch keine Lernenden im System.

Es gibt noch keine Kurse.

Es gibt noch keine Lerninhalte, Aufgaben, Prüfungen usw.

Die eigentliche Arbeit mit Moodle beginnt also erst jetzt und bedarf noch einiger administrativer Vorbereitung innerhalb des nun bestehenden Systems. Möglicherweise möchte eine Schule, eine Hochschule oder ein Unternehmen die Lernplattform auch optisch etwas individueller gestalten? Dann sind die verschiedenen Designoptionen interessant. Funktionell kann Moodle über den bereits mit der Grundinstallation recht beachtlichen Umfang durch die Installation von Plugins noch sinnvoll erweitert werden. Doch hier gilt es aufzupassen, denn die Entwickler der Plugins müssen nicht unbedingt dem Moodle-Projekt angehören und es ist nicht garantiert, dass ein möglicherweise sehr nützliches und beliebtes Plugin in einer neuen Version noch funktionieren kann.

Die gute Nachricht: In den weiteren Kapiteln wird die Ebene der Betriebssysteme und der Serverumgebung weitgehend verlassen.

**Bild 4.31** Die Installation ist geschafft! Die Moodle-Oberfläche ist natürlich noch leer.

4.4 Plugins für Moodle

**119**

**■**

**■ 4.4■Plugins für Moodle**

Das Lernmanagementsystem Moodle bietet bereits mit seiner Grundinstallation sehr vielseitige Möglichkeiten, um Kurse zu gestalten und um Lernzielkontrollen durchzuführen.

Darüber hinaus gibt es jedoch eine Vielzahl nützlicher Erweiterungen für Moodle. Hier kann es sich beispielsweise um moderne Erscheinungsbilder – sogenannte _Themes_ – handeln. Es gibt administrative Plugins wie Terminplaner oder automatische Wartelisten für überbuchte Kurse. Zudem ist das Thema Plagiatserkennung immer wichtiger in der Beurteilung von Aufgaben geworden. Auch hier gibt es mittlerweile Plugins, die eine Unterstützung anbieten.

Sehr interessant für die motivierende Gestaltung von Kursen ist die Möglichkeit, Feedbacks einzufordern. Auch Lernspiele haben einen meist sehr einfachen, aber für kurze Übungs-phasen nutzbringenden Charakter. Sogar sehr komplexe Prüfungen sind mit Moodle möglich. All dies ist natürlich nur dann wirklich sinnvoll, wenn die erbrachten Leistungen der Lernenden auch tatsächlich übersichtlich für die jeweils zuständigen Lehrenden zusammengefasst werden können.

Weitere Plugins gibt es für die Kommunikation und die Zusammenarbeit innerhalb der Moodle-Plattform sowie für die inhaltliche Gestaltung. Natürlich ist die Zahl der verfügbaren Plugins sehr groß, sodass in den Kapiteln dieses Werks nur eine kleine Auswahl vorgestellt werden kann. An dieser Stelle soll vor allem die Suche nach dem richtigen Plugin und dessen Installation im Vordergrund stehen.

**4.4.1■Das richtige Moodle-Plugin**

Wie sucht man das richtige Plugin? Wird es tatsächlich benötigt oder erscheint es lediglich als „nice to have“? Die Frage sollte im Kollegenkreis gewissenhaft diskutiert werden, denn ein Moodle-Plugin ist möglicherweise mit zusätzlichem administrativem Aufwand verbunden und es kann – wenn es nicht zum Moodle-Standard gehört – nicht garantiert werden, dass es auch für künftige Moodle-Versionen weiterentwickelt wird! Das bedeutet wiederum, dass eine Fixierung auf ein bestimmtes Plugin möglicherweise sicherheitsrelevante Updates und Upgrades von Moodle verhindert.

Die Praxis zeigt bedauerlicherweise oft, dass Plugins im System eingerichtet, jedoch selten tatsächlich genutzt werden. Um die richtige Erweiterung für das Moodle-System zu finden, sei hier eine (selbstverständlich unverbindliche) Empfehlung gegeben.

**Zuerst das Standardpaket prüfen**

Werden tatsächlich Erweiterungen benötigt, weil der Leistungsumfang des

Standardpakets nicht ausreicht? Gibt es (gute und zuverlässig weiterent-

wickelte) Erweiterungen, die den Funktionen des Standardpakets überlegen sind? Ein Plugin sollte nur dann installiert werden, wenn dessen Bestand als nachhaltig gesichert angenommen werden kann. Ein späterer Verzicht auf

ein Plugin führt häufig zu Verstimmungen im Kreis der Lehrenden.

■

**120** 4 Moodle-Grundinstallation

**4.4.1.1■Bedarfskonferenz**

Was brauchen die Lehrenden? Was unterstützt deren Unterricht oder Training wirklich?

In einer Bedarfskonferenz sollte die Möglichkeit gegeben werden, ganz offen Wünsche zu formulieren. Dabei ist es noch nicht wirklich erforderlich, verbindliche Zusagen zu machen.

Es ist eher ein sinnvolles „Brainstorming“, welches es dem Systemverwalter erleichtert, passende Lösungen zu recherchieren. Konferenzen dieser Art steigern zudem die Akzeptanz der Lernumgebung.

Als Quintessenz einer solchen Konferenz kann eine „Wunschliste“ entstehen, anhand der zunächst verschiedene Erweiterungen ausgewählt, auf einem Testsystem installiert und in einem engen Kreis von Probanden getestet werden. Erst wenn sich eine Erweiterung tatsächlich bewährt hat, wird sie in das Produktivsystem aufgenommen.

**Empfehlung: ein Testsystem als Experimentierplattform**

Um der Kritik vorzugreifen: Ja, es sind zwei Installationen erforderlich! Ja, es braucht zwei unabhängige Bereiche auf dem Webserver und zwei eigene Datenbanken! Und ja, es ist zusätzlicher administrativer Aufwand erforderlich! Es können allerdings risikofrei nahezu alle erdenklichen Szenarien durchgespielt und ausprobiert werden. Dazu sollten die Lehrenden, die später mit den

Erweiterungen arbeiten werden, eingeladen und deren Meinung berücksichtigt werden. Ein Tipp: Ein Server, der in einer „virtuellen Maschine13“ wie zum Beispiel VirtualBox oder VMware läuft, lässt sich leicht auf einen definierten Anfangszustand zurücksetzen, wenn mit Kopien einer solchen virtuellen

Maschine gearbeitet wird.

■

**4.4.1.2■Recherchegrundlagen**

Bei der Suche nach einem geeigneten Plugin für das Moodle-System reicht es nicht aus, nur der Wunschliste der Lehrenden zu folgen. Aus technischer Betrachtungsweise ist es zunächst viel wichtiger, dass ein Plugin mit dem Moodle-System kompatibel ist und dass es auch auf dem Server reibungslos funktionieren kann. So kann es also vorkommen, dass ein Webserver durchaus die aktuellen Systemvoraussetzungen für Moodle erfüllt, jedoch das Plugin möglicherweise noch weitere PHP-Erweiterungen oder aktuellere Versionen von PHP und der Datenbank erfordert. In aller Regel können ältere Erweiterungen, die für Moodle-Versionen bis Moodle 1.9 entwickelt wurden, heute nicht mehr eingesetzt werden.

Dies liegt unter anderem an dem Entwicklungssprung bei der PHP-Plattform. Auch Erweiterungen für Moodle 2.x sollten zuerst in einer Experimentalumgebung getestet werden, bevor sie in das Live-System implementiert werden.

13 Eine virtuelle Maschine ist ein Computersystem, dessen Hardware lediglich simuliert wird. Es handelt sich also um eine Software, in der ein vollständiges Betriebssystem installiert wird, in dem auch vollwertige Programme laufen können. Virtualisierung ist tatsächlich eine Technik, die sogar für größere Systeme zum Einsatz kommt. Wichtig ist allerdings, unbedingt eine gut bemessene (physische) Hardwareplattform zu verwenden, die ausreichende Ressourcen für das Host- und das Gastsystem bietet. Eine virtuelle Maschine kann sehr einfach kopiert (geklont) werden und lässt sich im Fall einer Zerstörung schnell und unkompliziert wiederherstellen.

![Image 86](index-144_1.jpg)

4.4 Plugins für Moodle

**121**

Beginnen sollte die Recherche auf der offiziellen Seite des Moodle-Projekts. Hier wird ein _Moodle Plugin Directory_ 14 angeboten, das mehr als 1600 Erweiterungen enthält. Interessant dürften aber auch Erweiterungen sein, mit denen andere multimediale Lernsysteme in die Moodle-Plattform integriert werden können. Immer wichtiger werden zum Beispiel _virtuelle_ _Klassenzimmer_. Dabei handelt es sich um meist als eigenständige Plattformen konzipierte Kommunikationslösungen, die neben einem Textchat und einem Interactive Whiteboard auch die Möglichkeit der Audio- und Video-Konferenz bieten und es gestatten, Präsentationen vorzuführen. Diese virtuellen Klassenräume bzw. Konferenzlösungen laufen zumeist nicht auf einem eigenen Server! Oft sind sie auch kostenpflichtig. Allerdings können die Sitzungen mithilfe von Moodle direkt organisiert und der Zugang zur Sitzung direkt aus der Moodle-Session heraus initiiert werden. Neben den Kursinhalten des virtuellen Klassenzimmers können zusätzlich die Materialien aus der Moodle-Plattform verwendet werden.

**Mögliche Kostenpflicht beachten!**

Virtuelle Klassenräume gibt es auch zum „Nulltarif“, jedoch meist nur in sehr stark eingeschränkter Form mit einer geringen Zahl von Teilnehmerinnen und Teilnehmern. Sie sind darüber hinaus zumeist in der Nutzungsdauer stark

limitiert. Wird jedoch viel auf örtliche Unabhängigkeit in der Schulung Wert gelegt – insbesondere bei der internen Weiterbildung von Mitarbeitern ist dies interessant –, sind die Preise von wenigen Euro im Monat gegenüber

Aufwendungen für Arbeitsausfälle und Dienstreisen marginal.

■

**Bild 4.32** Über die offizielle Seite des Moodle-Projekts sind mehr als 1600 Erweiterungen verschiedener Kategorien zu finden. Darüber hinaus bieten freie Entwickler teilweise sehr interessante Plugins an.

14 Das Moodle Plugin Director[y _https://moodle.org/plugins/_ bie](https://moodle.org/plugins/)tet verschiedene Moodle-Erweiterungen zum Download an.

![Image 87](index-145_1.jpg)

**122** 4 Moodle-Grundinstallation

Plugins gibt es in verschiedenen Kategorien:

Verwaltung (Administration)

Bewertung, Beurteilung (Assessment)

Zusammenarbeit (Collaboration)

Kommunikation (Communication)

Inhalt (Content)

Schnittstellen (Interface)

**4.4.2■Installation eines Plugins**

Nach der Auswahl eines Plugins sollte vor dem Download geprüft werden, ob es überhaupt für die installierte Moodle-Version geeignet ist. Auf der Webseite des Moodle-Projekts wird ausdrücklich darauf hingewiesen, dass Plugins nicht zwingend getestet wurden. Wer zunächst in einer Testumgebung arbeitet, kann (und sollte) dort experimentieren. In einer Produktivumgebung wird stets empfohlen, den sicheren Weg zu wählen. Ein Test kann aber durchaus auch positive Ergebnisse zeigen und eine nicht explizit für die bestehende Moodle- Version bezeichnete Erweiterungen als einsetzbar entlarven.

**Die „goldene Regel“**

Vor jeder Systemänderung oder -erweiterung gehört es sich, ein vollständiges Backup, also eine Sicherheitskopie des Moodle-Datenverzeichnisses und der Moodle-Datenbank anzufertigen!

■

**Bild 4.33** Die Erweiterungen müssen zur installierten Moodle-Version passen. Sonst können weit-reichende Funktionsstörungen die Folge sein.

![Image 88](index-146_1.jpg)

4.4 Plugins für Moodle

**123**

**Bild 4.34** Die Installation des Plugins beginnt im Bereich „Website-Administration“ mit den Rechten eines Moodle-Administrators.

Hat man die gewünschte Erweiterung heruntergeladen, kann sie in das Moodle-System installiert werden. Das funktioniert durch Hochladen des ZIP-Archivs über einen sehr einfachen Dialog der Moodle- _Website-Administration_. Natürlich ist dieser Bereich von Moodle nicht für jede Benutzerin bzw. jeden Benutzer zugänglich. Moodle legt eine sehr klare Hierarchie im System fest, nach der Rechte und Nutzungseinschränkungen festgelegt werden können. Diese _Rollen im Moodle-System_ werden im folgenden Kapitel vorgestellt.

Nach dem Upload überprüft Moodle das Installationspaket auf Fehler. Werden keine gefunden, erfolgt eine weitere Überprüfung, ob gegebenenfalls Aktualisierungen vorhanden sind.

Diese können per Mausklick gesucht werden. Eine grün hinterlegte Meldung signalisiert letztlich die erfolgreiche Installation. Wird diese Meldung nicht angezeigt, so sind folgende Prüfungen durchzuführen:

Hat der Webserver die erforderlichen Schreibrechte im System?

Ist das Plugin für die installierte Moodle-Version geeignet?

Passen die PHP-Versionen und die PHP-Erweiterungen zu den Systemanforderungen des Plugins?

Entspricht die Datenbank den Systemanforderungen des Systems?

![Image 89](index-147_1.png)

![Image 90](index-147_2.jpg)

**124** 4 Moodle-Grundinstallation

**Bild 4.35** Mithilfe eines solchen einfachen Upload-Dialogs, wie er in anderen Bereichen auch von _Teachern_ zum Hochladen von Lehrmaterialien und von _Students_ zur Abgabe ihrer Arbeiten genutzt wird, lässt sich das neue Plugin in das System einspielen.

**Bild 4.36** Nach dem Upload des ZIP-Archivs mit den Installationsdateien des neuen Plugins wird der Installationsvorgang in der Website-Administration von Moodle mit einem Mausklick gestartet.

![Image 91](index-148_1.jpg)

![Image 92](index-148_2.jpg)

![Image 93](index-148_3.jpg)

4.4 Plugins für Moodle

**125**

**Bild 4.37** Zunächst wird das Installationsskript auf Fehler überprüft. Auch fehlende Schreibrechte im Webserver, die für die Installation des Plugins nötig sind, werden an dieser Stelle immer wieder geprüft.

**Bild 4.38** Stimmen die Versionen? Gibt es aktualisierte Pakete? Dieser Dialog lässt eine Prüfung zu.

**Bild 4.39** Es ist geschafft! Das erste Plugin wurde soeben im eigenen Moodle-System installiert.

![Image 94](index-149_1.jpg)

**126** 4 Moodle-Grundinstallation

Mit der Zeit werden zahlreiche Erweiterungen im System installiert sein, die neben den mehr als 400 Plugins der Standardinstallation existieren. Um diese zu verwalten, ruft der Moodle-Administrator erneut die Website-Administration auf und wählt im Bereich _Plugins_ die _Plugin-Übersicht_. Diese ist in zwei Bereiche gegliedert:

Eine gesamte Übersicht (alle Plugins) listet alle bereits installierten Plugins auf. Über eine Schaltfläche _Einstellungen_ können diese bereits in der Übersicht bearbeitet werden. In einer eigenen Rubrik werden lediglich die zusätzlich neben dem Standardumfang installierten Erweiterungen aufgelistet, was die Übersicht ver bessert und die individuelle Administration erleichtert.

**Bild 4.40** Im Moodle-System gehören bereits über 400 Plugins zum Stammumfang! Die soeben installierte Erweiterung ist nicht nur in der Gesamtliste, sondern darüber hinaus im Register „Zusätzliche Plugins“ zu finden.

![Image 95](index-150_1.jpg)
