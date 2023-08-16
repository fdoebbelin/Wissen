Installing Node.js through standard Ubuntu repository is pretty straight-forward. Open a terminal and issue the following –

```
sudo apt update
sudo apt install nodejs
```

First, we have updated the repository to make the latest version of the package available. Thereafter, package i.e. Node.js was installed.

To verify whether the package has successfully installed, run either of the following –

```
node -v
nodejs -v
```

It would return with the version of the package installed. In our case, we could install version 10.15.2.