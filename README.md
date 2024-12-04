WordPress Stack with Nginx Proxy and GitOps Deployment



This repository contains the Kubernetes manifests, Helm charts, and automation scripts required to deploy a WordPress stack with an Nginx reverse proxy using GitOps practices. The deployment leverages Argo CD to automate and manage the Kubernetes cluster.



Project Overview:-
This project involves the following components:

WordPress Application:-
A CMS platform running with a MySQL database backend.

Nginx Reverse Proxy:-
Acts as a gateway to the WordPress application, forwarding requests securely.

Database:-
MySQL database to store WordPress data.

GitOps with Argo CD:-
Automatically manages application deployment on Kubernetes when changes are pushed to this repository.



Objectives
Deploy the WordPress stack (WordPress app, MySQL DB, Nginx proxy) using Kubernetes.
Configure GitOps practices to automate deployment using Argo CD.
Secure sensitive information using encryption tools.
Ensure deployments are organized into namespaces for better separation and management.
