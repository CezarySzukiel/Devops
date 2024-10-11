## Deployment
```bash
#Create a deployment YAML file
kubectl create deployment [name: nginx] --image=[image: nginx:alpine] --dry-run=client -o yaml > deployment.yaml

#Create a deployment in k8s
kubectl create -f deployment.yaml

# Imperatively scale the Deployment Pods to 4
kubectl scale deployment [name: nginx] --replicas=4

# Declaraively scale the Deployment Pods to 4
vim deployment.yaml -> spec.replicas = 4
kubectl apply -f deployment.yaml

# Change deployment image
kubectl set image image deployment/nginx nginx

# Change Service selector
kubectl set selector svc [service-name: nginx-svc] 'role=green'
```