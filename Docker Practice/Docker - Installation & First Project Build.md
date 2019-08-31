# Docker - Installation & First Project Build
In this blog, I am going to tell about the installation of Docker on Linux and how you can create the Docker image and launch a container.
I think you already have well settled Linux.
1. Docker Installation

    Update the system

        sudo yum check-update
        curl -fsSL https://get.docker.com/ | sh
    Expected output after the installation command. Start the Docker
2. To start the docker 

        systemctl start docker
        systemctl enable docker
    To check the status of the docker, if started or not 

        systemctl status docker
3. How to deploy a Project
    
    i. Let us start by creating a project folder. I have created the folder with name "project" after creation lets went to the directory.

        mkdir project
        cd project
    ii. Create an HTML 
    vi index.html
    Press `esc+i` to insert

        <!DOCTYPE html>
        <html>
        <head> 
            <title>First Page</title>
        </head>
        <body> 
            <h1>This is Start!!</h1>
        </body>
        </html>

    I have given the sample code you can refer. To save the code press `Esc+:` then wq and press enter.

    iii. Now create a Docker file
    vi Dockerfile
    Press `Esc+i` to insert
        
        FROM centos: latest

        LABEL project="Trial"
        LABEL maintainer "aman.sharma163@gmail.com"

        RUN yum -y install httpd

        EXPOSE 80

        COPY index.html /var/www/html

        CMD [ "/usr/sbin/httpd" ,"-D", "FOREGROUND"]
    I have given the sample code you can refer. To save the code press `Esc+:` then wq and press enter.
    
    By now your project creation and docker file creation is completed
    List of file in Project Folder
    
    iv. To build the docker image run:

        docker build /home/amanlalpuria/project/ -t webserver

    `/home/practice/project/` is the directory where the project is present and webserver is the name of the image file which is going to be created.

    v. To launch the container :
        
        docker run -dit -p 1024:80 webserver

    vi. To access the page :

        curl http://10.0.2.15:1024

    Try the above code where `10.0.2.15` is the IP of the system and `1024` is the port where the container started.