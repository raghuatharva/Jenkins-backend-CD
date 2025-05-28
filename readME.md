# 🚀 Node.js Backend - CD Pipeline (Jenkins + AWS ECR + Multi-Env)

This guide explains how the backend Docker image built during CI is **pulled from AWS ECR** and deployed to different environments (**dev**, **staging**, **prod**) using **Jenkins pipelines**.

---

## 🎯 Objectives

- Pull built image from **ECR**
- Deploy to multiple environments (e.g., **Dev**, **Staging**, **Prod**)
- Use **Jenkins** as the CD orchestrator
- Maintain separate config per environment
- Ensure smooth, secure, automated deployment process

---

## 📦 Deployment Stack

- **AWS ECR** for image storage  
- **Jenkins** for CD pipelines  
- **Docker** or **Kubernetes** (optional) for runtime deployment  
- **EC2** or **ECS/EKS** as deployment targets  
- **Jenkins Shared Libraries** (optional)

---

## 🚧 Pre-requisites

- Jenkins nodes with `docker`, `awscli`, `kubectl` (if K8s)
- ECR Repository created
- Jenkins has IAM credentials to pull from ECR
- SSH access (for EC2) or Kubeconfig (for EKS)

---

## 🌐 Environments

We support the following environments:

- `dev`
- `staging`
- `prod`

Each has:

- Separate deployment targets (e.g., EC2 IPs or Kubernetes namespaces)
- Environment-specific env files or configs
