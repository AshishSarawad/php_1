
Welcome to README file for dockersing a simple PHP App
Please follow the below steps for lab exercises:

sudo docker build . -t your_docker_user_id/myphpapp
(note - change the above your_docker_user_id to userid you had created in cloud.docker.com)
sudo docker images
the above command to see the image you had created
sudo docker login
enter your docker hub crendetials
sudo docker push your_docker_user_id/myphpapp
(note - change the above your_docker_user_id to userid you had created in cloud.docker.com)

How to run application?

sudo docker run -p 80:80 --rm --name myfirstApp1 your_docker_user_id/myphpapp
now go to browser enter the public dns name with port no 8081.  

### if you would like to run on differet port 
sudo docker run -p 8092:80 --rm --name myfirstApp2 your_docker_user_id/myphpapp
Make sure you open port 8092 in security firewall rules.


sample commands for reference:( you dont have to execute, please refer them)

sudo docker images 
   - this command will list all docker images you have on your machine.
   
sudo docker search ubuntu – search the image in docker registry
sudo docker pull ubuntu
  - pull the image from docker registry
sudo docker ps 
  - list all the containers running
sudo docker ps -a  
  list all the containers running/ran
$ sudo docker run -it alpine /bin/sh  to run in interactive mode
$ sudo docker stop <container_id>
$ sudo docker rm  <container_id>

sudo docker rmi image_id --> To delete the images

sudo docker run alpine /bin/sh
sudo docker run -it alpine /bin/sh

sudo docker run alpine ls -l

sudo docker run -it --rm -p 8088:8080 tomcat

sudo docker run -d dockersamples/static-site
sudo docker stop 6a3884611cc6
sudo docker ps �> to know the running containers
sudo docker rm  6a3884611cc6
sudo docker run --name static-site -e AUTHOR="Your Name" -d -P dockersamples/static-site
sudo docker port static-site
sudo curl http://localhost:32768
sudo docker run --name static-site-2 -e AUTHOR="John Smith" -d -p 8080:80 dockersamples/static-site
