 Add the following line to your `/etc/apt/sources.list`.

```
$ sudo vi /etc/apt/sources.list
deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian eoan contrib
```
The Oracle public key for apt-secure can be combine downloading and registering:

```
$ wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
$ wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
```

The key fingerprint for oracle_vbox_2016.asc is

```
B9F8 D658 297A F3EF C18D  5CDF A2F6 83C5 2980 AECF
Oracle Corporation (VirtualBox archive signing key) <info@virtualbox.org>
```

The key fingerprint for oracle_vbox.asc is

```
7B0F AB3A 13B9 0743 5925  D9C9 5442 2A4B 98AB 5139
Oracle Corporation (VirtualBox archive signing key) <info@virtualbox.org>
```

To install VirtualBox, do

```
$ sudo apt-get update
$ sudo apt-get install virtualbox-6.1
```

Replace virtualbox-6.1 by virtualbox-6.0 or virtualbox-5.2 to install the latest VirtualBox 6.0 or 5.2 build.

What to do when experiencing The following signatures were invalid: BADSIG ... when refreshing the packages from the repository?

# sudo -s -H
# apt-get clean
# rm /var/lib/apt/lists/*
# rm /var/lib/apt/lists/partial/*
# apt-get clean
# apt-get update
