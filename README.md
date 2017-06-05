# docker-testing
Simple node.js app for container linking testing

## Executing mongodb docker
docker run --name db -d -p 27017:27017 -v /Volumes/Patricio/docker/mongo-nodejs/mongodata mongo
docker run --name db -d -p 27017:27017 mongo

docker exec -it db bash

## Prueba para validar codigo
docker run -it -rm prueba bash


# Docker Link
docker run -d --name db mongo
docker run --name app -d -p 3000:3000 -e MONGO_URL=mongodb://mongoalias/test --link db:mongoalias [imagen]

# Docker Composers
