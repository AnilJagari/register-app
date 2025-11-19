
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
![After – Application Live](images/after/Screenshot 202025-11-19 20124144.png)

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

## ✅ Tips for a clean repo

- Keep images in `images/before` and `images/after` exactly as listed above.  
- If filenames contain spaces, GitHub requires them to be either URL-encoded (as in this file) or renamed without spaces (recommended).  
- Prefer small, optimized screenshots (keep repo size reasonable).

---

## ✨ Want more?
I can:
- Remove spaces from filenames and update links automatically.  
- Produce a small pipeline diagram image and add it to the README.  
- Create a `Jenkinsfile` snippet and `argocd` manifest examples for this flow.

Tell me which of the above you'd like next.
