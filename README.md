# Tutorial - Docker Containers

## Setup

### Lab VM
Log into your Azure Portal and start your Lab VM

In Azure cloud shell, open port 8080 on the lab VM
  
    az vm open-port --resource-group fall-2022-lab-work --name labvm --port 8080

Log into the Lab VM via ssh
  
    ssh -i <path-to-private-key> username@ip-address 
   
### Docker Setup & Maven setup
Install Docker on your Lab VM

    sudo apt install docker.io

### Install Maven
Maven is used to build and package a java application. Run the command below to install maven.

    sudo apt install maven
    
    
## Setup PetClinic Java Spring Boot Application
    
    # create lab directory
    cd ~
    mkdir labs
    cd labs
    mkdir containers
    cd containers
    
    # Clone petclinic spring boot application
    git clone https://github.com/spring-projects/spring-petclinic.git
    
    cd spring-petclinic
 
### Run the web app
    # Package the application
    mvn package
    
    # Run the executable
    java -jar target/spring-petclinic-2.7.3.jar

## Dockerize the executable

### Create the Docker File
    touch Dockerfile
    
    
