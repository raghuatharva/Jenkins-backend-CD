# Jenkins Continuous Deployment Pipeline – Expense App

This repository contains the Jenkins CD pipeline configuration for deploying the **Expense App** (Frontend + Backend) into a Kubernetes environment using Helm charts.

---

## 📦 Components Involved

- **Jenkinsfile (CD)** – Defines CD stages for:
  - Cloning Helm charts
  - Updating `values.yaml`
  - Deploying via Helm
  - Notifying stakeholders

- **Deployed using:**  
  - Helm 3  
  - Kubernetes  
  - Docker (images already built in CI stage)

---

## 🛠️ Prerequisites

Before you use this pipeline, ensure:

- Jenkins is configured with:
  - Kubernetes plugin (optional)
  - Docker installed (if needed)
  - Git & Helm CLI installed
  - Kubeconfig file available for deployment cluster
- Credentials are stored securely:
  - GitHub Access Token (if private repo)
  - Docker Registry credentials (if pushing images)
  - Kubeconfig stored as secret file credential

---

## 📁 Repo Structure

```bash
jenkins-cd/
├── Jenkinsfile
├── helm-values/
│   ├── backend-values.yaml
│   └── frontend-values.yaml
