---
source: https://ohmyposh.dev/
---

A prompt theme engine for any shell.

```PowerShell
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
```

passende Schriftart installieren
```PowerShell
scoop bucket add nerd-fonts
scoop install Meslo-NF
code ~\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
{
    "profiles":
    {
        "defaults":
        {
            "font":
            {
                "face": "MesloLGM NF"
            }
        }
    }
}
```

Prompt einrichten
```PowerShell
New-Item -Path $PROFILE -Type File -Force
code $PROFILE
oh-my-posh init pwsh | Invoke-Expression

. $PROFILE
```

### VS Code

When using Visual Studio Code, you will need to configure the integrated Terminal to make use of the Nerd Font as well. This can be done by changing the `Integrated: Font Family` value in the Terminal settings (default shortcut: `CTRL + ,` and search for `Integrated: Font Family` or via `Users` -> `Features` -> `Terminal`).

If you are using the JSON based settings, you will need to update the `terminal.integrated.fontFamily` value. Example in case of `MesloLGM NF` Nerd Font:

```
"terminal.integrated.fontFamily": "MesloLGM NF"
```
