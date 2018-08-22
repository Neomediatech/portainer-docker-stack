# Portainer Docker Stack
Docker compose file from the VERY AMAZING work of https://portainer.io crazy developers!
From their home page: "Portainer is an open-source lightweight management ui which allows you to easily manage your docker hosts or swarm cluster".

This docker-compose.yml file is customized for our needs. Original file is from portainer.io repository (https://portainer.readthedocs.io/en/stable/deployment.html#inside-a-swarm-cluster).

## Requirements
* Docker initialized as swarm :

`docker swarm init`
* Directory /srv/data/docker/containers/portainer/data created :

`mkdir -p /srv/data/docker/containers/portainer/data created`
* We use /srv/data/docker/var instead of /var/lib/docker, then keep attention on paths in this file

## Usage
* curl -L https://raw.githubusercontent.com/Neomediatech/portainer-docker-stack/master/docker-compose.yml -o portainer-agent-stack.yml
* docker stack deploy --compose-file=portainer-agent-stack.yml Portainer
* access your Portainer stack just deployed with a browser to http://ip-of-your-docker-host:9000
