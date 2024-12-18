 Ubuntu Dockerfile

 This repository contains **Dockerfile** of [Ubuntu](http://www.ubuntu.com/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

Docker
is a software platform that allows you to build, test, and deploy applications quickly.  Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

containers
are software code packages that contain an application’s code, its libraries, and other dependencies that it needs to run in the cloud. Any software application code requires additional files called libraries and dependencies before it can run. 

Steps:-
-->Launch linux instance-->Connect with the instance

![Screenshot (19)](https://github.com/user-attachments/assets/c8a945a6-95c3-4803-9a20-50b8a7c5adb6)

Commands:
sudo su

Yum update -y

Yum install docker

Service docker status-->to check status of docker

Press q to quit

Service docker start-->to start docker

Service docker status-->it will show active


![Screenshot (21)](https://github.com/user-attachments/assets/3989246d-d04e-4e73-9d18-70b300481042)

Docker images [to list all docker images available in instance]
Search ‘docker hub’ on google--> search ubuntu and copy the command and paste in putty
command-->docker pull ubuntu

vi index.html [for creating index.html]

<h1>Hello from docker</h1>

to quit press ecs+  :wq

cat index.html

docker images

vi Dockerfile

FROM ubuntu

RUN apt update -y

RUN apt-get install apache2 -y

COPY index.html /var/www/html

EXPOSE 80

CMD ["apachectl","-D","FOREGROUND"]

Cat Dockerfile

Docker build -t img1:v1 .

Docker images

Docker run -p 80:80 image id
![Screenshot (25)](https://github.com/user-attachments/assets/42492dad-7ae9-4762-be6b-5460ff33aa98)

output

![Screenshot (27)](https://github.com/user-attachments/assets/d6454963-466b-4b31-a412-ca28b15677d5)



