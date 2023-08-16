By [swiftstack](https://hub.docker.com/u/swiftstack) • Updated 8 months ago

# pico swiftstack

`pico swiftstack` is a containerized instance of SwiftStack cloud storage engine. it is running the same version of Swift, S3 API and authentication found in the commercial distribution of SwiftStack. This Docker container is designed for developers working on integration / testing with AWS S3 or Swift APIs. pico swiftstack may also be used when integrating with a CI/CD system.

## Options

- To run pico swiftstack with HTTPS (TLS) access, map internal port `8443` to the port you wish to use and add `--env HTTPS="true"` in the docker run command. See examples below.
    - note: when HTTPS is turned on, you cannot use non-TLS access (HTTP).

## Getting Started

1.  **Download Docker:** For example, Docker Desktop: https://www.docker.com/products/docker-desktop or other options: https://docs.docker.com/install/overview/
2.  **Run:** 

```
docker run -d --rm -p 8080:8080 --hostname="picoswiftstack" --name="picoswiftstack" swiftstack/picoswiftstack
```

5.  **View Credentials:** `docker exec picoswiftstack get_auth`

to run pico swiftstack with HTTPS (TLS) access, **Run:** `docker run -d --rm -p 8443:8443 --env HTTPS="true" --hostname="picoswiftstack" --name="picoswiftstack" swiftstack/picoswiftstack`

## Options

you can run the latest pico swiftstack with the following docker run command:

```
$ docker run -d --rm -p <your local port mapping>:8080 --hostname="YOUR_HOSTNAME_FOR_CONTAINER" --name="YOUR_CONTAINER_NAME" swiftstack/picoswiftstack:latest
```

to run the latest pico swiftstack with HTTPS (TLS) access, **Run:** `docker run -d --rm -p <your local port mapping>:8443 --env HTTPS="true" --hostname="YOUR_HOSTNAME_FOR_CONTAINER" --name="YOUR_CONTAINER_NAME" swiftstack/picoswiftstack:latest`

To run a specific version of `pico swiftstack` (corresponding to the same version of SwiftStack) run:

```
$ docker run -d --rm -p <your local port mapping>:8080 --hostname="YOUR_HOSTNAME_FOR_CONTAINER" --name="YOUR_CONTAINER_NAME" swiftstack/picoswiftstack:<desired version>
```

To run a specific version of `pico swiftstack` (corresponding to the same version of SwiftStack) with HTTPS (TLS) access, **Run:** `docker run -d --rm -p <your local port mapping>:8443 --env HTTPS="true" --hostname="YOUR_HOSTNAME_FOR_CONTAINER" --name="YOUR_CONTAINER_NAME" swiftstack/picoswiftstack:latest`

Get endpoint information: A user account will be created when you do `docker run` and you can use the command as below to get your SwiftStack auth and s3 authentication.

```
$ docker exec YOUR_CONTAINER_NAME get_auth
```

```
======================= CLUSTER AUTHENTICATION =======================
Swift API Auth: http://127.0.0.1:8080/auth/v1.0 or http://<your VM IP>:<your exposed port>/auth/v1.0
SwiftStack Auth Username: test
SwiftStack Auth Password: test
S3 API URL: http://127.0.0.1 or http://<your VM ip>
S3 API Region: us-east-1
S3 Access Key: test
S3 Secret Key: 65909e932bf2d27e7b289c05cdb084c4
======================================================================
```

The version tag is SwiftStack version e.g. 6.21.0.0 - You can check SwiftStack release notes find the corresponding Swift version e.g. 2.21.0.2

- https://www.swiftstack.com/docs/admin/release.html
- https://github.com/openstack/swift/releases

## Feedback

Please contact [pico@swiftstack.com](mailto:pico@swiftstack.com) for feedback or questions.

Docker Pull Command

Owner

[<img width="40" height="40" src="../../_resources/02c731f09341dd2b2ae3fd2043d509f3_a962f2f46853406cb.png"/>swiftstack](https://hub.docker.com/u/swiftstack)

Why Docker

[Overview](https://www.docker.com/why-docker)[What is a Container](https://www.docker.com/resources/what-container)

Products

[Product Overview](https://www.docker.com/products)

Product Offerings

[Docker Desktop](https://www.docker.com/products/docker-desktop)[Docker Hub](https://www.docker.com/products/docker-hub)

Features

[Container Runtime](https://www.docker.com/products/container-runtime)[Developer Tools](https://www.docker.com/products/developer-tools)[Docker App](https://www.docker.com/products/docker-app)[Kubernetes](https://www.docker.com/products/kubernetes)

Developers

[Getting Started](https://docs.docker.com/get-started/)[Play with Docker](https://www.docker.com/play-with-docker)[Community](https://www.docker.com/docker-community)[Open Source](https://www.docker.com/open-source)[Docs](https://docs.docker.com/)[Hub Release Notes](https://docs.docker.com/docker-hub/release-notes/)

Company

[About Us](https://www.docker.com/company)[Resources](https://www.docker.com/resources)[Blog](https://www.docker.com/blog/)[Customers](https://www.docker.com/customers)[Partners](https://www.docker.com/partners)[Newsroom](https://www.docker.com/company/newsroom)[Events and Webinars](https://www.docker.com/events-and-webinars)[Careers](https://www.docker.com/careers)[Contact Us](https://www.docker.com/company/contact)

© 2021 Docker Inc. All rights reserved | [Terms of Service](https://www.docker.com/legal/docker-terms-service) | [Privacy](https://www.docker.com/legal/privacy) | [Legal](https://www.docker.com/legal)