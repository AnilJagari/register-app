# CI → CD → SonarQube → DockerHub → ArgoCD → Application Pipeline

This project demonstrates a complete DevOps CI/CD workflow including:
- Continuous Integration (CI)
- Continuous Deployment (CD)
- SonarQube Code Quality Analysis
- Docker Image Build & Push to DockerHub
- ArgoCD GitOps Deployment
- Application Deployment on Kubernetes

---

## 📸 BEFORE COMMIT

These images show the pipeline *before* a new commit is pushed.

![Before 1](images/before/Screenshot%202025-11-19%20123129.png)
CI and CD Pipelines in jenkins
![Before 6](images/before/Screenshot%202025-11-19%20123345.png)
CI part
![Before 5](images/before/Screenshot%202025-11-19%20123316.png)
CI part
![Before 2](images/before/Screenshot%202025-11-19%20123153.png)
Sonarqube server
![Before 4](images/before/Screenshot%202025-11-19%20123235.png)
New Image Pushed to Dockerhub with Build Tag
![Before 3](images/before/Screenshot%202025-11-19%20123214.png)
Argocd deploying the new pods into the k8s cluster
![Before 7](images/before/Screenshot%202025-11-19%20123714.png)
Application on server

---

## 📸 AFTER COMMIT

These images show the pipeline automatically triggered after a commit.

![After 1](images/after/Screenshot%202025-11-19%20123453.png)
commit with new change
![After 2](images/after/Screenshot%202025-11-19%20123845.png)
CI part
![After 3](images/after/Screenshot%202025-11-19%20123906.png)
CD part
![After 4](images/after/Screenshot%202025-11-19%20123942.png)
Sonarqube server
![After 5](images/after/Screenshot%202025-11-19%20124005.png)
New Image Pushed to Dockerhub with Build Tag
![After 6](images/after/Screenshot%202025-11-19%20124106.png)
Argocd deploying the new pods into the k8s cluster
![After 7](images/after/Screenshot%202025-11-19%20124144.png)
Application on server

---


