# Microservices_Architecture_Setup
## Installation
### [Install Docker Desktop](https://www.docker.com/products/docker-desktop/)
### [Install Nginx Ingress](https://docs.nginx.com/nginx-ingress-controller/installation/installing-nic/installation-with-manifests/)
### Enable Kubernetes (Docker Setting)
![image](https://github.com/duc-beluga/Microservices_Architecture_Setup/assets/98554622/931bae42-8a01-4e2a-ad2d-aea4009288f3)
### [Install Chocolatey](https://chocolatey.org/install)
### [Install Skaffold](https://skaffold.dev/docs/install/)
```choco install -y -g skaffold```
### [Install Google CLI/SDK](https://cloud.google.com/sdk/docs/install-sdk)
### [Install gke-gcloud-auth-plugin](https://cloud.google.com/blog/products/containers-kubernetes/kubectl-auth-changes-in-gke)
### [Google Cloud Configurations. Set Kubernetes Context](https://cloud.google.com/blog/products/containers-kubernetes/kubectl-auth-changes-in-gke)
```
gcloud auth login
gcloud init
gcloud components install gke-gcloud-auth-plugin
gcloud components update
set USE_GKE_GCLOUD_AUTH_PLUGIN=True
gcloud container clusters get-credentials <kubernetesClusterName>
```
--------------------------------------------------
## Configuration
- [Kubernete Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- [ClusterIP Service](https://kubernetes.io/docs/concepts/services-networking/service/)
- [Nginx Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)
- [Skaffold](https://skaffold.dev/docs/design/config/)
## Commands
Skaffold: 

```skaffold dev```

Kubernette: 

```kubectl get pods```

```kubectl get deployments```

Docker:

```docker build -t <dockerID>/<imageName> .```
## Files Architecture
- **auth (microservice 1)**
  - node_modules/
  - src/
    - index.ts
  - .dockerignore
  - Dockerfile
  - package.json
  - package-lock.json
  - tsconfig.json
- **infra/**
  - k8s/
    - auth-depl.yaml
    - auth-srv.yaml
    - ingress-srv.yaml
  - skaffold.yaml

