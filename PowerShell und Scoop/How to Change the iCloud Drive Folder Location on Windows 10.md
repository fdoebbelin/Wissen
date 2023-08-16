
```PowerShell
cmd /c mklink /J "C:\Users\f.doebbelin\iCloud Drive" "C:\Users\Public\iCloud Drive"

New-Item -ItemType SymbolicLink -Path "C:\Users\f.doebbelin\iCloud Drive" -Target "C:\Users\Public\iCloud Drive"
```
