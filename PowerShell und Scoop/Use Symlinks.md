
```PowerShell
cmd /c mklink /J "C:\Users\f.doebbelin\Desktop\Moodle" "D:\targets\Moodle"

New-Item -ItemType SymbolicLink -Path "C:\Users\f.doebbelin\Desktop\Moodle" -Target "D:\targets\Moodle"
```
