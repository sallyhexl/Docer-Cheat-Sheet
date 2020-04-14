# Sally's Docker Cheat Sheet

**Want to improve this cheat sheet?  See the [Contributing](#contributing) section!**

## Table of Contents

* [Why Docker](#why-docker)
* [Installation](#installation)
* [Install Docker Compose](#install-docker-compose)
* [Container](#container)
* [Contributing](#contributing)

## Why Docker

"With Docker, developers can build any app in any language using any toolchain. “Dockerized” apps are completely portable and can run anywhere - colleagues’ OS X and Windows laptops, QA servers running Ubuntu in the cloud, and production data center VMs running Red Hat.

Developers can get going quickly by starting with one of the 13,000+ apps available on Docker Hub. Docker manages and tracks changes and dependencies, making it easier for sysadmins to understand how the apps that developers build work. And with Docker Hub, developers can automate their build pipeline and share artifacts with collaborators through public or private repositories.

Docker helps developers build and ship higher-quality applications, faster." -- [What is Docker](https://www.docker.com/what-docker#copy1)


## Installation

### Connect to your server first
### Linux

Quick and easy install script provided by Docker:

```
wget -qO- https://get.docker.com/ | sh
```

### Check Version

It is very important that you always know the current version of Docker you are currently running on at any point in time. This is very helpful because you get to know what features are compatible with what you have running. This is also important because you know what containers to run from the docker store when you are trying to get template containers. That said let see how to know which version of docker we have running currently.

* [`docker version`](https://docs.docker.com/engine/reference/commandline/version/) shows which version of docker you have running.

Get the server version:

```
$ docker --version

```
## Install Docker Compose
### Linux

Quick and easy install script provided by Docker:

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
### Change Mod

```
sudo chmod +x /usr/local/bin/docker-compose
```
## Container

### Connect to your server first
### Get the docker

```
$ mkdir -p ~/html
$ docker run --name nginx -p 9091:80 -d -v ~/html:/usr/share/nginx/html nginx:1.17
$ docker ps -a
```
### List all the containers and their ID
```
$ docker container ls -a
```
### Stop the container
```
$ docker container stop 02704da5f7d1 (container ID)
```
### Delete the container
```
$ docker container rm 02704da5f7d1
```
## Contributing

Here's how to contribute to this cheat sheet.

### Open README.md

Click [README.md](https://github.com/wsargent/docker-cheat-sheet/blob/master/README.md) <-- this link




