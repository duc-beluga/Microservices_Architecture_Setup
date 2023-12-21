# Microservices_Architecture_Setup

## [Install Docker Desktop](https://www.docker.com/products/docker-desktop/)
## Enable Kubernetes (Docker Setting)
![image](https://github.com/duc-beluga/Microservices_Architecture_Setup/assets/98554622/931bae42-8a01-4e2a-ad2d-aea4009288f3)
## [Install Chocolatey](https://chocolatey.org/install)
## [Install Skaffold](https://skaffold.dev/docs/install/)
```choco install -y -g skaffold```
## [Install Google CLI/SDK](https://cloud.google.com/sdk/docs/install-sdk)
## [Install gke-gcloud-auth-plugin](https://cloud.google.com/blog/products/containers-kubernetes/kubectl-auth-changes-in-gke)
## [Google Cloud Configurations. Set Kubernetes Context]
```
gcloud auth login
gcloud init
gcloud components install gke-gcloud-auth-plugin
gcloud components update
set USE_GKE_GCLOUD_AUTH_PLUGIN=True
gcloud container clusters get-credentials <kubernetesClusterName>
```




