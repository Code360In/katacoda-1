## Start and setup Jenkins

Create a [bridge network](https://docs.docker.com/network/bridge/) in Docker using the following [docker network create](https://docs.docker.com/engine/reference/commandline/network_create/) command:
> `docker network create jenkins`{{execute}}

Create the following volumes  to share the Docker client TLS certificates needed to connect to the Docker daemon and persist the Jenkins data using the following [docker volume create](https://docs.docker.com/engine/reference/commandline/volume_create/) commands:
> `docker volume create jenkins-docker-certs`{{execute}}
>
> `docker volume create jenkins-data`{{execute}}

In order to execute Docker commands inside Jenkins nodes, download and run the **docker:dind** Docker image. Specify the location of your shared folder (e.g. d:\shared).
