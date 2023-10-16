# DockerinDocker_Jenkins
DockerinDocker

This repo contains a Dockerfile which will pull the jenkins docker image and install docker.

Command: 

 ```
 docker build --tag docker-in-docker-jenkins .
 ```
 
 To run the docker image:
 
 ```
 docker run -d --group-add 0 -v "//var/run/docker.sock:/var/run/docker.sock" -v jenkins_home:/var/jenkins_home -p 50000:50000 -p 8090:8080 --name jenkins docker-in-docker-jenkins
 ```
