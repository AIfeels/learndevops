# learndevops
Hi folks today in this task you will learn how to build and integrate you cicd pipeline with jenkis to your python application
**Prerequisite for this lab **
jenkins machine container with 250 MB of memory or 500 CPU 
10 GB hard disk 
**step -1** you have to install docker engine on you machine ** 
**step-2 ** Write a dockerfile for make jenkins container to setup cicd pipeline **

        **docker build -t myjenkins-blueocean:2.319.2-1 .** 
step-3  run the docker container after mapping volume or add configuration 

**docker run --name jenkins-blueocean --rm --detach \
  --network jenkins --env DOCKER_HOST=tcp://docker:2376 \
  --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 \
  --publish 8080:8080 --publish 50000:50000 \
  --volume jenkins-data:/var/jenkins_home \
  --volume jenkins-docker-certs:/certs/client:ro \
  --volume "$HOME":/home \
  myjenkins-blueocean:2.319.2-1**
  

  
