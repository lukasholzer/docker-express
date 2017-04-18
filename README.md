# Docker Setup for NODE.js with NGINX

This is a bootstrap repository for a basic setup with [Docker](https://docs.docker.com/) for an Node.js powered Development environment with [express.js](http://expressjs.com/) and as Proxy Reverse a simple [NGINX](https://www.nginx.com/resources/wiki/) setup.


## Requirements

- [Docker](http://docker.com) Download the app for: [Mac OSX](https://download.docker.com/mac/stable/Docker.dmg) or [Windows 10 App](https://download.docker.com/win/stable/InstallDocker.msi)
- [Docker Compose](http://docs.docker.com/compose/) installation with [homebrew](https://brew.sh/index_de.html) `brew install docker-compose`





### Commands

A short list of useful commands for this Bootstrapping

- run: `docker-compose up`
- run in background: `docker-compose up -d`
- build: `docker-compose build`
- shutdown: `docker-compose down`
- list all images: `docker images -a`
- list all running images: `docker ps`

### stop all containers and delete all images on Mac

After this commands every image and container has to be pulled again and created.
Clean reset if the hard drive is messed up.

``` bash
docker stop $(docker ps -a -q)
docker rm -v $(docker ps -a -q)
docker rmi $(docker images -q)
```

## Maintainer

**Lukas Holzer**

* Email: <office@lukasholzer.com>
* Twitter: [@luka5c0m](https://twitter.com/luka5c0m)
* Web: [www.lukasholzer.com](http://www.lukasholzer.com)