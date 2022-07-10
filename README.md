# kubernetes
# Kubernetes resources (kubectl)

kubectl get pods

kubectl describe pods

kubectl delete pods frontend-rwldh

kubectl get replicasets.apps

kubectl scale nginx-deployment --replicas=5

kubectl get deployment.app

kubectl describe deployment.apps nginx-deployment | grep -i image 

kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1

kubectl get rs

kubectl scale deployment/nginx-deployment --replicas=5

