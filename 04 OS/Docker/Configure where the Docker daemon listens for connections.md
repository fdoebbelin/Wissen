By default, the Docker daemon listens for connections on a UNIX socket to accept requests from local clients. It is possible to allow Docker to accept requests from remote hosts by configuring it to listen on an IP address and port as well as the UNIX socket. For more detailed information on this configuration option take a look at “Bind Docker to another host/port or a unix socket” section of the [Docker CLI Reference](https://docs.docker.com/engine/reference/commandline/dockerd/) article.

Configuring Docker to accept remote connections can be done with the `docker.service` systemd unit file for Linux distributions using systemd, such as recent versions of RedHat, CentOS, Ubuntu and SLES.

### Configuring remote access with `systemd` unit file

1.  Use the command `sudo systemctl edit docker.service` to open an override file for `docker.service` in a text editor.
    
2.  Add or modify the following lines, substituting your own values.
    
    ```
    [Service]
    ExecStart=
    ExecStart=/usr/bin/dockerd -H fd:// -H tcp://127.0.0.1:2375
    ```
    
3.  Save the file.
    
4.  Reload the `systemctl` configuration.
    
    ```
     $ sudo systemctl daemon-reload
    ```
    
5.  Restart Docker.
    
    ```
    $ sudo systemctl restart docker.service
    ```
    
6.  Check to see whether the change was honored by reviewing the output of `netstat` to confirm `dockerd` is listening on the configured port.
    
    ```
    $ sudo netstat -lntp | grep dockerd
    tcp        0      0 127.0.0.1:2375          0.0.0.0:*               LISTEN      3758/dockerd
    ```