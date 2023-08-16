I'm trying to install JetBrains Toolbox 1.6.2914 on Ubuntu 17.10

I extracted the `tar.gz` archive into `/opt` directory and I can correctly launch the application using terminal (or double clicking on the executable icon).

But I cannot find it in Gnome application menu. And the application is not even launched a system startup.

How can I properly install Toolbox on my machine?

asked Jan 25 '18 at 15:02

[![](_resources/9cc13546b8983844eaee1c6e5f384d46_172049d0d31e40219.png)](https://askubuntu.com/users/361419/davioooh)

If you launch the Toolbox application once you can click the icon in the top bar and go to settings and you'll see a check box to set it to launch at startup. To get the application to show up in the application menu, you need to have a `.desktop` file for it (mine is in `~./local/share/applications`), I'm not entirely sure how mine arrived there, but I've put it below. You'll want to replace `<username>` with your actual username, and you may want to comment out the `Icon` line because you may not have that file.

```
[Desktop Entry]
Type=Application
Name=JetBrains Toolbox
Exec=/home/<username>/.local/share/JetBrains/Toolbox/bin/jetbrains-toolbox %u
Icon=/home/<username>/.local/share/JetBrains/Toolbox/toolbox.svg
StartupNotify=false
Categories=Development;IDE;
Terminal=false
X-GNOME-Autostart-enabled=true
StartupWMClass=jetbrains-toolbox
MimeType=x-scheme-handler/jetbrains;

```

answered Jan 25 '18 at 17:24

[![](_resources/eed6a4a186f0dd41557bbeb0072f7d34_55d37b90af88468cb.jpg)](https://askubuntu.com/users/700752/wklock)

[wklock](https://askubuntu.com/users/700752/wklock)wklock

6155 bronze badges

With Toolbox 1.8.3678+, it is automatically created on the first start. So you just need to put it somewhere and open it.

> Based on the comment on the accepted answer.

## Not the answer you're looking for? Browse other questions tagged [software-installation](https://askubuntu.com/questions/tagged/software-installation "show questions tagged 'software-installation'") [17.10](https://askubuntu.com/questions/tagged/17.10 "show questions tagged '17.10'") [ubuntu-gnome](https://askubuntu.com/questions/tagged/ubuntu-gnome "show questions tagged 'ubuntu-gnome'") or [ask your own question](https://askubuntu.com/questions/ask).