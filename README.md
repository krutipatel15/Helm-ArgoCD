# 🚀 WordPress Stack with Nginx Proxy and GitOps Deployment

Once upon a time, deploying WordPress meant setting up servers manually, configuring proxies by hand, and worrying about keeping everything in sync.

So this project tells a better story.

This repository contains everything needed to deploy a **WordPress stack on Kubernetes** with:
- An **Nginx reverse proxy** in front,
- A **MySQL database** in the backend,
- And **GitOps automation using Argo CD** to keep the cluster always in the desired state.

Every change pushed to this repository becomes the source of truth — and Argo CD takes care of applying it to the cluster.

---

## 🧩 Project Overview

This project includes the following components:

### 📝 WordPress Application
A containerized WordPress application running inside Kubernetes, backed by a MySQL database.

### 🌐 Nginx Reverse Proxy
Acts as the gateway to the WordPress application and securely forwards incoming traffic.

### 🗄️ Database (MySQL)
Stores WordPress content, configuration, and user data.

### 🔁 GitOps with Argo CD
Argo CD continuously watches this repository and automatically:
- Detects changes
- Syncs them to the cluster
- Ensures the live environment always matches Git

---

## 🎯 Objectives

- Deploy the WordPress stack (WordPress app, MySQL DB, Nginx proxy) using Kubernetes
- Configure GitOps practices to automate deployment with Argo CD
- Secure sensitive information using encryption tools (for example: Kubernetes Secrets / Sealed Secrets)
- Organize deployments into namespaces for better separation and management

---


All components are deployed into Kubernetes and managed declaratively through Git.

---

## 🚀 How to Deploy

### 1️⃣ Prerequisites

- A running Kubernetes cluster
- `kubectl` configured
- Helm installed
- Argo CD installed in the cluster

---

### 2️⃣ Clone the repository

```bash
git clone <your-repo-url>
cd <your-repo-name>
```

### 3️⃣ Install Argo CD (if not already installed)

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### 4️⃣ Register the application with Argo CD
```bash
kubectl apply -f argocd/application.yaml
```

Argo CD will now:

Pull the manifests from Git
Deploy WordPress, MySQL, and Nginx
Continuously reconcile any changes

### 🧹 Cleanup

```bash
kubectl delete -f argocd/application.yaml
kubectl delete namespace <your-namespace>
```

