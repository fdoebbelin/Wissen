```
$ ssh root@192.168.1.1
sign_and_send_pubkey: signing failed: agent refused operation
```
The file permissions were too open (0644).

The following command solved it:

```
$ chmod 600 ~/.ssh/id_rsa
```