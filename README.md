# SecureKube DevSecOps

## Secure Enterprise CI/CD Pipeline with Kubernetes & Cloud-Native DevSecOps
SecureKube DevSecOps is a DevOps project that demonstrates a secure and automated CI/CD pipeline for containerized applications. The project integrates containerization, security scanning, Kubernetes deployment, and monitoring to simulate a real-world DevSecOps workflow used in modern cloud-native environments.

## Project Overview
This project implements an automated DevSecOps pipeline where application code is built, scanned for vulnerabilities, containerized, pushed to a container registry, deployed to a Kubernetes cluster, and monitored using observability tools.

The goal is to demonstrate practical DevOps skills including CI/CD automation, container orchestration, security integration, and system monitoring.


## Architecture Workflow

            Developer  
               |  
        GitHub Repository  
               |   
    GitHub Actions CI/CD Pipeline  
               | 
        Docker Image Build  
               | 
        Trivy Security Scan  
               | 
    DockerHub Image Registry  
               |  
    Kubernetes Deployment (Minikube)  
               | 
        Application Service  
               | 
    Prometheus Metrics Collection  
               |  
    Grafana Monitoring Dashboard  


## Technologies Used
### Version Control & CI/CD
- Git
- GitHub
- GitHub Actions

### Containerization
- Docker
- Docker Hub

### Security
- Trivy (Container vulnerability scanning)

### Container Orchestration
- Kubernetes
- Minikube

### Monitoring & Observability
- Prometheus
- Grafana


## Project Features
- Automated CI/CD pipeline using GitHub Actions
- Docker container image build and push to Docker Hub
- Container security scanning with Trivy
- Kubernetes-based deployment using Minikube
- Service exposure for application access
- Monitoring with Prometheus and Grafana dashboards
- Real-world DevSecOps workflow simulation


## CI/CD Pipeline Stages
1. Source code checkout from GitHub repository
2. Build Docker container image
3. Scan container image for vulnerabilities using Trivy
4. Push secure image to Docker Hub registry
5. Deploy application to Kubernetes cluster


## Deployment
Start Kubernetes cluster:
- minikube start

Deploy application:
- kubectl apply -f k8s/deployment.yaml
- kubectl apply -f k8s/service.yaml


Verify pods:
- kubectl get pods


Access application:
- minikube service hey-service


## Monitoring
Monitoring stack is implemented using Prometheus and Grafana.

Prometheus collects Kubernetes metrics and Grafana visualizes them through dashboards displaying:

- CPU utilization
- Memory usage
- Cluster metrics
- Pod performance


## Author
Mokshith S
memoksh.4@gmail.com

## Disclaimer
This project is created for educational and demonstration purposes to showcase DevOps practices including CI/CD, containerization, Kubernetes deployment, and monitoring.


