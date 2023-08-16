## Windows-Features aktivieren oder deaktivieren

```Start
Systemsteuerung>Programme>Windows-Features aktivieren oder deaktivieren
Hyper-V
VM-Plattform
```
oder

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
```


## Install WSL command

You can now install everything you need to run WSL with a single command. Open PowerShell or Windows Command Prompt in **administrator** mode by right-clicking and selecting "Run as administrator", enter the wsl --install command, then restart your machine.

PowerShellCopy

```
wsl --install
```

This command will enable the features necessary to run WSL and install the Ubuntu distribution of Linux. ([This default distribution can be changed](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#install)).

If you're running an older build, or just prefer not to use the install command and would like step-by-step directions, see **[WSL manual installation steps for older versions](https://learn.microsoft.com/en-us/windows/wsl/install-manual)**.

The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for files to de-compress and be stored on your machine. All future launches should take less than a second.

 Note

The above command only works if WSL is not installed at all, if you run `wsl --install` and see the WSL help text, please try running `wsl --list --online` to see a list of available distros and run `wsl --install -d <DistroName>` to install a distro. To uninstall WSL, see [Uninstall legacy version of WSL](https://learn.microsoft.com/en-us/windows/wsl/troubleshooting#uninstall-legacy-version-of-wsl) or [unregister or uninstall a Linux distribution](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#unregister-or-uninstall-a-linux-distribution).

## Change the default Linux distribution installed

By default, the installed Linux distribution will be Ubuntu. This can be changed using the `-d` flag.

-   To change the distribution installed, enter: `wsl --install -d <Distribution Name>`. Replace `<Distribution Name>` with the name of the distribution you would like to install.
-   To see a list of available Linux distributions available for download through the online store, enter: `wsl --list --online` or `wsl -l -o`.
-   To install additional Linux distributions after the initial install, you may also use the command: `wsl --install -d <Distribution Name>`.

 Tip

If you want to install additional distributions from inside a Linux/Bash command line (rather than from PowerShell or Command Prompt), you must use .exe in the command: `wsl.exe --install -d <Distribution Name>` or to list available distributions: `wsl.exe -l -o`.

If you run into an issue during the install process, check the [installation section of the troubleshooting guide](https://learn.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues).

To install a Linux distribution that is not listed as available, you can [import any Linux distribution](https://learn.microsoft.com/en-us/windows/wsl/use-custom-distro) using a TAR file. Or in some cases, [as with Arch Linux](https://wsldl-pg.github.io/ArchW-docs/How-to-Setup/), you can install using an `.appx` file. You can also create your own [custom Linux distribution](https://learn.microsoft.com/en-us/windows/wsl/build-custom-distro) to use with WSL.

## Set up your Linux user info

Once you have installed WSL, you will need to create a user account and password for your newly installed Linux distribution. See the [Best practices for setting up a WSL development environment](https://learn.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password) guide to learn more.

## Set up and best practices

We recommend following our [Best practices for setting up a WSL development environment](https://learn.microsoft.com/en-us/windows/wsl/setup/environment) guide for a step-by-step walk-through of how to set up a user name and password for your installed Linux distribution(s), using basic WSL commands, installing and customizing Windows Terminal, set up for Git version control, code editing and debugging using the VS Code remote server, good practices for file storage, setting up a database, mounting an external drive, setting up GPU acceleration, and more.