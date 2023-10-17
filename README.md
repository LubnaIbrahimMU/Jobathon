# Jobathon
# MySQL-and-Python
A small web app that allows users to create accounts, login, and make a bucket list.
This app is implemented using MySQL and Python. Copied from the tutorial http://code.tutsplus.com/tutorials/creating-a-web-app-from-scratch-using-python-flask-and-mysql--cms-22972

#Prerequisites/tools needed to work on this project.
-Docker
-Kubernetes
-Jenkins
-terraform


#Steps
-create Dockerfile for Flask-app
-create Dockerfile for MySQL
-creating Dockercompose for Both

Now we can't create GkE infra, I don't have access to GCP right now

then I created Kubernetes files 

#Setting Up Jenkins
Make sure you follow these steps to set up Jenkins from the Linode marketplace: https://www.linode.com/marketplace/apps/linode/jenkins/

#Setup
 By using Jenkinsfile we can build Docker Images and Push them to my Dockerhub

-Build docker Images using Dockerfile - Tag docker images
-Complete Declarative CI/CD Pipelines in Jenkins Project - Push Images to DockerHub



