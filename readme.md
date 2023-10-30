# Docker Volume


# create volume
docker volume create myVol

# inspect the volume 
docker volume inspect myVol

# list the volumes
docker volume ls

# run a Nginx container that will use the volume
docker run -d --name devtest -v myVol:/app nginx:latest

# conect to the instence 
docker  exec -it devtest bash


# app folder  will mapped to the volume , evry things store or writing in this folder will writing externally outside the container.

# create a file in the volums using nano 

apt-get update 
apt-get install nano


# detach from the instance 

exit

# stop and remove the container 


# Run it Agin and see if the fill still exists

docker run -d --name devtest -v myVol:/app nginx:latest
docker exec -it devtest bash
cd app 
cat text.txt


# after runing this commandes we constate that even crash the container the app file still exist.

# even the container restart or crash the file stile exist 

