# Reddit Clone App on Kubernetes
This project demonstrates how to deploy a Reddit clone app on Kubernetes and expose it to the world using Minikube as the cluster.
Below is an overview of the architecture of this Reddit Clone App running on Kubernetes.
![Structure](https://github.com/harshnayangithub/Reddit_Clone/assets/126700987/240762ca-4211-43c7-bbb5-2a0bb1cac94d)

## Prerequisites
Before you begin, you should have the following tools installed on your local machine: 

- Docker
- Minikube cluster ( Running )
- kubectl
- Git

You can install Prerequisites by doing these steps. [click here & complete all steps one by one]().


## Installation
Follow these steps to install and run the Reddit clone app on your local machine:

1) Clone this repository to your local machine: `git clone https://github.com/harshnayangithub/Reddit_Clone.git`
2) Navigate to the project directory: `cd Reddit_Clone`
3) Create a Dockerfile.
4) Build the Docker image for the Reddit clone app: `docker build -t Reddit_Clone .`
5) Push the image to Docker Hub: `docker push <DockerHub_Username>/<Imagename>`(In my case it looks something like this `harshnayan/reddit`)
6) Deploy the app to Kubernetes: `kubectl apply -f deployment.yaml`
7) Deploy the Service for deployment to Kubernetes: `kubectl apply -f service.yaml`
8) Expose the app as a Kubernetes service: `kubectl expose deployment reddit-deployment --type=NodePort --port=5000`

This is how it looks after deployment
![Deployed App](https://github.com/harshnayangithub/Skin_O_Care/assets/126700987/cc57231e-7f13-4953-8ae0-2ed120b1f348)
My deployment URL on EC-2 looks something like this (http://3.108.194.17:3000/)
I have used two different instance one for the CI and other for the Deployment.
![EC-2 Instance](https://github.com/harshnayangithub/Skin_O_Care/assets/126700987/ffc09193-1e0f-4bf3-b8fb-b1353906d2c7)




