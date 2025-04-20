# DockerContainerisationProject
This project is a demonstration on how to build images and use them as a template to create a container to host a static HTML webpage on your local host machine.

Below is the flow of Mini Project :

![Alt Text](assets/images/Project01.png)


# Steps of Creating project :

Step 01 : Create a project directory, let say Myproject by below command
           mkdir Myproject
           cd Myproject
        

Step 02 : Create an index.html file via vim editor by vim index.html

step 03 : write the required html file in it.

step 04:  Install the docker on the host machine.

step 05: Create DockerFile :

       FROM nginx
       COPY index.html usr/share/nginx/html 

step 06: Create docker Image by below command :

         docker build -t Myproject:v1 .

step 07: Create container by below command:

          docker run -p 8080:80 -d Myproject:v1
        

The container is accessed by “host-ip-address:8080”

Where port 8080 denotes the port number of your local host which is
accessing the port 80 of the container.

