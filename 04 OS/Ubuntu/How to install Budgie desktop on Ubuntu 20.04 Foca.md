Details

Ubuntu

27 April 2020

The objective of this tutorial is to install Budgie desktop as an [alternative desktop environment](https://linuxconfig.org/the-8-best-ubuntu-desktop-environments-20-04-focal-fossa-linux) on [Ubuntu 20.04](https://linuxconfig.org/ubuntu-20-04-guide) Focal Fossa Desktop/Server Linux.

**In this tutorial you will learn:**

- How to install `tasksel`
- How to install Budgie desktop
- How to switch to lightdm display manager
- How to login to Budgie desktop

![](resources/09-how-to-install-budgie-desktop_ba09fa8437a5462ea.png)Budgie desktop on Ubuntu 20.04 Focal Fossa Linux

## Software Requirements and Conventions Used

|     |     |
| --- | --- |Software Requirements and Linux Command Line Conventions
| Category | Requirements, Conventions or Software Version Used |
| --- | --- |
| System | [Installed Ubuntu 20.04](https://linuxconfig.org/how-to-install-ubuntu-20-04-focal-fossa-desktop) or [upgraded Ubuntu 20.04 Focal Fossa](https://linuxconfig.org/how-to-upgrade-ubuntu-to-20-04-lts-focal-fossa) |
| Software | tasksel |
| Other | Privileged access to your Linux system as root or via the `sudo` command. |
| Conventions | **#** \- requires given [linux commands](https://linuxconfig.org/linux-commands) to be executed with root privileges either directly as a root user or by use of `sudo` command  <br>**$** \- requires given [linux commands](https://linuxconfig.org/linux-commands) to be executed as a regular non-privileged user |

## Install Budgie desktop on Ubuntu 20.04 step by step instructions

1.  We will be using the `tasksel` command to install Budgie desktop. In case the `tasksel` command is not available on your system you can install it by:
    
    $ sudo apt install tasksel
	
3.  Execute the following command to begin the Budgie desktop installation:
    
    $ sudo tasksel install ubuntu-budgie-desktop
    
    [![Budgie desktop installation command on Ubuntu 20.04](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/01-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Budgie desktop installation command on Ubuntu 20.04")
    
    Budgie desktop installation command on Ubuntu 20.04
    
    [![Wait for tasksel to complete the Budgie desktop installation](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/02-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Wait for tasksel to complete the Budgie desktop installation")
    
    Wait for `tasksel` to complete the Budgie desktop installation
    
4.    
    
    [![Lightdm configuration information](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/04-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Lightdm configuration information")
    
    Lightdm configuration information
    
    [![Use TAB to select lightdm and hit ok button](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/05-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Use TAB to select lightdm and hit ok button")
    
    Use TAB to select lightdm and hit `ok` button
    
5.    
    Reboot your Ubuntu 20.04 system:
    
    [![Reboot your Ubuntu 20.04 system](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/06-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Reboot your Ubuntu 20.04 system")
    
    Reboot your Ubuntu 20.04 system
    
6.  Select Desktop session as `Budgie`:
    
    [![Open Desktop session selection menu](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/07-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Open Desktop session selection menu")
    
    Open Desktop session selection menu
    
    [![Select Budgie Desktop, enter your password and hit login button](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)](https://linuxconfig.org/images/08-how-to-install-budgie-desktop-on-ubuntu-20-04-focal-fossa-linux.png "Select Budgie Desktop, enter your password and hit login button")
    
    Select `Budgie Desktop`, enter your password and hit login button
    

***LINUX CAREER NEWSLETTER**  
Subscribe to [NEWSLETTER](https://bit.ly/2X5D30q) and receive latest news, jobs, career advice and tutorials.*

***DO YOU NEED ADDITIONAL HELP?**  
Get extra help by visiting our [LINUX FORUM](https://forum.linuxconfig.org/) or simply use comments below.*

* * *

* * *

**Comments and Discussions**  
![](_resources/blank_b28b4c0d0ab64025a0eaab6c2e735f39.gif)