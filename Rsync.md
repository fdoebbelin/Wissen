## rsync keeps disconnecting: broken pipe
fixed this by upgrading to rsync v3.11. The issue was happening on v2.6.9. 
``` shell 
$ brew install rsync
$ rsync --version
rsync  version 3.1.2  protocol version 31
```