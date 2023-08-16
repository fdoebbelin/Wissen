Being a network administrator requires a deep knowledge about remote login protocols such as **rlogin**, **telnet** and **ssh**. The one I will discuss in this article is **ssh**, a secure remote protocol which is used to work remotely on other machines or transfer data between computers using [SCP (Secure Copy)](https://www.tecmint.com/scp-commands-examples/) command. But, what is **OpenSSH** and how to install it in your **Linux** distribution?

[![Install OpenSSH in Linux](_resources/Install-OpenSSH-in-Linux.gif)](https://www.tecmint.com/wp-content/uploads/2013/11/Install-OpenSSH-in-Linux.gif)

Install OpenSSH in Linux

### What is OpenSSH?

**OpenSSH** is a free open source set of computer tools used to provide secure and encrypted communication over a computer network by using the **ssh** protocol. Many people, new to computers and protocols, create a misconception about **OpenSSH**, they think it is a protocol, but it is not, it is a set of computer programs that use the **ssh protocol**.

**OpenSSH** is developed by the Open BSD group and it is released under **Simplified BSD License**. A main factor which has made possible for **OpenSSH** to be used so much among system administrators is its multi-platform capability and very useful nice features it has. The latest version is **OpenSSH 6.4** which has been released on **November 8, 2013**.

This version of **OpenSSH** comes with many new features and patches, so if you already use **OpenSSH** for administering your machines, I suggest you to do an upgrade.

### Why Use OpenSSH And Over Telnet Or Ftp?

The most important reason why should use **OpenSSH** tools over **ftp** and **telnet** is that all communications and user credentials using **OpenSSH** are encrypted, they are also protected from man in the middle attacks. If a third party tries to intercept your connection, **OpenSSH** detects it and informs you about that.

### What Are Some Of The OpenSSH Features?

1.  Secure Communication
2.  Strong Encryption (**3DES**, **Blowfish**, **AES**, **Arcfour**)
3.  **X11** Forwarding (encrypt **X** Window System traffic)
4.  Port Forwarding (encrypted channels for legacy protocols)
5.  Strong Authentication (**Public Key**, One-Time Password and Kerberos Authentication)
6.  Agent Forwarding (**Single-Sign-On**)
7.  Interoperability (Compliance with **SSH 1.3, 1.5**, and **2.0** protocol Standards)
8.  **SFTP** client and server support in both **SSH1** and **SSH2** protocols.
9.  **Kerberos** and **AFS Ticket Passing**
10. Data Compression

### Installation of OpenSSH in Linux

To install **OpenSSH**, open a terminal and run the following commands with superuser permissions.

#### On Ubuntu/Debian/Linux Mint

$ sudo apt-get install openssh-server openssh-client

#### On RHEL/Centos/Fedora

Type the following **yum** command to install openssh client and server.

\# yum -y install openssh-server openssh-clients

### Configuration of OpenSSH

It’s time to configure our **OpenSSH** behaviour through the **ssh config** file, but before editing the **/etc/ssh/sshd_config** file we need to backup a copy of it, so in case we make any mistake we have the original copy.

Open a terminal and run the following command to make a copy of the original sshd configuration file.

$ sudo cp /etc/ssh/sshd\_config  /etc/ssh/sshd\_config.original_copy

As you can see from the command I typed, I added the **original_copy suffix**, so every time I see this file I know it is an original copy of the sshd config file.

### How Do I Connect to OpenSSH

Before we go further, we need to verify if our **openssh** server is working or not. How to do that? You can try to connect to the **openssh** server from your **localhost** through your **openssh client** or do a **portscan** with **nmap**, but I like to use a small tool called **netcat**, also known as the **TCP**/**IP** Swiss army knife. I love working with this amazing tool on my machine, so let me show it to you.

\# nc -v -z 127.0.0.1 22

Referring to the **netcat** results, the ssh service is running on port **22** on my machine. Very good! What if we want to use another port, instead of **22**? We can do that by editing the sshd configuration file.

Set your **OpenSSH** to listen on **TCP** port **13** instead of the default TCP port **22**. Open the **sshd_config** file with your favourite text editor and change the port directive to **13**.

\# What ports, IPs and protocols we listen for
Port 13

Restart **OpenSSH** server so the changes in config file can take place by typing the following command and run **netcat** to verify if the port you set for listening is open or not.

$ sudo /etc/init.d/ssh restart

Should we verify is our openssh server is listening on port 13, or not?. This verification is necessary, so I am calling my lovely tool **netcat** to help me do the job.

\# nc -v -z 127.0.0.1 13

Do you like to make your openssh server display a nice login banner? You can do it by modifying the content of **/etc/issue.net** file and adding the following line inside the sshd configuration file.

Banner /etc/issue.net

### Conclusion

There are many things you can do with the **openssh** tools when it comes to the way you configure your **openssh server**, I can say that your imagination is the limit!.

Read Also: [5 Best Practices to Secure and Protect OpenSSH Server](https://www.tecmint.com/5-best-practices-to-secure-and-protect-ssh-server/)