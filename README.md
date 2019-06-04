# Spring Boot Admin 


## Build with maven 
mvn clean install

## Docker command

docker build -t spring-boot-admin:v1 .

## Run with Docker

docker run spring-boot-admin:v1


## Run with Kubernetes  using google cloud and use your porject.


docker tag spring-boot-admin:v1 gcr.io/appsutility-141503/spring-boot-admin:v1

gcloud docker -- push gcr.io/appsutility-141503/spring-boot-admin:v1

## If you want run and validate

kubectl run spring-boot-admin --image=gcr.io/appsutility-141503/spring-boot-admin:v1


## Deploy spring boot using Kubernetes deployment file

kubectl create -f spring-boot-admin-service.yaml	

## Update deployment with v2 version 

kubectl set image deployment/spring-boot-admin spring-boot-admin=gcr.io/appsutility-141503/spring-boot-admin:v2



