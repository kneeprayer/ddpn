## Synopsis
This repository has been created for **Docker** based Django development environment.

## Installation

1. Install Docker on your OS environment
  <https://docs.docker.com/engine/installation/>
2. `cd `**somewhere**
3. `mkdir `**somename** and `cd `**somename**
4. `git clone https://github.com/kneeprayer/ddpn.git`
5. `cp tmp.env .env` and fix .env file.
6. `chmod 755 bin/*.sh`
7. `bin/create-server.sh`
8. if you want to login to django images, do `sudo docker exec -i -t django /bin/bash`

## How to use it
* Start Docker Images  `bin/start-server.sh`  
* Stop Docker Images  `bin/stop-server.sh`  
* Make Docker Images  `bin/create-server.sh`    
* Delete Docker Images  `bin/delete-server.sh`    
  * If you want to delete MySQL database file also, you should remove data directory to use `rm -rf posgres/data/`  

## Setting up a your Development Environment

If you want to change app or db version, you should fix **docker-compose.yml** file.  
  image: posgres:alpine  ->  image: posgres:9.6.5-alpine  

You can check docker version on the Docker Hub.  
  django : <https://hub.docker.com/_/python/>  
  Nginx : <https://hub.docker.com/_/nginx/>  
  Postgresql : <https://hub.docker.com/_/postgres/>  

## License
This project is licensed under the terms of the MIT license.
