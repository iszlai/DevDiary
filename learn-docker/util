#clean up docker containers
docker rm `docker ps -a | cut -d" " -f1 |grep -v CONTAINER`


docker build -t="stet" .
#apache CMD
docker run -d -p 80:80 stet

#simple echo entry
docker run echo test
#apache Entrypoint
docker run -d -p 80:80 web2 -D FOREGROUND

#environment
$ docker run -it simpleenv /bin/bash
root@c45326ec79ee:/# env


#volumes

#create volume
docker run -it -v /test-volume --name=lehelvolume ubuntu:15.04 /bin/bash
#mount from other container 
docker run -it --volumes-from lehelvolume  --name=cont2 ubuntu:15.04 /bin/bash
#from host machine   (docker host : docker local)
docker run /data:/data
#delete volume
docker rm -v lehelvolume


#network

-P for random ports
docker ports


#linking containers

cont 1 =src
cont 2 =recriver

docker run --name=src -d img #img has expose

docker run --name=receiver --link=src:ali-src -it ubuntu:15.04 /bin/bash

#in container 2 receiver the source is mappaed as ali-src 
#env variables are set up
#added to /etc/hosts
