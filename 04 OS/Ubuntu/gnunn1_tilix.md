#### <a id="user-content-background"></a>[](#background)Background

Tilix uses a GTK+ 3 widget called VTE (Virtual Terminal Emulator). The VTE widget was originally designed as the back-end for GNOME Terminal but was fortunately designed as a GTK widget so that other terminal emulator applications could leverage it instead of rolling their own. Many popular Linux terminal emulators use this component.

One aspect of VTE configuration is the use of /etc/profile.d/vte.sh. The VTE uses this script to override the PROMPT_COMMAND in order to feed itself additional information via terminal control codes. In particular, this script is used to tell the VTE the current directory of the shell. Previously the VTE component used to read this from /proc/&lt;pid&gt;/cwd however according to [VTE upstream](https://bugzilla.gnome.org/show_bug.cgi?id=697475) there were a number of issues with this approach and hence the change to /etc/profile.d/vte.sh.

The issue with this change though is that different distributions treat /etc/profile.d differently. The expectation is that when a shell is initiated all scripts in /etc/profile.d are executed. On Fedora, this works as expected for both login and non-login based shells. However, other distributions (Ubuntu and Arch at least) only execute scripts in /etc/profile.d for login shells. The problem with this is the default configuration for most terminal emulators using VTE, including GNOME Terminal and Tilix, is to not run the shell as a login shell.

#### <a id="user-content-impact"></a>[](#impact)Impact

This means that on some Linux distributions vte.sh never gets executed and VTE loses certain features that are dependent on the PROMPT_COMMAND. In particular, the two features that we know are impacted:

- The current directory is never reported by VTE. This means when splitting terminals in Tilix instead of inheriting the directory from the current terminal the split terminal always opens in your home terminal. GNOME Terminal has the same issue when creating new tabs
- The Fedora patched VTE that provides notification support depends on PROMPT_COMMAND, so this issue means notifications will not work.

#### <a id="user-content-fixing-the-issue"></a>[](#fixing-the-issue)Fixing the issue

Fortunately fixing this issue is quite easy, you can do either of the two options below.

##### <a id="user-content-1-source-vtesh-in-bashrc"></a>[](#1-source-vtesh-in-bashrc)1\. Source vte.sh in bashrc

Update `~.bashrc` (or `~.zshrc` if you are using zsh) to execute vte.sh directly, this involves adding the following line at the end of the file.

```
if [[ $TILIX_ID ]]; then
        source /etc/profile.d/vte.sh
fi 
```

On Ubuntu (16.04), a symlink is probably missing. You can create it with:

```
ln -s /etc/profile.d/vte-2.91.sh /etc/profile.d/vte.sh 
```

If you use a custom `PROMPT_COMMAND` instead of simply overriding `PS1` you also need to update your `PROMPT_COMMAND` to append working directory information. This can be achieved by calling `__vte_osc7` which gets defined when you source `/etc/profile.d/vte-2.91.sh`.

```
function custom_prompt() {
  __git_ps1 "\[\033[0;31m\]\u \[\033[0;36m\]\h:\w\[\033[00m\]" " \n\[\033[0;31m\]>\[\033[00m\] " " %s"
  VTE_PWD_THING="\[$(__vte_osc7)\]"
  PS1="$PS1$VTE_PWD_THING"
}
PROMPT_COMMAND=custom_prompt 
```

##### <a id="user-content-2-or-use-a-login-shell"></a>[](#2-or-use-a-login-shell)2\. OR use a login shell

Enable the option in your Tilix Profile (under Preferences) to use a login shell, the screenshot below shows the option that needs to be checked.

![Profile - Command](_resources/687474703a2f2f67657870657274732e_5a95a31b90314d628.png)