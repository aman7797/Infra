# Bamboo Installation in CentOS

## What is Bamboo

Bamboo is a continuous integration (CI) server that can be used to automate the release management for a software application, creating a continuous delivery pipeline.

## Pre-Requirement

1. Centos 6.x +
2. Apache
3. Java (The JDK 1.8 version )
4. Bamboo License

## Java Installation

1. To check if Java is already installed or not 

        java -version

2. Lets start by installing JDK 1.8.0

        yum install java-1.8.0-openjdk

3. This will install Java 1.8.0 now set the java path to `/usr/local/bin/java` 

        export  $JAVA_HOME= /usr/local/bin/java

4. To check if the Java Home path is set or not 

        echo $JAVA_HOME

    We are set with the JAVA .

## Postgres Installation

1. We can install PostgreSQL using yum install:

        yum install postgresql-server postgresql-contrib

    This might take some time to complete.

2. Initialize the Database - Once the installation is done, we can initialize the database using the below command:

        postgresql-setup initdb

    ![postgressInitDB](img/postgressInitDB.png)

3. Start the Database - after initializing the database, we can start the database using:

        systemctl start postgresql

4. (**Optional)** Enable PostgreSQL - This completes our database installation and initialization. If required we can configure PostgreSQL to start on every system reboot automatically.

        systemctl enable postgresql

    ![postgressInitDB](img/enablePostgres.png)
