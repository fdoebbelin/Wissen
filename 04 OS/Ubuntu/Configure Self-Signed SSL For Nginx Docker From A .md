## Build an Nginx Docker Image With Alpine And Secure It With A Self-Signed SSL Certificate With OpenSSL

- Creating and configuring a Docker container from scratch with Alpine
- Creating a new Self-Signed Certificate
- Trusting the certificate with our local computer
- Creating a Dockerfile with exchangeable SSL certificates
- Setting up GitHub with automatic Docker Hub builds

You just need [Docker](https://hub.docker.com/editions/community/docker-ce-desktop-mac) for this.

- Docker CE `18.09.2`
- Mac OS Mojave or Equivalent

Pure and simple, security. There’s a bunch of other stuff as well, but mainly security.

To start, we’re going to use [Alpine](https://www.alpinelinux.org/), because it’s the smallest footprint, and can be a good base for security as well. The reason is because there are less dependencies, which mean less chances of exploitation.

We’ll expose port `443` to start because it’s the default port for https.

<a id="f68d"></a>docker run -it -p 80:80 -p 443:443 --name nginx-alpine-ssl alpine /bin/sh;


![](_resources/1_0ZWycZ0prb9eDyr_YLbMIQ_be0690c6ff074a3c9fb179244.png)

Docker Run

Let’s install `nginx` now:

<a id="1e89"></a>apk add nginx;

Make the directory that’s needed for nginx:

<a id="8729"></a>mkdir /run/nginx/;

Run nginx:

<a id="64d6"></a>nginx;

Testing the server is running with `curl`

<a id="d7eb"></a>apk add curl;  
curl localhost;<a id="a085"></a>\# Expected output  
\# &lt;html&gt;  
\# &lt;head&gt;&lt;title&gt;404 Not Found&lt;/title&gt;&lt;/head&gt;  
\# &lt;body&gt;  
\# &lt;center&gt;&lt;h1&gt;404 Not Found&lt;/h1&gt;&lt;/center&gt;  
\# &lt;hr&gt;&lt;center&gt;nginx&lt;/center&gt;  
\# &lt;/body&gt;  
\# &lt;/html&gt;


![](_resources/1_QqGSTKJZRCWT8-JjuJQJtQ_e8e4121950ae4fc788a47e2cf.png)

Docker Install Nginx & Curl

It will show `404` because there is no html file and no configuration setup for `nginx` to point to a root directory to load files from.

Looking at the `default.conf` nginx file:

<a id="6f97"></a>apk add nano;  
nano /etc/nginx/conf.d/default.conf

Change it to the following, save and exit:

**File:** `/etc/nginx/conf.d/default.conf`

<a id="ccb2"></a>server {  
        listen 80 default_server;  
        listen \[::\]:80 default_server; <a id="4cd9"></a>**\# New root location**  
        location / {  
 **root /var/www/localhost/htdocs;**   
 **# return 404;**  
        } <a id="439b"></a># You may need this to prevent return 404 recursion.  
        location = /404.html {  
                internal;  
        }  
}


![](_resources/1_zd7DC1-GC15GTc6HgxD5lg_75ca42f463d142429f310c1ca.png)

Modifying nginx default.conf

Restart `nginx`:

<a id="0bc7"></a>nginx -s reload;

Create an html in the `htdocs` folder:

<a id="8397"></a>echo "&lt;h1&gt;Hello world!&lt;/h1&gt;" > /var/www/localhost/htdocs/index.html;

Test that it’s working with `curl`:

<a id="8a4e"></a>curl localhost;<a id="0dab"></a>\# Expected output  
\# &lt;h1&gt;Hello world!&lt;/h1&gt;


![](_resources/1_h2LilJxCmE2syYm0e1KMnQ_9e472bb299504f6e9b03d61e3.png)

http://localhost

Next we need to use OpenSSL to generate our key and certificate files.

<a id="e6e3"></a>apk add openssl;

Create our new `key` and `crt` files:

<a id="cd7b"></a>openssl req -x509 -nodes -days 365 -subj "/C=CA/ST=QC/O=Company, Inc./CN=mydomain.com" -addext "subjectAltName=DNS:mydomain.com" -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt;<a id="44de"></a>\# Expected Output  
\# Generating a RSA private key  
\# .......................................+++++  
\# ....+++++  
\# writing new private key to '/etc/ssl/private/nginx-selfsigned.key'  
\# -----


![](_resources/1_fIZX0Ti7OM0TIU1iYsSUcg_2fb5b4fe71a945548a743c578.png)

OpenSSL generating new key and crt files

## What Each Options Means

To give some context as to what we’re doing in out `openssl` options:

- `**req**` — to specify we want to use `-x509`
- `**-x509**` — to specify we want to create a self-signed certificate instead of generating a certificate signing request.
- `**-nodes**` — makes it so that we skip the option to secure our certificate with a passphrase, so that nginx can read it.
- `**-days 365**` — specifies how long the certificate would be valid for, which is 365 days.
- `**-subj “/C=CA/ST=QC/O=Company, Inc./CN=mydomain.com"**` — this allows us to specify subject without filling in prompts. `/C` for country, `/ST` for state, `/O` for organization, and `/CN` for common name.
- `**-addext “subjectAltName=DNS:mydomain.com"**` — which adds additional attributes to our certificate which is needed to make it a valid certificate seen by both our browser and local machine.
- `**-newrsa rsa:2048**` — specifies that we want to generate both a new certificate and a new key with an RSA key of 2048 bits.
- `**-keyout /etc/.../yourfile.key**` — specifies the location of the output `.key` file.
- `**-out /etc/.../yourfile.crt**` — specifies the location of the output `.crt` file.

We now need to associate our SSL certificate to our `default.conf` nginx file.

**File:** `/etc/nginx/conf.d/default.conf`

<a id="03bd"></a>server {  
        listen 80 default_server;  
        listen \[::\]:80 default_server;  
  **listen 443 ssl http2 default_server;**  
 **listen \[::\]:443 ssl http2 default_server;  
        ssl_certificate /etc/ssl/certs/nginx-selfsigned.crt;**  
 **ssl\_certificate\_key /etc/ssl/private/nginx-selfsigned.key;** <a id="2549"></a>\# New root location  
        location / {  
                root /var/www/localhost/htdocs;   
                # return 404;  
        } <a id="7de4"></a># You may need this to prevent return 404 recursion.  
        location = /404.html {  
                internal;  
        }  
}


![](_resources/1_9CTeETqFXiFUtv63kx2otA_4828d03ea4c243cab734f9668.png)

New nginx configuration with SSL enabled & certificates

Save the file, check the file is correct with:

<a id="76a5"></a>nginx -t;<a id="66d1"></a>\# Expected Output  
\# nginx: the configuration file /etc/nginx/nginx.conf syntax is ok  
\# nginx: configuration file /etc/nginx/nginx.conf test is successful

**Don’t forget** to now reload `nginx`:

<a id="f58c"></a>nginx -s reload;

Let’s test https with `curl`:

<a id="f6e8"></a>curl [https://localhost](https://localhost/);<a id="8bee"></a>\# Expected Output  
\# curl: (60) SSL certificate problem: self signed certificate  
\# More details here: [https://curl.haxx.se/docs/sslcerts.html](https://curl.haxx.se/docs/sslcerts.html)<a id="90ab"></a>\# curl failed to verify the legitimacy of the server and therefore could not establish a secure connection to it. To learn more about this situation and how to fix it, please visit the web page mentioned above.

This happens because our SSL certificate is self-signed and not really a legitimate certificate. To get around this, just to see if https is working, run:

<a id="c346"></a>curl [https://localhost](https://localhost/) --insecure;<a id="a966"></a>\# Expected Output  
\# &lt;h1&gt;Hello world!&lt;/h1&gt;


![](_resources/1_yW2jymqJipUVAG-9H8zcBw_51f7caa87c5848eab1e5e2a1d.png)

Browser Not Trusting Certificate

To get around this temporarily in our browser, just click **“Help me understand”** in `**Opera**` or click “**Advanced”** in `**Chrome**`.


![](_resources/1_kXfuVoPakOwlHLQeXjpWuQ_ca464b6dcde04963aa4184ae2.png)

Temporarily getting around unsafe (self-signed) SSL certificate in Opera


![](_resources/1_3-_4X8dk3dMguER6Q1-59Q_9ca90ddf15584cfb9e444ed5e.png)

Temporarily getting around unsafe (self-signed) SSL certificate in Chrome

Next we’ll configure out domain `mydomain.com` to point to `localhost` or more specifically `127.0.0.1`. You’ll need root access for this, with you password, by modifying the `hosts` file. Make sure to open a new `**Terminal**` tab or window, and run:

<a id="59ac"></a>sudo nano /etc/hosts;

**File:** `/etc/hosts`

<a id="1f9a"></a>##  
\# Host Database  
#  
\# localhost is used to configure the loopback interface  
\# when the system is booting.  Do not change this entry.  
##  
127.0.0.1       localhost  
255.255.255.255 broadcasthost  
::1             localhost  
127.0.0.1       mydomain.com


![](_resources/1_K78Qrb5g4rhyhiyRNP3IAA_943d3a38f08e486283c67723d.png)

Modified hosts file

If we open up our browser, we’ll see the following when we visit [**https://mydomain.com**.](https://mydomain.com./)


![](_resources/1_jrEmFZPMdmH2AtzW82G6rQ_f4e5f061210d45e5921bc96a8.png)

[https://mydomain.com](https://mydomain.com/)

We could just get around this temporarily by proceeding to it being unsafe, but we’ll take the next steps to make ***mydomain.com*** trusted by our local computer.

In order for us to trust the domain, we need to copy and place the `crt` (certificate) in our `**Keychain Access**`.

First we need to get a copy of that certificate in the Docker container. In a new `**Terminal**` window or tab, run:

<a id="c9a8"></a>docker cp nginx-alpine-ssl:/etc/ssl/certs/nginx-selfsigned.crt ~/Desktop;


![](_resources/1__VQEDbxfYWjbSjoTeT5tKA_6338359682cb4f08bceedf9ff.png)

Copying Docker certificate to local computer

Open up you `**Keychain Access**` app.


![](_resources/1_8-jyLXasCR355NsyGBl6ag_f60d5c9d4b554daf85ee5d8af.png)

Where to find Mac OS Keychain Access App

When the `**Keychain Access**` app loads up, on the left side bar, select **Certificates**. Drag the newly copied `nginx-selfsigned.crt` file from the Desktop to `**Keychain Access**`.


![](_resources/1_Ds439QZ7vGjtqQKZJ2r40w_3636a1a466ae496796367b35e.gif)

Drag new certificate to Keychain Access app

Next we need to make sure the certificate is trust by our computer. ***Double click*** on the newly added certificate, click the ***Trust*** dropdown and set ***“When using this certificate”*** to ***Always Trust***.


![](_resources/1_t78_3Mn5Y7W9-erq9unrdw_04b9a3d87a814955af2a4bca3.png)

Always trust mydomain.com

Close the window the ***mydomain.com*** certificate window. You will be prompted to enter your computer password to validate and confirm the change.

Now open up [***https://mydomain.com****.*](https://mydomain.com./)


![](_resources/1_hLAelsh23OaDz46UU4mWMg_c843e92b08e347379f16b953a.png)

[https://mydomain](https://mydomain/).com working

You’ll see the domain is now working with https and it displays a green 🔒icon.

Next we’ll create a Docker file with some configuration files and an `entrypoint.sh` script.

For this we’ll create a new folder and copy our `key` and `crt` files to a newly created `config` folder, as long with our modified `**nginx**` configuration `default.conf` file.

## Creating our new folders:

<a id="ddea"></a>mkdir ~/Documents/nginx-alpine-ssl;  
mkdir ~/Documents/nginx-alpine-ssl/config;

## Copying our files:

<a id="d33b"></a>\# certificate  
docker cp nginx-alpine-ssl:/etc/ssl/certs/nginx-selfsigned.crt ~/Documents/nginx-alpine-ssl/config;<a id="4658"></a>\# private key  
docker cp nginx-alpine-ssl:/etc/ssl/private/nginx-selfsigned.key ~/Documents/nginx-alpine-ssl/config;<a id="6072"></a>\# nginx configuration file  
docker cp nginx-alpine-ssl:/etc/nginx/conf.d/default.conf ~/Documents/nginx-alpine-ssl/config;

## Creating our Dockerfile:

<a id="7196"></a>touch ~/Documents/nginx-alpine-ssl/Dockerfile;

**File:** `/Dockerfile`

<a id="c27c"></a>\# BASE  
FROM alpine<a id="4661"></a>\# RUN  
RUN apk add nginx; \  
    mkdir /run/nginx/; \  
    echo "&lt;h1&gt;Hello world!&lt;/h1&gt;" > /var/www/localhost/htdocs/index.html;<a id="32d4"></a>\# CONFIGUTATIONS  
\# nginx configuration  
ADD $PWD/config/default.conf /etc/nginx/conf.d/default.conf<a id="6668"></a>\# keys and certs  
ADD $PWD/config/*.key /etc/ssl/private/  
ADD $PWD/config/*.crt /etc/ssl/certs/<a id="1fed"></a>WORKDIR /var/www/localhost/htdocs<a id="940d"></a>\# ENTRYPOINT  
COPY $PWD/config/entrypoint.sh /usr/local/bin<a id="1374"></a>RUN chmod +x /usr/local/bin/entrypoint.sh<a id="1de9"></a>ENTRYPOINT \["/bin/sh", "/usr/local/bin/entrypoint.sh"\]<a id="9c64"></a>\# EXPOSE PORTS  
EXPOSE 80<a id="3a28"></a>EXPOSE 443<a id="0393"></a>\# RUN COMMAND  
CMD \["/bin/sh", "-c", "nginx -g 'daemon off;'; nginx -s reload;"\]

## Creating Our Entrypoint Script:

This will be our script that will run at run time and we want to add some environment variables to add the ability to change the certificate and key out.

<a id="53f1"></a>touch ~/Documents/nginx-alpine-ssl/config/entrypoint.sh

**File:** `/config/entrypoint.sh`

<a id="8ca5"></a>\# Main shell script that is run at the time that the Docker image is run<a id="b418"></a>\# Go to default.conf directory  
cd /etc/nginx/conf.d;<a id="8e8a"></a>\# ENV VARS  
\# A list of environment variables that are passed to the container and their defaults<a id="ad3d"></a>\# CRT - double check that the file exists  
export CRT="${CRT:=nginx-selfsigned.crt}";  
if \[ -f "/etc/ssl/certs/$CRT" \]  
then  
    # set crt file in the default.conf file  
    sed -i "/ssl\_certificate \\//c\\\\\tssl\_certificate \\/etc\\/ssl\\/certs\\/$CRT;" default.conf;  
fi<a id="8b72"></a>\# KEY - double check that the file exists  
export KEY="${KEY:=nginx-selfsigned.key}";  
if \[ -f "/etc/ssl/private/$KEY" \]  
then  
    # set key file in the default.conf file  
    sed -i "/ssl\_certificate\_key \\//c\\\\\tssl\_certificate\_key \\/etc\\/ssl\\/private\\/$KEY;" default.conf;  
fi<a id="495f"></a>\# Needed to make sure nginx is running after the commands are run  
nginx -g 'daemon off;'; nginx -s reload;

## Making A Build

To test the Dockerfile, let’s make a build by running the following in the root directory of the project:

<a id="3552"></a>docker build . -t nginxssltest;

## Running Our Container

Let’s run our container and then do a `curl` test:

<a id="9a8a"></a>docker run -it -d -p 80:80 -p 443:443 --name test nginxssltest;<a id="7173"></a>curl localhost;<a id="1a5f"></a>\# Expected output  
\# &lt;h1&gt;Hello world!&lt;/h1&gt;<a id="da6c"></a>curl [https://localhost](https://localhost/) --insecure;<a id="24a2"></a>\# Expected output  
\# &lt;h1&gt;Hello world!&lt;/h1&gt;

If we open up our browser, with our certificate trusted by our computer, we can see it works:

[https://mydomain.com](https://mydomain.com/) Working

Now that we see that it’s working, let’s test another domain with different generated keys.

First, let us modify out `hosts` file to add a new domain to it.

<a id="16e7"></a>sudo nano /etc/hosts;

**File:** `/etc/hosts`

<a id="f263"></a>##  
\# Host Database  
#  
\# localhost is used to configure the loopback interface  
\# when the system is booting.  Do not change this entry.  
##  
127.0.0.1 localhost  
255.255.255.255 broadcasthost  
::1             localhost  
127.0.0.1 mydomain.com  
127.0.0.1 newdomain.com

/etc/hosts

## Generate New Certificate & Key

Next, we’ll generate new `crt` and `key` files in a new folder called `certkey`. To do this though, Mac OS doesn’t support `-addext` and instead of going the route of trying to reconfiguring our local `openssl.conf` file, we’ll just use an alpine docker image as a one time use to generate the keys we need.

<a id="4a2f"></a>mkdir ~/Documents/nginx-alpine-ssl/certkey;<a id="94dd"></a>cd ~/Documents/nginx-alpine-ssl;<a id="4f40"></a>\# --rm will remove the container after it's run  
docker run --rm **-v $PWD/certkey:/usr/share** alpine /bin/sh -c "apk add openssl; openssl req -x509 -nodes -days 365 -subj \\"/C=CA/ST=QC/O=Company, Inc./CN=**newdomain.com**\\" -addext \\"subjectAltName=DNS:**newdomain.com**\\" -newkey rsa:2048 -keyout **/usr/share/new-selfsigned.key** -out **/usr/share/new-selfsigned.crt;**"

## Add Our Certificate To Keychain Access

Drag our newly created `new-selfsigned.crt` to the`**Keychain Access**` app.

Running Container With New Keys

Now we have our new `crt` and `key` files located in our new `certkey` folder. With them, we can use them with our new environment variables defined by our `entrypoint.sh` file:

<a id="e9dd"></a>**\# -v is mounting both to the certs and private folder in docker  
\# -e CRT=name of certificate  
\# -e KEY=name of key**<a id="359c"></a>docker run -it -d -v $PWD/certkey:/etc/ssl/private/ -v $PWD/certkey:/etc/ssl/certs/ -e CRT=new-selfsigned.crt -e KEY=new-selfsigned.key -p 80:80 -p 443:443 --name newssl nginxssltest;

If we open our browser now to [**https://newdomain.com**,](https://newdomain.com,/) we’ll see:

[https://newdomain.com](https://newdomain.com/) working with the new certificates

This next part is to bring it all together with a GitHub repository and a connected Docker Hub repository that creates automatic builds for us to use.

## Connecting With GitHub

In the root of our project, let’s get our repo setup:

<a id="7f9c"></a>\# create your new repo<a id="471e"></a>curl -u ***{github-username}*** \  
--url https://api.github.com/user/repos \  
-d "{\\"name\\":\\"nginx-alpine-ssl\\"}";<a id="f516"></a>\# if you have two-factor authentication use  
\# curl -u ***{github-username}*** \  
\# --url https://api.github.com/user/repos \  
\# --header 'x-github-otp: ***{your-code}***' \  
\# -d "{\\"name\\":\\"nginx-alpine-ssl\\"}";<a id="f713"></a>\# initiate git  
git init;<a id="daf5"></a>\# link new repo  
git remote add origin "https://github.com/***{your-github-username}***/nginx-alpine-ssl.git"

## Creating Documentation Files

<a id="9387"></a>\# create a .gitignore file  
echo ".DS_Store\\ncertkey" > .gitignore;<a id="3302"></a>\# create a README.md file  
echo "# Nginx Alpine SSL\\n\\nThis will create a basic nginx ssl enabled http server that runs on alpine.\\n\\n## Requirements\\n\\n- Docker CE\\n\\n## Options\\n\\n\\`-e CRT={your-cert-name.crt}\\` - allows you to specify your own \\\`crt\\\` file  (note there is a default for mydomain.com).\\n\\n\\`-e KEY={your-private-key.key}\\` - allows you to specify your own \\\`key\\\` file (note there is a default for mydomain.com).\\n\\n## Generate Your Own Self-Signed SSL\\n\\n\\`\\`\\`bash\\ndocker run --rm -v **\**$PWD/local/path:/usr/share alpine /bin/sh -c \\"apk add openssl; openssl req -x509 -nodes -days 365 -subj \\\\\"/C=CA/ST=QC/O=Company, Inc./CN=yourdomain.com\\\\\" -addext \\\\\"subjectAltName=DNS:yourdomain.com\\\\\" -newkey rsa:2048 -keyout /usr/share/your-key-name.key -out /usr/share/your-cert-name.crt;\\"\\n\\`\\`\\`\\n\\n## Example Run\\n\\n\\`\\`\\\`bash\\ndocker run -it -d -v \\$PWD/local/path:/etc/ssl/private/ -v \\$PWD/local/path:/etc/ssl/certs/ -e CRT=your-cert-name.crt -e KEY=your-private-key.key -p 80:80 -p 443:443 --name container-name {docker-hub-user}/{docker-hub-repo};\\n\\\`\\`\\`" > README.md;

## Committing + Pushing Our Code

<a id="8a07"></a>git add .;  
git commit -m "INIT: Initial commit."  
git push origin master;

## Creating A New Docker Hub Repository

We’ll need to create a new Docker Hub repository and make sure it’s connected to our GitHub repository.

New Docker Hub Repository

Link to GitHub

Find our GitHub repository and keep to these basic settings.

Docker Hub Automatic Build Configurations

Click **Save** and the automatic building will begin.

Docker Image Building

**NOTE:** You might need to refresh the page to see the latest build status.

## Running Your New Docker Image

Once the Docker image is built, you can pull and run your new image. All you need to do is run:

<a id="2362"></a>docker run -it -d -p 80:80 -p 443:443 --name nginxssl {docker-hub-username}:{docker-hub-repo};

This image works well even for valid certificates, so you could validate a new certificate with Let’s Encrypt and pass that along as an environment variable with a mounted folder. Additionally you could take advantage of [**turning your nginx Docker container into a reverse proxy**](https://medium.com/@codingwithmanny/create-an-nginx-reverse-proxy-with-docker-a1c0aa9078f1) and have multiple containers under one SSL certificate.

If you got value from this, and/or if you think this can be improved, please let me know in the comments.

Please share it on twitter 🐦 or other social media platforms. Thanks again for reading. 🙏

Please also follow me on **twitter**: [@codingwithmanny](https://twitter.com/codingwithmanny) and **instagram** at [@codingwithmanny](https://www.instagram.com/codingwithmanny/).
