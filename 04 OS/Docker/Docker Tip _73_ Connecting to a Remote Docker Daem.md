# 1. Configure the Docker daemon to allow remote connections:

Keep in mind this is only meant to be used for local connections between your newly minted VM and your dev box with WSL. This is not meant to be used to connect from external networks because we’re going to connect unencrypted.

The reason we’re doing it over an unencrypted channel is because otherwise you’ll need to set up SSL certificates. You could always create self-signed certs and use those if you’re paranoid about local network traffic not being encrypted.

```
# These commands get run inside of your VM.

# Create the directory to store the configuration file.
sudo mkdir -p /etc/systemd/system/docker.service.d

# Create a new file to store the daemon options.
sudo nano /etc/systemd/system/docker.service.d/options.conf

# Now make it look like this and save the file when you're done:
[Service]
ExecStart=
ExecStart=/usr/bin/dockerd -H unix:// -H tcp://0.0.0.0:2375

# Reload the systemd daemon.
sudo systemctl daemon-reload

# Restart Docker.
sudo systemctl restart docker
```

That’s going to let you continue to connect to the Docker daemon from within the VM thanks to `-H unix://`, but it also exposes the Docker Daemon with `-H tcp://0.0.0.0:2375` so that anyone can connect to it over the non-encrypted port.

When I say “anyone”, that would be anyone on your local network, assuming you have a router / firewall that is blocking port 2375 from the outside world.

# 2. Configuring your dev box to connect to the remote Docker daemon:

You could run `DOCKER_HOST=tcp://X.X.X.X:2375 docker info` where you’ll want to replace `X.X.X.X` with your server’s IP address (or hostname).

If you want to set `DOCKER_HOST` by default so it always connects remotely you can export it in your `~/.bashrc` file. Here’s an example of that as a 1 liner:

```
echo "export DOCKER_HOST=tcp://X.X.X.X:2375" >> ~/.bashrc && source ~/.bashrc
```
That just adds the export line to your `.bashrc` file so it’s available every time you open your terminal. The `source` command reloads your bash configuration so it takes effect now.

Congratulations, you’re now able to connect to a remote Docker daemon.