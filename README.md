# Kubernetes Website Deployment using Docker, GitHub & Docker Hub

## 📌 Project Overview

This project demonstrates the complete DevOps workflow of containerizing and preparing a static website for Kubernetes deployment.

The application is built using **HTML** and **CSS**, version-controlled with **Git**, hosted on **GitHub**, containerized using **Docker**, published to **Docker Hub**, and is ready to be deployed on **Kubernetes**.

---

## 🚀 Technologies Used

- HTML5
- CSS3
- Git
- GitHub
- Docker
- Docker Hub
- Nginx
- Kubernetes (Upcoming Deployment)

---

## 📂 Project Structure

```
k8s-github-actions-project
│
├── Website
│   ├── index.html
│   └── style.css
│
├── Dockerfile
├── .gitignore
└── README.md
```

---

## ⚙️ Dockerfile

```dockerfile
FROM nginx:latest

COPY Website/ /usr/share/nginx/html/

EXPOSE 80
```

---

## 🛠️ Build Docker Image

```bash
docker build -t k8s-github-actions-project:v1 .
```

---

## ▶️ Run Docker Container

```bash
docker run -d -p 8080:80 --name mywebsite k8s-github-actions-project:v1
```

Visit:

```
http://localhost:8080
```

---

## 📦 Docker Hub

Tag the image:

```bash
docker tag k8s-github-actions-project:v1 dakshata16/k8s-github-actions-project:v1
```

Push the image:

```bash
docker push dakshata16/k8s-github-actions-project:v1
```

Docker Hub Repository:

```
https://hub.docker.com/r/dakshata16/k8s-github-actions-project
```

---

## 📁 Git Commands

```bash
git init
git add .
git commit -m "Initial Commit"
git push -u origin main
```

---

## 🐳 Docker Commands

Build Image

```bash
docker build -t k8s-github-actions-project:v1 .
```

View Images

```bash
docker images
```

Run Container

```bash
docker run -d -p 8080:80 --name mywebsite k8s-github-actions-project:v1
```

View Running Containers

```bash
docker ps
```

Stop Container

```bash
docker stop mywebsite
```

Remove Container

```bash
docker rm mywebsite
```

---

## 🔄 Project Workflow

```
Create Website
        │
        ▼
Initialize Git Repository
        │
        ▼
Push Source Code to GitHub
        │
        ▼
Build Docker Image
        │
        ▼
Run Docker Container
        │
        ▼
Push Image to Docker Hub
        │
        ▼
Deploy to Kubernetes
```

---

## 🎯 Features

- Static website built using HTML & CSS
- Version controlled using Git
- Source code hosted on GitHub
- Containerized using Docker
- Docker image stored in Docker Hub
- Ready for Kubernetes deployment

---

## 📚 Learning Outcomes

Through this project, I learned:

- Git and GitHub
- Docker Image Creation
- Docker Containers
- Dockerfile
- Docker Hub
- Image Tagging
- Nginx Web Server
- Basic Kubernetes Deployment Workflow

---

## 🚀 Future Enhancements

- Deploy application on AWS EC2
- Install Minikube
- Deploy on Kubernetes
- Create Deployment and Service YAML files
- Automate deployment using GitHub Actions
- Implement CI/CD pipeline

---

## 👩‍💻 Author

**Dakshata Chiman**

GitHub: https://github.com/dakshatachiman81-tech

Docker Hub: https://hub.docker.com/u/dakshata16

---

## ⭐ If you found this project helpful, feel free to star the repository.
