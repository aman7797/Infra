# Docker
 This doc explain how to create a Docker image and push to Docker Hub
 
 ## Creating a Docker Image
 
 1. Create a Docker Image
 
  ```docker
  FROM  centos:centos6
  MAINTANER Aman Lalpuria
  RUN yum -y install openssh-server
  EXPOSE 22
  ADD start.sh /start.sh
  CMD /start.sh
  ```

2. Now build the Docker Image
  
        docker build -t amanlalpuria/apache-kafka:1.0
   
   *docker build* - to build the Dockerfile to image
   
   *-t* - to tag the image name 
   
   *amanlalpuria* - the docker hub
   
   *apache-kafka* - the repository(image) name
   
   *1.0* - the image tag

3.  
