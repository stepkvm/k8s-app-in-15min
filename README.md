App in Kubernetes in 15 minutes

This simple example show you a way to create nginx app on Kubernetes

## Step by step
use sh/bash -- terminal/console, whatever
1. **Deployment**
kubectl apply -f deployment.yaml
2. ** Service
kubectl apply -f service.yaml
3. ** Verify:
You can check them using
kubectl get pods
kubectl get svc

** oneliner:
if you dont want to download or create .yaml definitions just do:
kubectl create deployment nginx-demo --image=nginx
kubectl expose deployment nginx-demo --port=80 --type=NodePort
kubectl get pods
kubectl get svc

kubectl get svc nginx-demo
using external IP addres (if there is a load balancer) you can access the app
