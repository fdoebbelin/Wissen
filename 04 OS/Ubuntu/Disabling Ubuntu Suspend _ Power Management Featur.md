In some configurations, Ubuntu power conservation options are enabled by default.  For server machines this is something that can make the machine unavailable and is generally unsuitable for a server machine.  In a headless (non-GUI) server, these functions can be disabled as follows from the command line:

Disabling power management functions:

```
$ sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
``` 


Re-Enabling power management functions:

```
$ sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target
```
