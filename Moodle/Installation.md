---
source: https://docs.moodle.org/311/en/Installation_guide_for_Windows_using_WSL_(Windows_Subsystem_for_Linux)
---


```sh
sudo apt update && sudo apt upgrade
sudo apt install apache2 php libapache2-mod-php
sudo apt install mariadb-server
sudo service mariadb start
```


secure the root password of your database. Again write it down! Everything else can be accepted at default value.


```sh
sudo mysql_secure_installation
mysql -u root -proot
```


Install the modules required for Moodle.


```sh
sudo apt install graphviz aspell ghostscript clamav php-pspell php-curl php-gd php-intl php-mysql php-xml php-xmlrpc php-ldap php-zip php-soap php-mbstring
```

Restart Apache so that the modules are loaded correctly,

```sh
sudo service apache2 restart
sudo service apache2 status
sudo service mysql status
```

Use git to get the latest version of Moodle.


```sh
cd /opt
sudo git clone git://git.moodle.org/moodle.git
cd moodle
sudo git branch -a
...
remotes/origin/MOODLE_401_STABLE
remotes/origin/master

sudo git branch --track MOODLE_401_STABLE origin/MOODLE_401_STABLE
sudo git checkout MOODLE_401_STABLE

```

Put the Moodle code in the Apache webserver directory (/var/www/html), create the modledata directory, and set its permissions.

```sh
sudo cp -R /opt/moodle /var/www/html/
sudo mkdir /var/moodledata
sudo chown -R www-data /var/moodledata
sudo chmod -R 777 /var/moodledata
```

Set up the database. To use mysql, use the root password you set when securing the database. If you have a problem here, try restarting the mysql service. (sudo service mysql restart)

```sh
sudo mysql -u root -proot
```

Remember to change moodledude and passwordformoodledude

```sql
mysql> CREATE DATABASE moodle DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
mysql> create user 'admin'@'localhost' IDENTIFIED BY 'admin';
mysql> GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,CREATE TEMPORARY TABLES,DROP,INDEX,ALTER ON moodle.* TO 'admin'@'localhost';
mysql> quit;
```

Edit the php.ini file

```sh
sudo nano /etc/php/8.1/apache2/php.ini
```

Use `CTRL-W` to find the `max_input_vars`, remove the semicolon and change it to equal `5000`.

```
; How many GET/POST/COOKIE input variables may be accepted
max_input_vars = 5000
```

CTRL-O and CTRL-X saves the file, now restart Apache

```sh
sudo service apache2 restart
```

Services beim WSL-Boot starten

```sh
sudo nano /etc/wsl.conf
[boot]
command = service apache2 start; service cron start; service mysql start
```

Now go to (your IP address)/moodle on your browser and finish the install. If yio have forgotten your IP address use the command hostname -I. 
Database type is `mariadb`, data directory is `/var/moodledata` and you use the user name and password you changed from moodledude to connect to the database. Save the config file by entering:

```sh
sudo nano /var/www/html/moodle/config.php 
```

and pasting in the content from the `config.php` page and save (`CTRL-O, CTRL-X`)_ 
Other than a warning on "site not https", all requirements should be met.

Administrator-Login

```
http://localhost/moodle
fritz
#s3Kr3t#
```

Set up cron for housekeeping.


```sh
sudo crontab -u www-data -e
Select 1 to use nano. Enter this command, save and exit.
* * * * * /usr/bin/php  /var/www/html/moodle/admin/cli/cron.php >/dev/null
```


Plugins can be used to add new features to your Moodle installation. On your new Moodle, go to

```
Dashboard -> Site administration -> Plugins -> Install plugins
```

Install a plugin from the Moodle plugins directory.
Choose "`Moodle Benchmark`", "Install now" and your new Moodle site.
You will get a message _/var/www/html/moodle/report is not writable_. On your WSL window, enter this command.

```sh
sudo chmod 777 /var/www/html/moodle/report
```

Go back to Moodle to continue, confirm and continue. Don't forget to reset the permissions back so the directory is again not writable.

```sh
sudo chmod 755 /var/www/html/moodle/report
```

The benchmark report will now be under `Site administration -> Reports`

WSL is great for learning. If you have mastered these steps, move on to [Installing Moodle on a Ubuntu cloud server](https://docs.moodle.org/311/en/Installing_Moodle_on_a_Ubuntu_cloud_server "Installing Moodle on a Ubuntu cloud server")
