# 🚀 Kubernetes GitHub Actions CI/CD Project

A production-style DevOps project demonstrating an end-to-end CI/CD pipeline using GitHub Actions, Docker, Kubernetes, Docker Hub, and AWS EC2.

---

# 📌 Project Overview

This project automates the complete application deployment lifecycle.

Whenever code is pushed to the **main** branch:

- GitHub Actions automatically builds a Docker image.
- Pushes the image to Docker Hub.
- Connects to an AWS EC2 instance using SSH.
- Pulls the latest Docker image.
- Recreates the Docker container.
- Deploys the latest version of the application automatically.

The application is also deployed locally on Kubernetes with production-ready configurations including ConfigMaps, Secrets, Health Checks, Horizontal Pod Autoscaler, and NGINX Ingress.

---

# 🏗 Project Architecture

```
                  Developer
                      │
                  git push
                      │
                      ▼
               GitHub Repository
                      │
                      ▼
              GitHub Actions CI/CD
                      │
      ┌───────────────┼────────────────┐
      │               │                │
      ▼               ▼                ▼
 Build Docker     Push Image      SSH into EC2
    Image         Docker Hub
                                      │
                                      ▼
                            Pull Latest Docker Image
                                      │
                                      ▼
                            Restart Docker Container
                                      │
                                      ▼
                              Live Application
```

---

# ⚙ Technologies Used

- AWS EC2
- Docker
- Docker Hub
- Kubernetes
- Git
- GitHub
- GitHub Actions
- Linux (Ubuntu)
- NGINX Ingress Controller
- Metrics Server
- Horizontal Pod Autoscaler (HPA)

---

# 📂 Project Structure

```
k8s-github-actions-project/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml
│
├── K8s/
│   ├── namespace.yaml
│   ├── Deployment.yaml
│   ├── Service.yaml
│   ├── configmap.yaml
│   ├── secret.yaml
│   └── ingress.yaml
│
├── Website/
│   ├── index.html
│   └── style.css
│
├── Dockerfile
├── .gitignore
└── README.md
```

---

# 🚀 Features

- Dockerized Web Application
- Kubernetes Deployment
- Kubernetes Service
- ConfigMaps
- Secrets
- Liveness Probe
- Readiness Probe
- Resource Requests & Limits
- Horizontal Pod Autoscaler (HPA)
- Metrics Server
- NGINX Ingress
- GitHub Actions CI Pipeline
- Docker Hub Integration
- AWS EC2 Deployment
- Automatic Continuous Deployment

---

# 🐳 Docker

## Build Image

```bash
docker build -t k8s-github-actions-project .
```

## Run Container

```bash
docker run -d -p 80:80 k8s-github-actions-project
```

---

# ☸ Kubernetes Deployment

Create Namespace

```bash
kubectl apply -f K8s/namespace.yaml
```

Deploy Application

```bash
kubectl apply -f K8s/
```

Verify Deployment

```bash
kubectl get all -n dev
```

---

# 📈 Horizontal Pod Autoscaler

Check HPA

```bash
kubectl get hpa -n dev
```

View Metrics

```bash
kubectl top pods -n dev
```

---

# 🌐 Ingress

Check Ingress

```bash
kubectl get ingress -n dev
```

Access

```
http://website.local
```

or

```
http://<EC2-Public-IP>
```

---

# ⚡ GitHub Actions Workflow

The CI/CD pipeline performs the following steps:

- Checkout Repository
- Build Docker Image
- Login to Docker Hub
- Push Latest Image
- Push Versioned Image
- Connect to AWS EC2 via SSH
- Pull Latest Docker Image
- Stop Existing Container
- Start New Container
- Deploy Updated Application

---

# ☁ AWS Deployment

Application is hosted on:

- Ubuntu EC2 Instance
- Docker Engine
- GitHub Actions Deployment
- Docker Hub Image Repository

---

# 📷 Screenshots

## Kubernetes

- Pods Running
- Services
- Ingress
- HPA
- Metrics Server

## GitHub Actions

- Successful Workflow
- Docker Image Build
- Deployment Logs

## AWS EC2

- Running Docker Container
- Live Website

---

# 📊 Project Highlights

✔ End-to-End CI/CD Pipeline

✔ Dockerized Application

✔ Kubernetes Deployment

✔ Auto Scaling with HPA

✔ Metrics Server

✔ NGINX Ingress

✔ AWS EC2 Deployment

✔ GitHub Actions Automation

✔ Docker Hub Integration

---

# 🔮 Future Enhancements

- Prometheus Monitoring
- Grafana Dashboards
- ELK / EFK Logging
- Terraform Infrastructure as Code
- Amazon EKS Deployment
- ArgoCD GitOps
- Helm Charts
- SonarQube Code Quality
- Trivy Image Scanning

---

# 👩‍💻 Author

**Dakshata Chiman**

AWS Cloud & DevOps Engineer

GitHub: https://github.com/dakshatachiman81-tech

LinkedIn: https://www.linkedin.com/in/dakshata-chiman

---

# ⭐ If you found this project useful, don't forget to Star the repository!
