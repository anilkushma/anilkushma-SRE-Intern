# MySQL and WordPress Deployment on Kubernetes
 
This repository contains Kubernetes manifests to deploy a MySQL StatefulSet and a WordPress Deployment with PersistentVolumeClaims (PVCs) and Services.
 
## Prerequisites
 
- A Kubernetes cluster
- `kubectl` configured to access your Kubernetes cluster
 
## Deployment
 
1. **Clone the Repository:**
 
    ```sh
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```
 
2. **Deploy MySQL:**
 
    Apply the MySQL manifest:
 
    ```sh
    kubectl apply -f mysql-deployment.yaml
    ```
 
3. **Deploy WordPress:**
 
    Apply the WordPress manifest:
 
    ```sh
    kubectl apply -f wordpress-deployment.yaml
    ```
 
## Accessing WordPress
 
Once deployed, WordPress can be accessed using the external IP of the LoadBalancer service on port `80`. You can get the external IP by running:
 
```sh
kubectl get services
```

if ip is not shown  than we need use port-forward 
```sh
kubectl port-forward svc/wordpress 9000:80
```
