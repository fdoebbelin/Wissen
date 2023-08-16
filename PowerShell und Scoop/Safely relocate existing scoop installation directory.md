---
source: https://github.com/ScoopInstaller/Scoop/issues/3852
---
today i move scoop to another disk successfully. you should do the follow things:  
1. move total scoop to new disk. (if use copy, del old scoop folder, or rename it, to make sure old scoop folder is invaild)  
2. open 'scoop/shims/scoop.cmd' and 'scoop/shims/scoop.ps1', update scoop folder path as new location.  
3. open win10 environment variables panel, update all variable path contains scoop path to new scoop location. Especially be careful for 'Path' variable in both User and System.  
4. create new environment variable in System Variable, variable name is "SCOOP", variable value is new scoop location. if "SCOOP" already exists, just update it.(Maybe scoop software only create this env variable when install location is not default "~/scoop" path)  
5. open cmd, execute scoop command, it should work with no any error. execute "where scoop" showing scoop command path, make sure it is new scoop location.  
6. execute "scoop reset *" command to recreate all scoop app folder's "current JUNCTION". (junction canot be copy,so it lost target after copy)  
7. now it is finish. scoop and all scoop app should work fine now.

I have done my moving using this suggested solution, and it works nicely so far.

I'd like to add a few steps/precautions:

- step 0. close all scoop apps and services before doing any moving, check your tray and services (eg. Chrome, MSI Afterburner, mysql server service and such)
- do steps 1-7 as written above
- step 8. adjust your shortcuts if made manually, eg.
    - Taskbar icons/shortcuts

```
Windows + R
Type : shell:User Pinned\Taskbar
Press "OK" or "Enter"
```

- right click all shortcuts from scoop installed apps, Properties, and adjust path to new location
    - note that Chrome / Chromium contain EXE path PLUS a profile path in same shortcut (command line) and you need to point BOTH to correct locations!!
- do same for any shortcuts like on Desktop etc

There may or may not be some apps that need some manual tweaking, eg I've found:

- 7zip file `scoop\apps\7zip\current\install-context.reg` has path inside that will be applied for right-click menu and it will be wrong, needs update to reg, then re-apply reg
- mysql server will need service uninstall and reinstall like this (adjust .ini path to your new location and adjust your path inside the INI file itself eg. my `C:\scoop\apps\mysql\current\my.ini` contains the line pointing to persisted `data` folder which I forgot to change)

```
link: https://dev.mysql.com/doc/refman/8.0/en/windows-start-service.html
mysqld --remove
mysqld --install MySQL --defaults-file="C:\scoop\apps\mysql\current\my.ini"
```

- a lot of apps (Chrome, Notepad++, 7zip, VLC, ZULU Java, ...) that registered as default apps to open certain files/extensions will need manual updating in registry eg.

```
\Software\Classes\Applications\<app name>\shell\open\command
```

I ended up re-scanning whole registry with `Ctrl+F` searching for a string `scoop\apps` and modifying all paths to new location. This included default file handling as noted above, services as MySQL example ( `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` ) and several more places. I've also used that to fix some paths that pointed to paths like `\scoop\apps\<appname>\<version>` instead `\scoop\apps\<appname>\current`, hopefully I did not mess up something ;D

Anyway, messing with registry you need to beware what you're doing, I'm just saying some apps seem to have registry paths, which may or may not get updated on next app update.

Since I've changed few services, I've also done a full PC reboot, and then another `scoop update` and `scoop update "*"` and `scoop cleanup --all` after it was rebooted.

Main apps I care about to stay "intact" (Chrome and Notepad++ with kazillion tabs) still work fine after this procedure.