### Einführung

SSH oder Secure Shell ist ein verschlüsseltes Protokoll zur Verwaltung von und Kommunikation mit Servern. Wenn Sie mit einem Ubuntu-Server arbeiten, verbringen Sie wahrscheinlich die meiste Zeit in einer Terminalsitzung, die über SSH mit Ihrem Server verbunden ist.

In dieser Anleitung geht es um die Einrichtung von SSH-Schlüsseln für eine Ubuntu 20.04 Installation. SSH-Schlüssel bieten eine einfache und sichere Möglichkeit, sich bei Ihrem Server anzumelden. Sie werden allen Benutzern empfohlen.

## Schritt 1 — Erstellen des Schlüsselpaars

Der erste Schritt besteht darin, ein Schlüsselpaar auf dem Client-Computer (normalerweise Ihrem Computer) zu erstellen:

Standardmäßig erstellen die neuesten Versionen von `ssh-keygen` ein 3072-Bit-RSA-Schlüsselpaar, das für die meisten Anwendungsfälle sicher genug ist. (Optional können Sie über Flag `-b 4096` einen größeren 4096-Bit-Schlüssel erstellen lassen.)

Nach Eingabe des Befehls sollte die folgende Ausgabe angezeigt werden:

```
Output

Generating public/private rsa key pair.
Enter file in which to save the key (/==your_home==/.ssh/id_rsa): 
```

Drücken Sie die Eingabetaste, um das Schlüsselpaar im Unterverzeichnis `.ssh/` in Ihrem Stammverzeichnis zu speichern, oder geben Sie einen alternativen Pfad an.

Wenn Sie zuvor ein SSH-Schlüsselpaar erstellt haben, wird möglicherweise die folgende Eingabeaufforderung angezeigt:

```
Output

/home/==your_home==/.ssh/id_rsa already exists.
Overwrite (y/n)? 
```

Wenn Sie den Schlüssel auf der Festplatte überschreiben, können Sie sich **nicht** mehr mit dem vorherigen Schlüssel authentifizieren. Seien Sie sehr vorsichtig bei der Auswahl von „Ja“, da dies ein destruktiver Prozess ist, der nicht rückgängig gemacht werden kann.

Sie sollten dann die folgende Eingabeaufforderung sehen:

```
Output

Enter passphrase (empty for no passphrase): 
```

Hier können Sie optional eine sichere Passphrase eingeben, die dringend empfohlen wird. Mit einer Passphrase wird eine zusätzliche Sicherheitsebene hinzugefügt, um zu verhindern, dass sich nicht autorisierte Benutzer anmelden. Weitere Informationen zur Sicherheit finden Sie in unserem Tutorial unter [Konfiguration einer auf SSH-Schlüsseln basierten Authentifizierung auf einem Linux-Server](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server).

Sie sollten dann eine Ausgabe ungefähr wie folgt sehen:

```
Output

Your identification has been saved in /==your_home==/.ssh/id_rsa
Your public key has been saved in /==your_home==/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:/hk7MJ5n5aiqdfTVUZr+2Qt+qCiS7BIm5Iv0dxrc3ks user@host
The key's randomart image is:
+---[RSA 3072]----+
|                .|
|               + |
|              +  |
| .           o . |
|o       S   . o  |
| + o. .oo. ..  .o|
|o = oooooEo+ ...o|
|.. o *o+=.*+o....|
|    =+=ooB=o.... |
+----[SHA256]-----+ 
```

Sie haben jetzt einen öffentlichen und privaten Schlüssel, die Sie zur Authentifizierung verwenden können. Der nächste Schritt besteht darin, den öffentlichen Schlüssel auf Ihrem Server abzulegen, damit Sie sich mithilfe der SSH-Schlüsselauthentifizierung anmelden können.

## Schritt 2 – Kopieren des öffentlichen Schlüssels auf Ihren Ubuntu-Server

Die schnellste Möglichkeit, Ihren öffentlichen Schlüssel auf den Ubuntu-Host zu kopieren, ist die Verwendung eines Dienstprogramms namens `ssh-copy-id`. Aufgrund der Einfachheit wird diese Methode dringend empfohlen, falls sie verfügbar ist. Wenn Sie auf Ihrem Client-Computer nicht über `ssh-copy-id` verfügen, können Sie eine der beiden in diesem Abschnitt beschriebenen alternativen Methoden verwenden (Kopieren über passwortbasiertes SSH oder manuelles Kopieren des Schlüssels).

### Kopieren des öffentlichen Schlüssels mit `ssh-copy-id`

Das Tool `ssh-copy-id` ist in vielen Betriebssystemen standardmäßig enthalten, sodass es möglicherweise auf Ihrem lokalen System zur Verfügung steht. Damit diese Methode funktioniert, müssen Sie bereits über einen passwortbasierten SSH-Zugriff auf Ihren Server verfügen.

