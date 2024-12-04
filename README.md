WordPress Stack with Nginx Proxy and GitOps Deployment

This repository contains the Kubernetes manifests, Helm charts, and automation scripts required to deploy a WordPress stack with an Nginx reverse proxy using GitOps practices. The deployment leverages Argo CD to automate and manage the Kubernetes cluster.

Project Overview
This project involves the following components:

WordPress Application
A CMS platform running with a MySQL database backend.

Nginx Reverse Proxy
Acts as a gateway to the WordPress application, forwarding requests securely.

Database
MySQL database to store WordPress data.

GitOps with Argo CD
Automatically manages application deployment on Kubernetes when changes are pushed to this repository.

Objectives
Deploy the WordPress stack (WordPress app, MySQL DB, Nginx proxy) using Kubernetes.
Configure GitOps practices to automate deployment using Argo CD.
Secure sensitive information using encryption tools.
Ensure deployments are organized into namespaces for better separation and management.


WordPress Stack with Nginx Proxy and GitOps Deployment
This repository contains the Kubernetes manifests, Helm charts, and automation scripts required to deploy a WordPress stack with an Nginx reverse proxy using GitOps practices. The deployment leverages Argo CD to automate and manage the Kubernetes cluster.

Project Overview
This project involves the following components:

WordPress Application
A CMS platform running with a MySQL database backend.

Nginx Reverse Proxy
Acts as a gateway to the WordPress application, forwarding requests securely.

Database
MySQL database to store WordPress data.

GitOps with Argo CD
Automatically manages application deployment on Kubernetes when changes are pushed to this repository.

Objectives
Deploy the WordPress stack (WordPress app, MySQL DB, Nginx proxy) using Kubernetes.
Configure GitOps practices to automate deployment using Argo CD.
Secure sensitive information using encryption tools.
Ensure deployments are organized into namespaces for better separation and management.
Repository Structure
plaintext
Copy code
.
├── nginx-proxy/
│   ├── Dockerfile
│   ├── helm-chart/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   └── values.yaml
├── wordpress-app/
│   ├── Dockerfile
│   ├── helm-chart/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   └── values.yaml
├── database/
│   ├── Dockerfile
│   ├── helm-chart/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   └── values.yaml
├── k8s-manifests/
│   ├── nginx-deployment.yaml
│   ├── wordpress-deployment.yaml
│   ├── db-deployment.yaml
├── .github/
│   └── workflows/
│       ├── deploy.yml
├── README.md
└── secrets/
    └── encrypted-secrets.yaml
Features
Helm Charts
Helm charts are used to simplify the deployment of each component (Nginx proxy, WordPress app, MySQL database).

GitOps Deployment
Argo CD monitors this repository and automatically applies changes to the Kubernetes cluster.

Namespace Management
Each component is deployed into its own namespace:

proxy for Nginx
wp for WordPress
db for MySQL Database
Secure Configurations
Sensitive data is encrypted 

