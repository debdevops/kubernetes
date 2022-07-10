# kubernetes Docs - https://kubernetes.io/docs/
# Kubernetes resources (kubectl)
# --dry-run: By default as soon as the command is run, the resource will be created. If you simply want to test your command , use the --dry-run=client option. This will not create the resource, instead, tell you whether the resource can be created and if your command is right.

kubectl run nginx --image=nginx

kubectl get pods

kubectl describe pods

kubectl delete pods frontend-rwldh

kubectl run nginx --image=nginx --dry-run=client -o yaml

kubectl get replicasets.apps

kubectl scale nginx-deployment --replicas=5

kubectl get deployment.app

kubectl describe deployment.apps nginx-deployment | grep -i image 

kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1

kubectl create deployment --image=nginx nginx

kubectl create deployment --image=nginx nginx --dry-run -o yaml

kubectl get rs

kubectl scale deployment/nginx-deployment --replicas=5

kubectl create deployment nginx --image=nginx --replicas=4

kubectl apply -f deployment-namespace.yaml

kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml

kubectl get namespace

kubectl get pods --namespace dev

kubectl run redis --image=redis --namespace finance

kubectl create service nodeport nginx --tcp=80:80 --node-port=30080 --dry-run=client -o yaml

# find blue pod in all namespaces
kubectl get pods --all-namespaces | grep blue 

kubectl -n dev get svc

