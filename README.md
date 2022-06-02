### DevOps Project ###

![devops 1](https://user-images.githubusercontent.com/61089660/171560025-e78adf85-0b0b-47e7-8ac6-366728ff5ea3.JPG)

"DevOps Project - CI/CD with Git, GitHub, Jenkins, Ansible, Tomcat, DockerHub, Docker and Kubernetes"

In this project I have used a local version system as Git, GitHub as a distributed version system, Jenkins as a CI/CD tool, 
Maven as a build tool, Ansible for configuration management under deployment tool, Tomcat as a application server, DockerHub as 
to store the images, Docker for containerisation and Kubernetes as a container management tool.

I have setup all this environment on AWS, We have the source code with the developers and they commit that code onto the 
distributed version control system during the development phase and then we need to build this code.

For that,I have used the CI tool called Jenkins, Once Jenkins built the code, it to generate artifacts, Those artifacts 
we need to deploy it onto the target environment.So we needed some tool which can able to deploy the artifacts 
on the target server so I have used Ansible as a deployment tool and it can able to deploy our applications on on a VM or
docker container or a Kubernetes(Pod).In this project I have initially deploy an application on VM and then I deployed it on 
Docker container and last we are going to deploy it on Kubernetes Cluster(Pod).

In this project I have deployed an application on three different kind of target environments.Initially, I have deployed it on
VM, Second is on Docker container and last on Kubernetes cluster(Pod).

So the first developers write a code and commit into git and pushes this code into github then jenkins pull that code and build
that code with the help of maven then jenkins generate the artifacts over to ansible server. I have used ansible as deployment 
tool. In this server I have created Dockerfile for to pull the image of tomcat and copy the the war file into the default webapps
directory of the tomcat and from that Dockerfile I have created image for that i have insalled docker on ansible server. I have
created ansible-playbook for to deploy an image over to dockerhub and deploy container onto Kubernetes, so that I have setup
the Kubernetes cluster with the help of AWS-EKS and created manifest file for to delpoyment and service.

So in this way I have setup a complete CICD pipeline for to deploy an artitcats over to the target environment.
