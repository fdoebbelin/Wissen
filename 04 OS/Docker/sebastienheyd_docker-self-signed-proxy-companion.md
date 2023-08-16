**WARNING ! Self-signed certificates should only be used on local projects !**

self-signed-certificate-nginx-proxy-companion is a lightweight companion container for the [nginx-proxy](https://github.com/jwilder/nginx-proxy). It allows the creation of self-signed certificates automatically.

If you need to set Let's Encrypt certificates for production, see : [docker-letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion).

## <a id="user-content-features"></a>[](#features)Features

- Automatic creation self-signed certificates with a **20 years validity period** (!) using original [nginx-proxy](https://github.com/jwilder/nginx-proxy) container.
- Automatic creation of a certificate autority (CA) to trust your self-signed certificates

## <a id="user-content-usage"></a>[](#usage)Usage

To use it with original [nginx-proxy](https://github.com/jwilder/nginx-proxy) container you must declare 2 volumes :

- `/var/run/docker.sock` (read only) to access docker socket
- `/etc/nginx/certs` (writable) to create self-signed certificates

#### <a id="user-content-example"></a>[](#example)Example:

- First start nginx with the 2 volumes declared:

$ docker run -d -p 80:80 -p 443:443 \
    --name nginx-proxy \
    -v /var/run/docker.sock:/tmp/docker.sock:ro \
    -v /path/to/certs:/etc/nginx/certs:ro \
    -v /etc/nginx/vhost.d \
    jwilder/nginx-proxy

- Second start this container:

$ docker run -d \
    --name proxy-companion \
    -v /var/run/docker.sock:/var/run/docker.sock:ro \
    -v /path/to/certs:/etc/nginx/certs:rw \
    -e "NGINX\_PROXY\_CONTAINER=nginx-proxy"
    sebastienheyd/self-signed-proxy-companion

**Note** : by default `NGINX_PROXY_CONTAINER` = proxy, if your proxy container name is `proxy` you don't have to specify the name.

- Then start any proxied containers with an additional env var `SELF_SIGNED_HOST`

$ docker run -d \
    --name example-app \
    -e "VIRTUAL_HOST=example.com.localhost,www.example.com.localhost,mail.example.com.localhost" \
    -e "SELF\_SIGNED\_HOST=example.com.localhost" \
    tutum/apache-php

**Note** : in this example `SELF_SIGNED_HOST` value `example.com.localhost` will cover `*.example.com.localhost`, you don't have to add all FQDN. See [wildcard](https://github.com/jwilder/nginx-proxy#wildcard-certificates) documentation.

#### <a id="user-content-with-docker-compose-"></a>[](#with-docker-compose-)With docker-compose :

First start nginx and companion with the 2 volumes declared:

version: '2'

services:
    proxy:
        container_name: proxy
        restart: always
        image: jwilder/nginx-proxy
        ports:
            \- "80:80"
            \- "443:443"
        volumes:
            \- /var/run/docker.sock:/tmp/docker.sock:ro
            \- ./vhost.d:/etc/nginx/vhost.d
            \- ./certs:/etc/nginx/certs
        networks:
            \- proxy

    proxy-companion:        
        container_name: proxy-companion
        restart: always
        image: sebastienheyd/self-signed-proxy-companion
        volumes:
            \- /var/run/docker.sock:/var/run/docker.sock:ro
            \- ./certs:/etc/nginx/certs

networks:
    proxy:
        external: true

Then start any proxied containers with an additional env var `SELF_SIGNED_HOST`

version: '2'

services:
    app:
        container_name: example-app
        image: tutum/apache-php:latest
        environment:
            VIRTUAL_HOST: "example.com.localhost,www.example.com.localhost,mail.example.com.localhost"
            SELF\_SIGNED\_HOST: "example.com.localhost"
        networks:
            \- proxy

networks:
    proxy:
        external: true

**Note** : in this example `SELF_SIGNED_HOST` value `example.com.localhost` will cover `*.example.com.localhost`, you don't have to add all FQDN. See [wildcard](https://github.com/jwilder/nginx-proxy#wildcard-certificates) documentation.

## <a id="user-content-trust-self-signed-certificates"></a>[](#trust-self-signed-certificates)Trust self-signed certificates

This will avoid you to see the alert "your connection is not private".

At the first launch of companion a CA certificate is generated. You will find `ca.crt` in your `certs` folder, this is your CA certificate.

There are several ways to import a CA certificate, here are two of them.

##### <a id="user-content-chrome"></a>[](#chrome)Chrome

Go to : `chrome://settings/certificates`

Go to `Trusted Root Certification Authorities` and import `ca.crt`

##### <a id="user-content-firefox"></a>[](#firefox)Firefox

Go to `about:config#privacy`

On the bottom of the page, click on `View certificates`, select `Authorities` \> `Import` then browse to `ca.crt`.

Check `Trust the CA to identify websites`