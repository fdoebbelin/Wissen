---
source:
---
Installation
```sh
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
```

Liste aller bekannten Repositories

```sh
scoop bucket known
main
extras
versions
nirsoft
sysinternals
php
nerd-fonts
nonportable
java
games
```

Nutzung weiterer Repositories

```sh
scoop install git
scoop bucket add extras
scoop bucket add nerd-fonts
```

interessante Pakete

```sh
scoop list
Installed apps:

Name                          Version                     Source
----                          -------                     ------
7zip                          22.01                       main
anki                          2.1.65                      extras
another-redis-desktop-manager 1.5.9                       extras
busybox                       4784-g5507c8744             main
calibre-normal                6.6.1                       extras
composer                      2.5.5                       main
cwrsync                       6.2.7                       main
dark                          3.11.2                      main
discord                       1.0.9010-15                 extras
dosbox-x                      0.84.2                      extras
dotnet-sdk                    6.0.400                     main
draw.io                       21.2.8                      extras
ffmpeg                        6.0                         main
ghostscript                   9.56.1                      main
gimp                          2.10.34                     extras
git                           2.37.2.windows.2            main
godot                         3.5.1                       extras
googlechrome                  109.0.5414.129              extras
inkscape                      1.2.2_2022-12-09_732a01da63 extras
innounp                       0.50                        main
mariadb                       10.9.3                      main
meld                          3.22.0                      extras
Meslo-NF                      2.3.3                       nerd-fonts
Meslo-NF-Mono                 2.3.3                       nerd-fonts
mysql-workbench               8.0.31                      main
oh-my-posh                    14.9.1                      https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest…
openssh                       9.2.0.0p1                   main
pandoc                        2.19.2                      main
pdfarranger                   1.9.2                       extras
pdftk                         2.02                        main
pdftk-builder                 3.10.0                      extras
poppler                       22.11.0-0                   main
powertoys                     0.70.1                      extras
python                        3.11.1                      main
redis                         5.0.14.1                    main
sqlitestudio                  3.4.3                       extras
symfony-cli                   5.5.2                       main
telnet                        msys-inetutils-1.7-1        main
tesseract                     5.3.0.20221214              main
tesseract-languages
which                         2.20                        main
windirstat                    1.1.2                       extras
winscp                        5.21.8                      extras
wkhtmltopdf                   0.12.6-1                    main
yarn                          1.22.19                     main
youtubedownloader             1.9.10                      extras
zoom                          5.13.5.12053                extras
```
