
# Kubernetes-AWS-Minikube-Django-React: A Comprehensive Guide to Orchestrating and Scaling Applications with Kubernetes on AWS using Minikube.

This repository guides the process of building a Kubernetes cluster on AWS from scratch using Minikube. The project includes the setup and management of Docker containers for both a Django backend and a React frontend application within Kubernetes pods. The repository covers key aspects of Kubernetes orchestration, including deployment, replication of pods, autoscaling, and autohealing. Furthermore, it addresses the management of network configurations and services, facilitating the interaction with the application through Kubernetes services while considering host IP considerations.

Noteworthy within this setup is the automatic recreation of failed pods and seamless load transfer to new pods using a service static IP, ensuring continuous availability and optimal performance.



## Installation

To start Deploy the django application first you need to install minikube,docker,and kubectl on your EC2 instance.

```bash
 sudo -i
```
```bash
# Docker Installation

 apt install docker.io -y
```
```bash
# Minikube Installation

 curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
 sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```
```bash
# kubectl Installation

  snap install kubectl --classic
```
```bash
# Start the Minikube

  minikube start --driver=docker --force
```



# Deployment

To deploy this First you need to make the clone of this repository then create docker image using Dockerfile.

```bash
  git clone https://github.com/RaviChandra001/Django-todo-app-.git
```
```bash
 # Create the docker image 
 cd django-todo-cicd

 docker build -t ravichandra001/ravi .
```
```bash
 # Now Run container so that can first deploy on docker

 docker run -dp 8000:8000 ravichandra001/ravi  
```
## Deploying on kubernetes 
```bash
 # Just come back 

 cd ..
```
```bash
 # Make pod using pod.yaml file

 kubectl apply -f pod.yaml
```
```bash
# Make deployemnt using deployemnt.yaml

 kubectl apply -f deployment.yaml
```
```bash
# Make service to route the request 

 kubectl apply -f service.yaml
```

## Start using Minikube
```bash
# List the todo-service 

kubectl get svc
```
```bash
 minikube service todo-service --url
```
```bash
# Binding the given Ip on some domain 

vim /etc/hosts
```
<img width="789" alt="Screenshot 2023-11-10 at 3 12 24 PM" src="https://github.com/RaviChandra001/Django-todo-app-/assets/134200599/5050960a-0e0c-4323-a642-343191deb2e7">

```bash
curl -L todo-app.com:3000
```
<img width="1188" alt="Screenshot 2023-11-10 at 3 27 42 PM" src="https://github.com/RaviChandra001/Django-todo-app-/assets/134200599/711750e6-0c15-4512-a31c-b029f73c5323">

## Features

- Automatic Pod Recreation and Load Transfer
- Continuous Availability Assurance
- Kubernetes Cluster Setup
- Robust Kubernetes Orchestration (Deployment, Replication, Autoscaling, and Autohealing)


## 🛠 Skills Gained 
Docker, Deployment, Kubernetes, AWS, Minikube, Kubectl, Creating YAML configuration files...



## 🚀 About Me
💡 Currently learning DevOps

🤝 Looking for help to work on DevOps projects

💬 Ask me about anything related to DevOps

📫 Connect with me on LinkedIn

⚡️ Fun fact: DevOps is too easy!


## Related

Here are some related projects

[DevOps_Project](https://www.interviewbit.com/blog/devops-projects/)

[CiCd Blog](https://katalon.com/resources-center/blog/ci-cd-tools)



## S u p p o r t

For support, email raviamazon1101@gmail.com or LinkedIn https://www.linkedin.com/in/ravi-chandra-5a2b99230/