Um dieses Dienstprogramm zu verwenden, müssen Sie nur den Remote-Host, zu dem Sie eine Verbindung herstellen möchten, und das Benutzerkonto angeben, zu dem Sie einen passwortbasierten SSH-Zugang haben. Auf dieses Konto wird Ihr öffentlicher SSH-Schlüssel kopiert.

Die Syntax lautet:

Möglicherweise wird die folgende Meldung angezeigt:

```
Output

The authenticity of host '==203.0.113.1== (==203.0.113.1==)' can't be established.
ECDSA key fingerprint is fd:fd:d4:f9:77:fe:73:84:e1:55:00:ad:d6:6d:22:fe.
Are you sure you want to continue connecting (yes/no)? ==yes== 
```

Das bedeutet, dass Ihr lokaler Computer den Remote-Host nicht erkennt. Dies geschieht, wenn Sie zum ersten Mal eine Verbindung zu einem neuen Host herstellen. Geben Sie „yes“ ein und drücken Sie `ENTER`, um fortzufahren.

Als nächstes durchsucht das Dienstprogramm Ihr lokales Konto nach dem Schlüssel `id_rsa.pub`, den wir zuvor erstellt haben. Wenn der Schlüssel gefunden wurde, werden Sie zur Eingabe des Passworts für das Konto des Remotebenutzers aufgefordert:

```
Output

/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
==username==@==203.0.113.1=='s password: 
```

Geben Sie das Passwort ein (Ihre Eingabe wird aus Sicherheitsgründen nicht angezeigt) und drücken Sie `ENTER`. Das Dienstprogramm stellt mit dem von Ihnen angegebenen Passwort eine Verbindung zum Konto auf dem Remote-Host her. Anschließend wird der Inhalt Ihres Schlüssels `~/.ssh/id_rsa.pub` in eine Datei im Stammverzeichnis `~/.ssh` des Remote-Kontos namens `authorized_keys` kopiert.

Sie sollten die folgende Ausgabe sehen:

```
Output

Number of key(s) added: 1

Now try logging into the machine, with:   "ssh '==username==@==203.0.113.1=='"
and check to make sure that only the key(s) you wanted were added. 
```

