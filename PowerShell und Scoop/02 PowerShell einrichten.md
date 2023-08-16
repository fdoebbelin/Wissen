---
source: https://ohmyposh.dev/
---

besserer Prompt mit Oh My Posh

```sh
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
scoop install nerd-fonts/Meslo-NF
scoop install nerd-fonts/Meslo-NF-Mono
# oh-my-posh font install
```

Windows Terminal konfigurieren
To ensure correct rendering of the glyphs you will need to enable the option `Use the new text renderer ("AtlasEngine")` in your terminal settings. For further details, see [here](https://github.com/microsoft/terminal/issues/8993).

Once you have installed a Nerd Font, you will need to configure the Windows Terminal to use it. This can be easily done by modifying the Windows Terminal settings (default shortcut: `CTRL + SHIFT + ,`). In your `settings.json` file, add the `font.face` attribute under the `defaults` attribute in `profiles`:

```json
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

geht auch über das Menü PowerShell>Darstellung>Schriftart

```
Schriftart: MesloGM NF
```

### Prompt ändern
Edit your PowerShell profile script, you can find its location under the `$PROFILE` variable in your preferred PowerShell version. For example, using notepad:

```sh
code $PROFILE
oh-my-posh init pwsh | Invoke-Expression
```

Once added, reload your profile for the changes to take effect.

```sh
. $PROFILE
```