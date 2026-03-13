# EKS Helm Web Application Deployment

This project demonstrates deploying a containerized web application to AWS EKS using Helm.

## Technologies Used

- Docker
- Kubernetes
- Helm
- AWS EKS
- Docker Hub

## Architecture

Browser → AWS Load Balancer → Kubernetes Service → Pod → Docker Container

## Steps Performed

1. Created a simple web application (HTML + Nginx)
2. Built Docker image
3. Pushed image to Docker Hub
4. Created Helm chart
5. Deployed application to EKS cluster
6. Exposed application using LoadBalancer service

## Commands Used

### Build Docker Image

docker build -t <dockerhub-username>/simple-webapp .

### Push Image

docker push <dockerhub-username>/simple-webapp

### Deploy with Helm

helm install webapp ./webapp-chart

### Verify Pods

kubectl get pods

### Get Public URL

kubectl get svc
