
Hat man im Hyper-V von Microsoft ein Ubuntu/Linux als virtuelle Maschine installiert, kann es vorkommen, dass die Bildschirmauflösung des Ubuntus sehr klein ist und nicht die mögliche Auflösung des physikalisch vorhanden Monitors einnimmt, wie zum Beispiel im nachfolgenden Bild dargestellt.

![](https://ekiwi-blog.de/wp-content/uploads/2022/03/bildschirmaufloesung-ubuntu-hyper-v.png)

Die Einstellungen zum Anzeigegerät unter Ubuntu bieten in diesem Fall auch nur eine bestimmte Auflösung an und es lässt sich keine andere auswählen.

![](https://ekiwi-blog.de/wp-content/uploads/2022/03/einstellungen-anzeigegeraet-ubuntu.png)

Um die Auflösung an den Monitor anzupassen muss man Anpassungen an der Konfigurationsdatei des GRUB-Bootloader von Linux vornehmen. Dafür muss man die grub-Datei bearbeiten.

Man ruft als in seinem virtuellen Ubuntu das Terminal auf. Zuerst muss man linux-image-extras installieren. Es handelt sich dabei um die erforderlichen Hyper-V-Treiber.

`~$ sudo apt-get install linux-image-extra-virtual`

Ggf. kommt es noch zu einer Problemmeldung, dass man folgendes manuell ausführen soll.

`~$ sudo dpkg --configure -a`

Im Terminal gibt man folgenden Befehl ein, um die grub-Datei mit dem Nano-Editor zu öffnen:

`~$ sudo nano /etc/default/grub`

Innerhalb der grub-Konfigurationsdatei muss man den Eintrag `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"` finden und `quiet splash` noch ergänzen um `video=hyperv_fb:1920×1080`. Vollständig sieht das also so aus:

`GRUB_CMDLINE_LINUX_DEFAULT="quiet splash video=hyperv_fb:1920×1080"`

![](https://ekiwi-blog.de/wp-content/uploads/2022/03/grub-nano-konfigurationsdatei.png)

Jetzt noch die Konfigurationsdatei im Nano-Editor speichern (Strg+O) und den Editor verlassen (Strg+X). Der Bootloader muss jetzt noch mit folgendem Befehl geupdated werden

`~$ sudo update-grub`

![](https://ekiwi-blog.de/wp-content/uploads/2022/03/terminal-grub-update.png)

Danach startet man die virtuelle Maschine neu (Befehl **reboot** im Terminal). Das Ubuntu startet dann mit der entsprechenden Auflösung. Verständlicherweise wird man eine Auflösung wählen, die mit dem verwendeten Monitor übereinstimmt. Es sind aber auch theoretisch andere individuelle Bildschirmauflösungen denkbar.

In meinem konkreten Fall konnte ich jedoch nur Full-HD (1980×1080) einstellen, obwohl der physische Monitor bis 2550×1440 unterstützt. Wähle ich letztere Einstellung, springt die VM auf die kleine Standard-Auflösung zurück. Ich vermute, es handelt sich hierbei um ein Treiberproblem, wodurch diese hohe Bildschirmauflösung nicht unterstützt wird.