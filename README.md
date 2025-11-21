# 🚀 DevOps End-to-End Project — Java Application → Kubernetes (EKS) with CI/CD & GitOps

This repository is a complete DevOps learning project that demonstrates how to build, automate, containerize, and deploy a Java application using industry-standard DevOps tools.  
You will install each tool from scratch, integrate them, and build a full CI/CD → GitOps pipeline that deploys the application to **Amazon EKS** with **Argo CD**.

---

## 📘 Project Overview

This project helps you understand how real-world DevOps workflows are implemented. The objective is to integrate Jenkins, SonarQube, Docker, Kubernetes, and Argo CD to create a fully automated CI/CD pipeline.

### You Will Learn:

- Installing and configuring DevOps tools  
- Running Jenkins Master + Agent builds  
- Performing code quality analysis using SonarQube  
- Building Docker images for the Java application  
- Deploying to Kubernetes (EKS)  
- Implementing GitOps automation using Argo CD  

---

# 🟦 1. Jenkins Installation & Configuration

Jenkins is used as the main **CI (Continuous Integration)** platform.

### ✔ What This Module Covers

- Jenkins installation on EC2  
- Setting up Jenkins Agent  
- Connecting Jenkins Master ↔ Agent  
- Running distributed builds  
- Configuring JDK, Maven, and tools in Jenkins  

📄 **Refer File:** `jenkins-setup.txt`  
> This file contains all commands and setup steps for Jenkins Master & Agent installation.

---

# 🟩 2. SonarQube Setup (Code Quality Analysis)

SonarQube is used to perform static code analysis for bugs, vulnerabilities, code smells, and quality gates.

### ✔ What This Module Covers

- Installing SonarQube server  
- Configuring memory and running service  
- Accessing the SonarQube dashboard  
- Creating authentication tokens  
- Integrating SonarQube with Jenkins  

📄 **Refer File:** `sonarqube-setup.txt`  
> This file contains full installation commands and integration steps.

---

# 🟨 3. Docker & Containerization

Docker is used to package the Java application into a container image.

### ✔ What This Module Covers

- Installing Docker  
- Writing Dockerfile for Java application  
- Building Docker images in Jenkins  
- Tagging and pushing images to Docker Hub  

---

# 🟥 4. Kubernetes Deployment (Amazon EKS)

The application is deployed to a fully managed Kubernetes cluster using Amazon EKS.

### ✔ What This Module Covers

- Installing AWS CLI, kubectl, eksctl  
- Creating EKS cluster  
- Verifying cluster nodes  
- Creating deployment & service YAML  
- Deploying Java application on Kubernetes  

📄 **Refer File:** `eks-k8s-argocd-setup.txt`  
> Includes all commands to install tools and create the EKS cluster.

---

# 🟦 5. Argo CD — GitOps Deployment

Argo CD is used for **continuous delivery**, enabling automatic deployment to Kubernetes when new code is pushed to GitHub.

### ✔ What This Module Covers

- Installing Argo CD on EKS cluster  
- Exposing the Argo CD UI (LoadBalancer)  
- Logging into Argo CD  
- Creating Argo CD Application  
- Setting GitOps sync and auto-heal  

📄 **Refer File:** `eks-k8s-argocd-setup.txt`  
> Contains Argo CD installation, exposure, login, and configuration steps.

---

# 🟪 6. Monitoring with Prometheus & Grafana

Prometheus and Grafana are used to monitor the Kubernetes cluster, application performance, and resource usage.

### ✔ What This Module Covers

- Installing Prometheus on Kubernetes  
- Installing Grafana on Kubernetes  
- Exposing Grafana dashboard  
- Adding Prometheus as a data source in Grafana  
- Creating dashboards to monitor pods, nodes, deployments, and cluster health  

📄 *(prometheus-grafana-setup.txt Coming Soon)*  
> This will contain all commands for installing and configuring Prometheus & Grafana on Kubernetes.



---

## 📸 BEFORE COMMIT — Pipeline State Before Code Change

These images show the pipeline before a new commit is pushed.

---

### 1) Jenkins — CI & CD Pipeline Overview
![Before – Pipeline Overview](images/before/Screenshot%202025-11-19%20123129.png)

*Figure: High level view of Jenkins pipelines (CI & CD).*

---

### 2) Jenkins — CI Stage (Build & Tests)
![Before – CI Stage](images/before/Screenshot%202025-11-19%20123345.png)

*Figure: CI stage showing build/test steps before commit.*

---

### 3) Jenkins — CD Stage (Docker Build Trigger)
![Before – CD Stage](images/before/Screenshot%202025-11-19%20123316.png)

*Figure: CD stage which packages artifact and triggers container build.*

---

### 4) SonarQube — Code Quality Dashboard
![Before – SonarQube](images/before/Screenshot%202025-11-19%20123153.png)

*Figure: SonarQube dashboard snapshot (before commit scan).*

---

### 5) DockerHub — Image (Before)
![Before – DockerHub Image](images/before/Screenshot%202025-11-19%20123235.png)

*Figure: DockerHub showing the currently available image/tag before change.*

---

### 6) ArgoCD — Deployment State (Before)
![Before – ArgoCD Deployment](images/before/Screenshot%202025-11-19%20123214.png)

*Figure: ArgoCD showing current application manifests & sync status.*

---

### 7) Application — Running Version (Before)
![Before – Application Running](images/before/Screenshot%202025-11-19%20170157.png)

*Figure: The application instance running the previous version.*

---

## 📸 AFTER COMMIT — Pipeline Execution After Code Change

After pushing a commit, Jenkins automatically triggers the pipeline — these images show that flow.

---

### 1) Git Commit — New Change Submitted
![After – Commit](images/after/Screenshot%202025-11-19%20123453.png)

*Figure: Commit message and files changed triggering CI.*

---

### 2) Jenkins — CI Stage Triggered Automatically
![After – CI Stage](images/after/Screenshot%202025-11-19%20123845.png)

*Figure: CI stage executing build & tests after commit.*

---

### 3) Jenkins — CD Stage Executing (Docker Build & Push)
![After – CD Stage](images/after/Screenshot%202025-11-19%20123906.png)

*Figure: CD step building image and preparing to push.*

---

### 4) SonarQube — New Analysis After Commit
![After – SonarQube](images/after/Screenshot%202025-11-19%20123942.png)

*Figure: SonarQube shows an updated analysis report for the new commit.*

---

### 5) DockerHub — New Versioned Image Published
![After – DockerHub Image](images/after/Screenshot%202025-11-19%20124005.png)

*Figure: Newly pushed Docker image with new build tag/version.*

---

### 6) ArgoCD — Syncing New Image & Rolling Update
![After – ArgoCD Deployment](images/after/Screenshot%202025-11-19%20124106.png)

*Figure: ArgoCD detected new image/tag and performed a sync/rollout.*

---

### 7) Application — Updated Version Live
![After – Application Live](images/after/Screenshot%202025-11-19%20124144.png)

*Figure: Application is updated and serving the new version.*

---

## 📘 Stage Descriptions (Short)

- **Continuous Integration (CI)** — Jenkins builds, runs unit tests and prepares artifacts.  
- **Continuous Deployment (CD)** — Jenkins builds Docker images, tags them, and pushes to DockerHub.  
- **SonarQube** — Static analysis for bugs, vulnerabilities and code smells; gate for quality.  
- **DockerHub** — Acts as the image registry for deployment artifacts.  
- **ArgoCD** — Watches Git (manifests) and image tags; performs syncs to Kubernetes.  
- **Kubernetes** — Runs the application pods, services and exposes the app.

---
