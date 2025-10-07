App in Kubernetes in 15 minutes

This simple example show you a way to create nginx app on Kubernetes

## Step by step

1. **Deployment**
use sh/bash -- terminal/console, whatever
kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

You can check them using
kubectl get pods
kubectl get svc

if you dont want to download or create .yaml definitions just do:
kubectl create deployment nginx-demo --image=nginx
kubectl expose deployment nginx-demo --port=80 --type=NodePort
kubectl get pods
kubectl get svc

kubectl get svc nginx-demo
using external IP addres (if there is a load balancer) you can access the app
