
This repository contains configuration files for building a 
Docker (http://docker.io) image for the Subsonic media streamer.

## Noteworthy

* Subsonic 6.0 (http://www.subsonic.org)
* uses jeanblanchard/docker-tomcat with Alpine Linux
* compiled to a 266 MB image instead of 484 MB


## Build your own image

```shell
$ docker build -t <your-name>/docker-subsonic .
```

## Get a pre-built image

A current image is available as a trusted build from the Docker index:

```shell
$ docker pull mbirth/subsonic
```

The repository page is at
https://hub.docker.com/r/mbirth/subsonic/


## Run a container with this image

```shell
$ docker run \
  --detach \
  --publish 8080:8080 \
  --volume "/wherever/your/music/is:/opt/music/:ro" \
  <your-name>/subsonic

```