Zu diesem Zeitpunkt wurde Ihr Schlüssel `id_rsa.pub` in das Remote-Konto hochgeladen. Sie können mit [Schritt 3](#step-3-%E2%80%94-authenticating-to-your-ubuntu-server-using-ssh-keys) fortfahren.

### Kopieren des öffentlichen Schlüssels mit SSH

Wenn Sie nicht über `ssh-copy-id` verfügen, aber einen passwortbasierten SSH-Zugriff auf ein Konto auf Ihrem Server haben, können Sie Ihre Schlüssel mit einer herkömmlichen SSH-Methode hochladen.

Wir können dazu den Befehl `cat` verwenden, um den Inhalt des öffentlichen SSH-Schlüssels auf dem lokalen Computer zu lesen und über eine SSH-Verbindung zum Remote-Server weiterzuleiten.

Auf der anderen Seite können wir sicherstellen, dass das Verzeichnis `~/.ssh` existiert und die richtigen Berechtigungen für das von uns verwendete Konto besitzt.

Wir können dann den Inhalt, den wir übergeben haben, in eine Datei namens `authorized_keys` in diesem Verzeichnis ausgeben. Wir verwenden das Umleitungssymbol `>>`, um den Inhalt anzuhängen, anstatt ihn zu überschreiben. Dadurch können wir Schlüssel hinzufügen, ohne zuvor hinzugefügte Schlüssel zu zerstören.

Der vollständige Befehl sieht wie folgt aus:

Möglicherweise wird die folgende Meldung angezeigt:

```
Output

The authenticity of host '==203.0.113.1== (==203.0.113.1==)' can't be established.
ECDSA key fingerprint is fd:fd:d4:f9:77:fe:73:84:e1:55:00:ad:d6:6d:22:fe.
Are you sure you want to continue connecting (yes/no)? ==yes== 
```

Das bedeutet, dass Ihr lokaler Computer den Remote-Host nicht erkennt. Dies geschieht, wenn Sie zum ersten Mal eine Verbindung zu einem neuen Host herstellen. Geben Sie `yes` ein und drücken Sie `ENTER`, um fortzufahren.

Anschließend sollten Sie aufgefordert werden, das Passwort für das Remote-Benutzerkonto einzugeben:

```
Output

==username==@==203.0.113.1=='s password: 
```

Nach Eingabe Ihres Passworts wird der Inhalt Ihres Schlüssels `id_rsa.pub` an das Ende der Datei `authorized_keys` des Kontos des Remote-Benutzers kopiert. Wenn dies erfolgreich war, fahren Sie mit [Schritt 3](#step-3-%E2%80%94-authenticating-to-your-ubuntu-server-using-ssh-keys) fort.

### Manuelles Kopieren des öffentlichen Schlüssels

Wenn Sie keinen passwortbasierten SSH-Zugriff auf Ihren Server haben, müssen Sie den obigen Vorgang manuell ausführen.

Wir werden den Inhalt Ihrer Datei `id_rsa.pub` manuell an die Datei `~/.ssh/authorized_keys` auf Ihrem Remote-Computer anhängen.

Um den Inhalt Ihres Schlüssels `id_rsa.pub` anzuzeigen, geben Sie Folgendes in Ihren lokalen Computer ein:

Der Inhalt des Schlüssels wird angezeigt, der ungefähr so aussehen sollte:

```
Output

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCqql6MzstZYh1TmWWv11q5O3pISj2ZFl9HgH1JLknLLx44+tXfJ7mIrKNxOOwxIxvcBF8PXSYvobFYEZjGIVCEAjrUzLiIxbyCoxVyle7Q+bqgZ8SeeM8wzytsY+dVGcBxF6N4JS+zVk5eMcV385gG3Y6ON3EG112n6d+SMXY0OEBIcO6x+PnUSGHrSgpBgX7Ks1r7xqFa7heJLLt2wWwkARptX7udSq05paBhcpB0pHtA1Rfz3K2B+ZVIpSDfki9UVKzT8JUmwW6NNzSgxUfQHGwnW7kj4jp4AT0VZk3ADw497M2G/12N0PPB5CnhHf7ovgy6nL1ikrygTKRFmNZISvAcywB9GVqNAVE+ZHDSCuURNsAInVzgYo9xgJDW8wUw2o8U77+xiFxgI5QSZX3Iq7YLMgeksaO4rBJEa54k8m5wEiEE1nUhLuJ0X/vh2xPff6SQ1BL/zkOhvJCACK6Vb15mDOeCSq54Cr7kvS46itMosi/uS66+PujOO+xt/2FWYepz6ZlN70bRly57Q06J+ZJoc9FfBCbCyYH7U/ASsmY095ywPsBo1XQ9PqhnN1/YOorJ068foQDNVpm146mUpILVxmq41Cj55YKHEazXGsdBIbXWhcrRf4G2fJLRcGUr9q8/lERo9oxRm5JFX6TCmj6kmiFqv+Ow9gI0x8GvaQ== demo@test 
```

Greifen Sie mit der jeweils verfügbaren Methode auf Ihren Remote-Host zu.

Sobald Sie Zugriff auf Ihr Konto auf dem Remote-Server haben, sollten Sie sicherstellen, dass das Verzeichnis `~/.ssh` vorhanden ist. Dieser Befehl erstellt bei Bedarf das Verzeichnis oder unternimmt nichts, wenn es bereits vorhanden ist:

Jetzt können Sie die Datei `authorized_keys` in diesem Verzeichnis erstellen oder ändern. Sie können den Inhalt Ihrer Datei `id_rsa.pub` an das Ende der Datei `authorized_keys` anfügen und diese bei Bedarf mit folgendem Befehl erstellen:

Ersetzen Sie im obigen Befehl `==public_key_string==​​​​` durch die Ausgabe des Befehls `cat~/.ssh/id_rsa.pub`, den Sie auf Ihrem lokalen System ausgeführt haben. Sie sollte mit `ssh-rsa AAAA...` beginnen.

Schließlich stellen wir sicher, dass für das Verzeichnis `~/.ssh` und die Datei `authorized_keys` die folgenden Berechtigungen festgelegt sind:

Dadurch werden rekursiv alle „Gruppen-“ und „anderen“ Berechtigungen für das Verzeichnis `~/.ssh/` entfernt.

Wenn Sie das Konto **root** zum Einrichten von Schlüsseln für ein Benutzerkonto verwenden, ist es auch wichtig, dass das Verzeichnis `~/.ssh` dem Benutzer und nicht **root** gehört:

In diesem Tutorial heißt unser Benutzer ==sammy==; aber Sie sollten den entsprechenden Benutzernamen in den obigen Befehl einsetzen.

Wir können jetzt eine passwortlose Authentifizierung mit unserem Ubuntu-Server versuchen.

## Schritt 3 – Authentifizierung bei Ihrem Ubuntu-Server mit SSH-Schlüsseln

Wenn Sie eines der oben genannten Verfahren erfolgreich abgeschlossen haben, sollten Sie sich *ohne* das Passwort des Remote-Kontos beim Remote-Host anmelden können.

Der grundlegende Prozess ist der gleiche:

Wenn Sie zum ersten Mal eine Verbindung zu diesem Host herstellen (wenn Sie die letzte Methode oben verwendet haben), wird möglicherweise Folgendes angezeigt:

```
Output

The authenticity of host '==203.0.113.1== (==203.0.113.1==)' can't be established.
ECDSA key fingerprint is fd:fd:d4:f9:77:fe:73:84:e1:55:00:ad:d6:6d:22:fe.
Are you sure you want to continue connecting (yes/no)? ==yes== 
```

Das bedeutet, dass Ihr lokaler Computer den Remote-Host nicht erkennt. Geben Sie „yes“ ein und drücken Sie dann `ENTER`, um fortzufahren.

Wenn Sie keine Passphrase für Ihren privaten Schlüssel angegeben haben, werden Sie sofort angemeldet. Wenn Sie beim Erstellen des Schlüssels eine Passphrase für den privaten Schlüssel eingegeben haben, werden Sie aufgefordert, diese jetzt einzugeben (beachten Sie, dass Ihre Tastatureingaben aus Sicherheitsgründen nicht in der Terminalsitzung angezeigt werden). Nach der Authentifizierung sollte eine neue Shell-Sitzung mit dem konfigurierten Konto auf dem Ubuntu-Server für Sie geöffnet werden.

Wenn die schlüsselbasierte Authentifizierung erfolgreich war, fahren Sie fort, um sich zu informieren, wie Sie Ihr System durch Deaktivieren der Passwortauthentifizierung weiter sichern können.

## Schritt 4 – Deaktivieren der Passwortauthentifizierung auf Ihrem Server

Wenn Sie sich mit SSH ohne Passwort bei Ihrem Konto anmelden konnten, haben Sie die auf SSH-Schlüssel basierte Authentifizierung für Ihr Konto erfolgreich konfiguriert. Ihr passwortbasierter Authentifizierungsmechanismus ist jedoch weiterhin aktiv. Dies bedeutet, dass Ihr Server weiterhin Brute-Force-Angriffen ausgesetzt ist.

Stellen Sie vor dem Ausführen der in diesem Abschnitt beschriebenen Schritte sicher, dass entweder die auf SSH-Schlüssel basierte Authentifizierung für das **root**-Konto auf diesem Server konfiguriert ist oder dass vorzugsweise die auf SSH-Schlüssel basierte Authentifizierung für ein non-root-Konto und mit `sudo`-Berechtigungen konfiguriert ist. Durch diesen Schritt werden passwortbasierte Anmeldungen gesperrt. Daher ist es von entscheidender Bedeutung, dass Sie weiterhin über Administratorrechte verfügen.

Sobald Sie bestätigt haben, dass Ihr Remote-Konto über administrative Berechtigungen verfügt, melden Sie sich mit SSH-Schlüsseln bei Ihrem Remote-Server an, entweder als **root** oder mit einem Konto mit `sudo`-Berechtigungen. Öffnen Sie dann die Konfigurationsdatei des SSH-Daemons:

Suchen Sie in der Datei nach einer Anweisung namens `PasswordAuthentication`. Diese Zeile kann mit einem `#` am Anfang der Zeile kommentiert werden. Entfernen Sie das Kommentarzeichen `#` und setzen Sie den Wert auf `no`. Dies deaktiviert Ihre Möglichkeit, sich über SSH mit Kontopasswörtern anzumelden:

/etc/ssh/sshd_config

```
. . .
PasswordAuthentication no
. . . 
```

Speichern und schließen dann noch die Datei durch Drücken von `STRG+ X`, anschließend von `Y`, um das Speichern der Datei zu bestätigen und abschließend durch Drücken von `ENTER`, um nano zu verlassen. Um diese Änderungen zu aktivieren, müssen wir den `sshd` Dienst neu starten:

Öffnen Sie vorsichtshalber ein neues Terminalfenster und testen Sie, ob der SSH-Dienst ordnungsgemäß funktioniert, bevor Sie Ihre aktuelle Sitzung schließen:

Nachdem Sie überprüft haben, dass der SSH Dienst korrekt funktioniert, können Sie alle aktuellen Serversitzungen sicher schließen.

Der SSH-Daemon auf Ihrem Ubuntu-Server reagiert jetzt nur noch auf eine Authentifizierung mit einem SSH-Schlüssel. Eine Anmeldung per Passwort ist deaktiviert.

## Zusammenfassung

Auf Ihrem Server sollte jetzt die auf SSH-Schlüsseln basierte Authentifizierung konfiguriert sein, damit Sie sich anmelden können, ohne ein Kontopasswort anzugeben.

Wenn Sie mehr über das Arbeiten mit SSH erfahren möchten, sehen Sie sich unseren [Leitfaden über SSH-Grundlagen](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys) an.