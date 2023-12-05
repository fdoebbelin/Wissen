
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
