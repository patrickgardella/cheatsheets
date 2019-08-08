---
title: Docker
keywords: cheatsheets
last_updated: August 2, 2019
tags: [cheatsheets containerization]
sidebar: cheatsheets_sidebar
permalink: cs_docker.html
folder: cheatsheets
---

## Terminology

Container: A container is used to execute an image.  See ``docker run``,
``docker-compose up``.

Image: A kind of snapshot of a computer system that can be run in a container.
Images are built from Dockerfiles.  See ``docker build``, ``docker-compose build``.

## Common commands

### Build an image

Build an image from Dockerfile in current directory:

```bash
    docker build -t imagetag .
```

### Start an image

Start a container from an image in interactive mode, run a command, and when the
command exits, stop the container without saving any changes:

```bash
    docker run --rm -it imagetag bash
```

## Cleanup

### Delete volumes

* [https://github.com/chadoe/docker-cleanup-volumes](https://github.com/chadoe/docker-cleanup-volumes) 

```bash
    docker volume rm $(docker volume ls -qf dangling=true)
    docker volume ls -qf dangling=true | xargs -r docker volume rm
```

### Delete networks

```bash
    docker network ls
    docker network ls | grep "bridge"
    docker network rm $(docker network ls | grep "bridge" | awk '/ / { print $1 }')
```

### Remove docker images

* [http://stackoverflow.com/questions/32723111/how-to-remove-old-and-unused-docker-images](http://stackoverflow.com/questions/32723111/how-to-remove-old-and-unused-docker-images)

```bash
    docker images
    docker rmi $(docker images --filter "dangling=true" -q --no-trunc)

    docker images | grep "none"
    docker rmi $(docker images | grep "none" | awk '/ / { print $3 }')
```

### Remove docker containers

* [http://stackoverflow.com/questions/32723111/how-to-remove-old-and-unused-docker-images](http://stackoverflow.com/questions/32723111/how-to-remove-old-and-unused-docker-images)

```bash
    docker ps
    docker ps -a
    docker rm $(docker ps -qa --no-trunc --filter "status=exited")
```

### Resize disk space for docker vm

```bash
    docker-machine create --driver virtualbox --virtualbox-disk-size "40000" default

```

## Networking

### Identify IP of the container

```bash
docker inspect -f "{{ .NetworkSettings.Networks.nat.IPAddress }}" myapp
```

## Common Problems

### Windows

If trying to run docker commands from Git Bash, it won't properly work with `${PWD}`. To deal with this, you have to set the environment variable:

```bash
MSYS_NO_PATHCONV=1 docker run -v $(pwd):/docs ...
```

or

```bash
MSYS_NO_PATHCONV=1 docker-compose up
```

