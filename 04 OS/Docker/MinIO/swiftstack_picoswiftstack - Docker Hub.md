# pico swiftstack

`pico swiftstack` is a containerized instance of SwiftStack cloud storage engine. it is running the same version of Swift, S3 API and authentication found in the commercial distribution of SwiftStack. This Docker container is designed for developers working on integration / testing with AWS S3 or Swift APIs. pico swiftstack may also be used when integrating with a CI/CD system.

## Options

- To run pico swiftstack with HTTPS (TLS) access, map internal port `8443` to the port you wish to use and add `--env HTTPS="true"` in the docker run command. See examples below.
    - note: when HTTPS is turned on, you cannot use non-TLS access (HTTP).

## Getting Started

1.  **Download Docker:** For example, Docker Desktop: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop) or other options: [https://docs.docker.com/install/overview/](https://docs.docker.com/install/overview/)
2.  **Run:** `docker run -d --rm -p 8080:8080 --hostname="picoswiftstack" --name="picoswiftstack" swiftstack/picoswiftstack`
3.  **View Credentials:** `docker exec picoswiftstack get_auth`

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

- [https://www.swiftstack.com/docs/admin/release.html](https://www.swiftstack.com/docs/admin/release.html)
- [https://github.com/openstack/swift/releases](https://github.com/openstack/swift/releases)