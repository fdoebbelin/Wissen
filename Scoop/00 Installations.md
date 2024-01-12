
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
scoop instal git
scoop bucket add extras
git config --global credential.helper manager-core
scoop install windows-terminal

winget search Microsoft.PowerShell
winget install --id Microsoft.Powershell --source winget

scoop install sudo
Add-LocalGroupMember -Group "Administrators" -Member "NEW_ACCOUNT_NAME"
```

Windows-Terminal im Explorer-Kontektmenü

```
reg import "C:\Users\Fritz-RainerDöbbelin\scoop\apps\windows-terminal\current\install-context.reg"

```

Update WSL

```
wsl --update
wsl --shutdown
wsl --set-default-version 2
wsl --list --online
wsl --install -d Ubuntu
wsl --list
```
