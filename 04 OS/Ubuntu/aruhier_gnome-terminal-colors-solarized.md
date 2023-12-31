Scripts for setting the Solarized color set with Gnome Terminal. To get nicely colored directory listings, you will also need to set up a [dircolors solarised color theme](https://github.com/seebi/dircolors-solarized).

For Mate Terminal, you can use [mate-terminal-colors-solarized](https://github.com/cledoux/mate-terminal-colors-solarized), maintained by @cledoux.

## <a id="user-content-colors"></a>[](#colors)Colors

Only the foreground, background and highlight colors are different in the light and dark color sets, as one of the main ideas behind Ethan Schonoovers work is to use the same colors in the palette for both.

See the [Solarized homepage](http://ethanschoonover.com/solarized) for theory behind the colors, screenshots, details and colorscheme versions for Vim, Mutt, popular terminal emulators and other applications.

For the original works of Ethan Schoonover, visit the [Solarized repository](https://github.com/altercation/solarized). The scripts for Gnome Terminal is maintained in [Gnome Terminal Colors Solarized repository](https://github.com/sigurdga/gnome-terminal-colors-solarized).

## <a id="user-content-installation-and-usage"></a>[](#installation-and-usage)Installation and usage

To be able to uninstall, we highly recommend that you create a new Gnome Terminal profile, using the menus in Gnome Terminal.

You need the `dconf` command (if you run a recent Gnome version). With Ubuntu, this can be installed by running

```
$ sudo apt-get install dconf-cli

```

Then clone the repository and you can run the installation script:

```
$ git clone https://github.com/aruhier/gnome-terminal-colors-solarized.git
$ cd gnome-terminal-colors-solarized
$ ./install.sh

```

And just follow the instructions.

You can also run the `set_dark.sh` or `set_light.sh` script, to directly set the dark or light solarized theme to the actived gnome-terminal profile. The options `--install-dircolors` or `--skip-dircolors` can also be used to install or not the solarized dircolors in a non-interactive mode.

To run this script remotely or via cron (or from any shell where `DBUS_SESSION_BUS_ADDRESS` is not set), you need to start a dbus connection:

```
$ dbus-launch ./install.sh

```

## <a id="user-content-uninstall"></a>[](#uninstall)Uninstall

Change to another profile in Gnome Terminal, then remove the Solarized profile by running:

### <a id="user-content-gnome-36-or-lower"></a>[](#gnome-36-or-lower)Gnome 3.6 or lower

```
$ rm -r ~/.gconf/apps/gnome-terminal/profiles/Solarized/
$ gconftool-2 --recursive-unset /apps/gnome-terminal

```

### <a id="user-content-gnome-38-or-higher"></a>[](#gnome-38-or-higher)Gnome 3.8 or higher

Be sure to have the dconf-cli package installed and do:

```
$ dconf reset -f /org/gnome/terminal/legacy/profiles:/PROFILE_ID"

```

Replace PROFILE_ID by your profile ID (you can get it in your profile configuration in gnome-terminal).

## <a id="user-content-themes"></a>[](#themes)Themes

Each theme has is own folder in the `colors` dir. It contains the following files:

- bd_color: bold color
- bg_color: background color
- fg_color: foreground color
- palette: list of colors for all standard color codes.

No additional configuration is needed to add a theme, the installation script just list at launch the children folders in the `colors` dir.

## <a id="user-content-dircolors"></a>[](#dircolors)Dircolors

The installation script will ask if a solarized dircolors is wanted. It will be downloaded and installed as `~/.dir_colors/dircolors`. On CentOS, it can be an issue (see issue #62), as the default setup use `~/.dir_colors` as dircolors. In that case, you should manually move `~/.dir_colors` as `~/.dir_colors/dircolors` before starting the installation script.

If the dircolors is not applied, please check that your shell actually source your dircolors:

```
if [ -f ~/.dir_colors/dircolors ]
    then eval `dircolors ~/.dir_colors/dircolors`
fi

```

This should not be necessary on major distributions (such as Ubuntu, Fedora, etc.) but could be on ArchLinux, Gentoo and others.

## <a id="user-content-contributors"></a>[](#contributors)Contributors

- Sigurd Gartmann [sigurdga@sigurdga.no](mailto:sigurdga@sigurdga.no)
- Anthony Ruhier [anthony.ruhier@gmail.com](mailto:anthony.ruhier@gmail.com)
- Paul Thomson [captbunzo@gmail.com](mailto:captbunzo@gmail.com)
- Techlive Zheng [techlivezheng@gmail.com](mailto:techlivezheng@gmail.com)
- Daniel Graña [dangra@gmail.com](mailto:dangra@gmail.com)

## <a id="user-content-conflicting-background-colors-in-vim"></a>[](#conflicting-background-colors-in-vim)Conflicting background colors in VIM

Use the 16 colors terminal option to get VIM to look like GVIM with solarized colors.

```
set t_Co=16

```