# Docker Volume

## Create a Volume
    docker volume create myVol

## Inspect the Volume
    docker volume inspect myVol

## List Volumes
    docker volume ls

## Run an Nginx Container Using the Volume
    docker run -d --name devtest -v myVol:/app nginx:latest

## Connect to the Container
    docker exec -it devtest bash

In this container, the /app folder is mapped to the volume, allowing data to be stored externally outside the container.

## Create a File in the Volume Using Nano
    apt-get update
    apt-get install nano

## Detach from the Container
    exit

## Stop and Remove the Container
    docker stop devtest
    docker rm devtest

## Run the Container Again and Verify Data Persistence
    docker run -d --name devtest -v myVol:/app nginx:latest
    docker exec -it devtest bash
    cd app
    cat text.txt

You will notice that even if the container crashes or is restarted, the text.txt file still exists. Docker volumes provide durable storage for your data.
