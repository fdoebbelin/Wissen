We need to set Forwarding to be enabled across the two v-Switches. Using this command (with admin rights) based on my v-Switch names works.

```
Get-NetIPInterface | where {$_.InterfaceAlias -eq 'vEthernet (WSL)' -or $_.InterfaceAlias -eq 'vEthernet (Default Switch)'} | Set-NetIPInterface -Forwarding Enabled
```