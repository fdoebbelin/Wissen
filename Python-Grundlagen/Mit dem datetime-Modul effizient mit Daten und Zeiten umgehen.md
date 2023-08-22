---
source: https://www.heise.de/hintergrund/Python-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen-9252303.html?seite=all
---

Mit dem eingebauten datetime-Modul in Python werden Sie zum Meister der Zeit und formatieren Daten oder berechnen Zeitabstände.

Lesezeit: 13 Min.

[In Pocket speichern](https://getpocket.com/save?url=https%3A%2F%2Fwww.heise.de%2Fhintergrund%2FPython-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen-9252303.html)

[vorlesen](https://app-eu.readspeaker.com/cgi-bin/rsent?customerid=4407&lang=de_de&readid=meldung&url=https%3A%2F%2Fwww.heise.de%2Fhintergrund%2FPython-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen-9252303.html%3Fseite%3Dall "Beitrag vorlesen und MP3-Download")[](https://www.heise.de/hintergrund/Python-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen-9252303.html?view=print)

[Druckansicht](https://www.heise.de/hintergrund/Python-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen-9252303.html?view=print) [Kommentare lesen](https://www.heise.de/forum/heise-online/Kommentare/Python-Grundlagen-Mit-dem-datetime-Modul-effizient-mit-Daten-und-Zeiten-umgehen/forum-524616/comment/)

![](https://heise.cloudimg.io/width/610/q85.png-lossy-85.webp-lossy-85.foil1/_www-heise-de_/imgs/18/4/2/8/7/7/8/9/teamplus_flat_vector_computer_code_representing_clocks_blue_and_0f1f7f50-774d-4b67-a605-d0297cf48c2c-887a56f1ceee1610.png)

Erstellt mit Midjourney durch heise online.

17.08.2023 17:37 Uhr

Von

- [Marvin Strathmann](https://www.heise.de/autor/Marvin-Strathmann-3629555)

Anzeige

Irgendwann muss man in Python mit Daten und Zeiten arbeiten. Sei es, um eine Zeitspanne zwischen zwei Daten zu berechnen, Uhrzeiten in ein verständliches Format zu bekommen oder Zeitzonen in verschiedenen Ländern zu berücksichtigen. Diese Aufgaben können komplex sein, da sie sowohl ein Verständnis für Zeitkonzepte als auch für die spezifischen Funktionen und Methoden in Python erfordern.

Zum Glück enthält Python das Modul datetime, das eine Vielzahl von Funktionen zur Arbeit mit Daten und Zeiten bereitstellt. Wir erklären die Grundlagen und zeigen, wie damit auch Anfänger das aktuelle Datum abrufen, die Tage bis zum Geburtstag berechnen oder verschiedene Zeiten miteinander vergleichen können. Wir gehen auch darauf ein, wie man datetime verwendet, um Daten und Zeiten zu formatieren und zu parsen, was besonders nützlich ist, wenn man mit Benutzereingaben oder externen Datenquellen arbeitet.

Zudem zeigen wir, wie datetime mit Zeitzonen umgeht. Die Behandlung von Zeitzonen kann eine Herausforderung sein, da je nach Land verschiedene Regeln für Sommerzeit und Winterzeit gelten. Mit datetime kann der Nutzer Zeitzonen erstellen und Daten zwischen Zeitzonen umwandeln. Schließlich erklären wir noch, wie die externe Bibliothek dateutil den Umgang mit verschiedenen Zonen erleichtert.

### Zeitprobleme

Bei der Arbeit mit Daten und Zeiten gibt es viel zu beachten. Entwickelt man etwa eine App, die für Nutzer auf der ganzen Welt gedacht ist, kommen plötzlich unterschiedliche Zeitzonen ins Spiel. Der App-Nutzer in New York fügt einen Termin für 15 Uhr hinzu. Aber was bedeutet das für einen Benutzer in Berlin? Ist die App schlecht programmiert, dann könnte der Berliner eine Benachrichtigung für den Termin um 15 Uhr Berliner Zeit erhalten – das wäre 9 Uhr morgens in New York.

Man muss nicht mal an einer internationalen App arbeiten. Auch die lokale Sommerzeit ist ein Problem: Die genauen Daten, an denen man die Uhren umstellt, variieren von Land zu Land und ändern sich manchmal von Jahr zu Jahr. Dies kann dazu führen, dass eine Stunde verloren geht oder gewonnen wird. Will man nun etwa Zeiten berechnen und Ereignisse planen, die genau während einer Zeitumstellung stattfinden, können Fehler passieren.

Dass Länder unterschiedlich sind, führt zu weiteren Herausforderungen: Manche Staaten verwenden das Zeitformat DD-MM-YYYY, andere MM-DD-YYYY. Dann nutzen verschiedene Länder Zeitangaben mit einer 12-Stunden-Uhr, anderer verwenden wiederum die 24-Stunden-Uhr. In manchen Staaten beginnt die Woche an einem Sonntag, in anderen an einem Montag – wer etwa den Wochentag berechnen will, kann da schnell verzweifeln.

Zusätzlich muss der Programmierer Schaltjahre berücksichtigen: Alle vier Jahre hat der Februar 29 Tage, das gesamte Jahr 366 statt 365 Tage. Und hat man dann die Zeitzone, die Sommerzeit, das Format, den Wochenbeginn, die Schaltjahre, einfach alles, in Betracht gezogen, dann können sich plötzlich Sommerzeiten oder ganze Zeitzonen einfach ändern – sie sind ja keine fixen Konstanten.

Kurz: Zeiten sind kompliziert. Und bevor man Berechnungen mit Zeiten und Daten durchführt, ist es eher sinnvoll, eine Bibliothek oder ein Modul zu verwenden, das speziell für die Arbeit mit Daten und Zeiten gedacht ist. Und genau dafür gibt es das datetime-Modul in Python.

### datetime

Das datetime-Modul ist ein eingebautes Modul in Python, das Klassen bereitstellt, um Daten und Zeiten zu bearbeiten. Mit dem datetime-Modul lassen sich einfache und komplexe Operationen mit Daten und Zeiten durchführen, etwa Zeiteinheiten hinzufügen oder subtrahieren, Daten und Zeiten in verschiedene Formate konvertieren und vieles mehr.

datetime muss man nicht installieren, sondern im Python-Code nur importieren und kann dann schon mit den Klassen arbeiten:

```
import datetime
```

### Hello World

Das datetime-Modul enthält mehrere Klassen, darunter `date`, `time`, `datetime`, `timedelta` und `timezone`. Die Klasse `date` repräsentiert ein Datum mit den Angaben für Jahr, Monat und Tag.

Als erste Hello-World-Aufgabe könnte man sich etwa das heutige Datum ausgeben lassen. Das geht mit `date` ganz einfach:

```
from datetime import date

aktuellesDatum = date.today()

print(aktuellesDatum)
```

Erst importiert der Nutzer `date` aus der datetime-Bibliothek. Mit `date.today()` lässt sich dann das aktuelle Datum abrufen. In diesem Beispiel packen wir es erst in die Variable `aktuellesDatum` und geben dann die Variable mit dem `print()`-Befehl in der Konsole aus. Das Datum erscheint im Format YYYY-MM-DD in der Konsole, also etwa `2023-10-15`.

Über die Attribute lassen sich einzelne Informationen aus dem Datumsobjekt ziehen:

```
from datetime import date

aktuellesDatum = date.today()

print(aktuellesDatum)
print(aktuellesDatum.year)
print(aktuellesDatum.month)
print(aktuellesDatum.day)
```

Mit diesem Code steht nicht nur das aktuelle Datum in der Konsole. Mit `.year` hinter der Variable gibts nur das Jahr, `.month` zeigt lediglich den Monat und `.day` den Tag.

### Arbeiten mit Daten

Ein `date`-Objekt lässt sich recht einfach mit der `date()`-Funktion erstellen:

```
from datetime import date

datum = date(2023, 10, 15)
```

Die Funktion nimmt als ersten Parameter das Jahr an, dann den gewünschten Monat und schließlich den Tag. Mehrere Date-Objekte lassen sich mit den Standardoperatoren von Python vergleichen, also mit `<`, `>`, `<=`, `>=`, `==` und `!=`. Dafür erstellen wir zwei Daten:

```
from datetime import date

datum1 = date(2023, 8, 17)
datum2 = date(2023, 8, 18)

print(datum1 < datum2)
```

In diesem Beispiel würde der Code `true` ergeben, da `datum1` (17. August 2023) vor `datum2` (18. August 2023) liegt – `datum1` ist also kleiner.

Es folgt etwas Datumsmathe. Denn man kann die Differenzen zwischen zwei Daten berechnen:

```
from datetime import date

datum1 = date(2023, 8, 17)
datum2 = date(2023, 8, 18)

delta = datum2 - datum1

print(delta.days)
```

Hier ziehen wir `datum1` von `datum2` ab. Die Differenz daraus ergibt ein `timedelta`-Objekt. So ein Objekt repräsentiert kein Datum, sondern eine Zeitdauer. Mit dem Attribut `.days` am Ende des `timedelta`-Objekts landet die Anzahl der Tage in der Konsole, also eine schlichte `1` – zwischen den beiden Daten liegt nur ein Tag Unterschied.

Der Nutzer kann zudem beliebig viele Tage zu einem bestimmten Datum addieren oder von einem Datum subtrahieren. Dafür benötigen wir aber vorab ein `timedelta`-Objekt. Die Klasse dafür müssen wir erst importieren:

```
from datetime import date, timedelta

datum = date(2023, 8, 17)

datum_plus_eins = datum + timedelta(days=1)

print(datum_plus_eins)
```

Mit `datum = date(2023, 8, 17)` lässt sich schnell ein Datum anlegen. Für die Variable `datum_plus_eins` addiert man dann zu dem Datum das `timedelta`-Objekt `timedelta(days=1)` – also einen Tag. Das Programm schreibt schließlich `2023-08-18` in die Konsole.

### Happy Birthday!

Wie lassen sich all diese Funktionen praktisch verwenden? Der Nutzer könnte etwa ein kleines Programm schreiben, das die Tage bis zu seinem nächsten Geburtstag berechnet.

Dafür importiert man wie vorher `date` aus datetime, lässt sich das heutige Datum berechnen und gibt seinen Geburtstag ein:

```
from datetime import date

heute = date.today()
geburtstag = date(1989, 12, 29)
```

Für den nächsten Geburtstag benötigt man dann das Jahr von heute sowie den Monat und den Tag des Geburtstags:

```
naechster_geburtstag = date(heute.year, geburtstag.month, geburtstag.day)
```

Aber was, wenn der nächste Geburtstag erst nächstes Jahr ist? Dafür schreiben wir eine kleine `if`-Abfrage, die prüft, ob heute größer als der nächste Geburtstag ist – also ob der Geburtstag in diesem Jahr schon rum ist:

```
if heute > naechster_geburtstag:
    naechster_geburtstag = date(heute.year + 1, geburtstag.month, geburtstag.day)
```

Wenn das der Fall ist, dann muss man nur zu `heute.year` eine 1 hinzufügen, also ein Jahr zum aktuellen Datum addieren. Der Rest ist simpel: Man zieht `heute` vom nächsten Geburtstag ab und erhält so ein `timedelta`-Objekt für die übrigen Tage: `verbleibende_tage = naechster_geburtstag - heute`. Anschließend gibt man die Anzahl der Tage mit `verbleibende_tage.days` in der Konsole aus:

```
print(f"Heute ist der {heute}, und es sind noch {verbleibende_tage.days} Tage bis zu Ihrem nächsten Geburtstag!")
```

Das komplette Programm sieht so aus:

```
from datetime import date

heute = date.today()
geburtstag = date(1989, 12, 29)

naechster_geburtstag = date(heute.year, geburtstag.month, geburtstag.day)

if heute > naechster_geburtstag:
    naechster_geburtstag = date(heute.year + 1, geburtstag.month, geburtstag.day)

verbleibende_tage = naechster_geburtstag - heute

print(f"Heute ist der {heute}, und es sind noch {verbleibende_tage.days} Tage bis zu Ihrem nächsten Geburtstag!")
```

### Uhrzeiten

Manchmal reicht ein Datum nicht aus und es muss etwas genauer ein – etwa bei Terminen. Dafür bietet `datetime` die Klasse `time`. Ein `time`-Objekt repräsentiert eine bestimmte Uhrzeit, unabhängig von einem bestimmten Tag. Der Import ist wieder denkbar einfach und erfolgt mit einem `from datetime import time`.

Analog wie bei `date` mit Jahren, Monaten und Tagen erstellt man ein `time`-Objekt, indem man die Stunde, Minute und Sekunde als Parameter an den Konstruktor der `time`-Klasse übergibt:

```
from datetime import time

zeit = time(13, 45, 30)

print(zeit)
```

Der erste Parameter ist die Stunde, der zweite die Minute und der dritte die Sekunde. Als Ausgabe erhält der Nutzer also die Uhrzeit 13:45:30. Mit `time` lassen sich ähnliche Dinge anstellen wie mit `date`. Uhrzeiten lassen sich etwa mit den üblichen Operatoren miteinander vergleichen. Über Attribute kann der Nutzer auch wieder die einzelnen Bestandteile des Objekts abrufen:

```
from datetime import time

zeit = time(13, 45, 30)

print(zeit.hour)
print(zeit.minute)
print(zeit.second)
```

Hier erscheint nacheinander `13`, `45` und dann `30` in der Konsole.

### Datum und Uhrzeiten zusammen

Die Kombination aus `date` und `time` bildet das `datetime`-Objekt. Es lässt sich etwa mit Jahr, Monat, Tag, Stunde, Minute und Sekunde erstellen:

```
from datetime import datetime

dt = datetime(2023, 8, 17, 14, 30)

print(dt)
```

Als Ausgabe landet hier `2023-08-17 14:30:00` in der Konsole.

Während `date.today()` sich ja das aktuelle Datum zieht, kann der Nutzer mit `datetime.now()` das aktuelle Datum und die Uhrzeit abrufen. Wie bei `date` und `time` lassen sich über Attribute wie `.year`, `.day` oder `.minute` die einzelnen Bestandteile des `datetime`-Objekts nutzen. Zudem kann man die Objekte vergleichen und Differenzen bilden.

### Daten formatieren

Eine immer wiederkehrende Aufgabe beim Arbeiten mit Daten ist das Formatieren. Schließlich will man nicht immer das Datum im Format YYYY-MM-DD HH:MM:SS ausgeben. Dafür gibt in der Bibliothek `datetime` die Methode `strftime()`:

```
from datetime import datetime

dt = datetime(2023, 8, 17, 14, 30)
dt_formatiert = dt.strftime("%Y.%m.%d %H:%M:%S")

print(dt_formatiert)
```

Dieser Code würde etwa `2023.08.17 14:30:00` ausgeben statt `2023-08-17 14:30:00` ohne die Formatierung.

Wichtig sind dabei die Formatcodes, die der Nutzer als Parameter übergibt. `%Y` gibt etwa das Jahr mit vier Ziffern aus, `%y` das Jahr mit nur zwei Ziffern. `%B` steht für den vollständigen Namen des Monats, `%A` zeigt den vollständigen Namen des Wochentags. [Eine komplette Liste mit allen Formatcodes findet man im Netz](https://strftime.org/).

Diese Formatcodes, eingeleitet mit dem Prozentzeichen, lassen sich mit normalen Zeichen kombinieren. `dt.strftime("Es ist %H:%M Uhr am %d. %B %Y.")` würde ergeben: `Es ist 14:30 Uhr am 17. August 2023.` ergeben

`dt.strftime("Es ist der %j. Tag des Jahres und es ist %A.")` schreibt in die Konsole: `Es ist der 229. Tag des Jahres und es ist Donnerstag.`

### Strings umwandeln

Oft möchte man Strings, die etwa ein Nutzer des Programms eingibt, in ein Datumsobjekt umwandeln. Dafür liefert datetime die Methode `strptime()`. Sie verlangt als Parameter erst den String und dann das zugehörige Format.

Nehmen wir an, der Nutzer tippt "2023.08.17 14:30" ein. Den String speichert man erst in einer Variable: `dt_string = "2023.08.17 14:30"`. Nun wandeln wir ihn in ein `datetime`-Objekt um: `dt = datetime.strptime(dt_string, "%Y.%m.%d %H:%M")`. Man bildet quasi den kompletten Input nach und nutzt dafür die Formatcodes, die auch bei `strftime()` zum Einsatz kommen.

Damit lässt sich jeder beliebige String umwandeln – egal in welchem Format er daherkommt:

```
from datetime import datetime

dt_string = "Datum: 17/08/2023, Uhrzeit: 14:30:45"
dt = datetime.strptime(dt_string, "Datum: %d/%m/%Y, Uhrzeit: %H:%M:%S")

print(dt)
```

Hier erhält man `2023-08-17 14:30:45` in der Ausgabe. Zusammen mit `strptime()` kann man einen beliebigen String in ein Datum verwandeln und dann mit `strftime()` im gewünschten Format wieder ausgeben:

```
dt_string = "2023-08-17 14:30:45"

dt = datetime.strptime(dt_string, "%Y-%m-%d %H:%M:%S")
print(f"Umgewandelt von String zu datetime: {dt}")

formatted_dt = dt.strftime("Datum: %d/%m/%Y, Uhrzeit: %H:%M:%S")
print(f"Umgewandelt von datetime zu String: {formatted_dt}")
```

### Zeitzonen

Wer länderübergreifend arbeitet, benötigt die Klasse `timezone` aus der datetime-Bibliothek. Damit ist es etwa möglich, `timezone`-Objekte zu erstellen:

```
from datetime import timedelta, timezone

tz = timezone(timedelta(hours=2))

print(tz)
```

Über `timedelta` fügt man hier zwei Stunden zur UTC-Zeit hinzu. Die Coordinated Universal Time ist der Zeitstandard, anhand dessen die Länder der Welt Uhren und Zeiten regulieren. Alle Zeitzonen sind durch ihre Verschiebung von UTC definiert. Diese Verschiebung wird als UTC- oder UTC+ und die Anzahl der Stunden und Minuten ausgedrückt – die Ausgabe im Beispiel ist daher `UTC+02:00`. UTC+2 ist die Osteuropäische Normalzeit und gilt etwa in Rumänien, Griechenland oder in Simbabwe.

Hat man eine Zeitzone erstellt, kann man sie auf ein `datetime`-Objekt anwenden:

```
from datetime import datetime, timedelta, timezone

tz = timezone(timedelta(hours=2))
dt = datetime(2023, 8, 17, 14, 30, tzinfo=tz)

print(dt)
```

Dafür nutzt man beim Erstellen den Parameter `tzinfo` und füllt ihn mit der eben erstellten Zeitzone.

Das funktioniert zwar, ist allerdings noch etwas umständlich. Wie zuvor erwähnt: Zeitzonen sind kompliziert, da möchte man nicht per Hand was zur UTC hinzufügen. Hier hilft die externe Bibliothek dateutil. Sie ist nicht Teil der Standardbibliothek von Python, lässt sich aber leicht mit pip installieren:

```
pip install python-dateutil
```

Der Import lautet dann aber nicht `import python-dateutil`, sondern schlicht `import dateutil`.

So lässt sich etwa die lokale Zeitzone bestimmen und auf ein `datetime`-Objekt anwenden:

```
from datetime import datetime
from dateutil import tz

local_tz = tz.tzlocal()

dt = datetime(2023, 8, 17, 14, 30, tzinfo=local_tz)

print(dt)
```

Wichtig ist hier, die lokale Systemzeitzone mit `tz.tzlocal()` abzurufen. Anschließend kann man sie wie vorhin mit `tzinfo` auf ein `datetime`-Objekt anwenden.

Praktisch: Mit einem `print(dt.tzname())` kann man direkt den Namen der Zeitzone abrufen, damit auch normale Menschen sie verstehen.

### Ausblick

Mit Daten und Zeiten zu arbeiten, kann zunächst kompliziert wirken. Wer aber die Funktionen der datetime-Bibliothek nutzt und ihre Syntax versteht, der wird bald zum Meister der Zeit in Python.

[Die Dokumentation listet alle Funktionen der Bibliothek auf](https://docs.python.org/3/library/datetime.html) und bietet nützliche Codebeispiele. Die externe Bibliothek dateutil kann noch sehr viel mehr, als wir in diesem Artikel beschrieben haben. [Auch hier lohnt sich ein Blick in die Dokumentation](https://dateutil.readthedocs.io/en/stable/#), um den Umgang mit Daten und Zeitzonen zu vereinfachen. ([str](mailto:str@heise.de "Marvin Strathmann"))