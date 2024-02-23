# KodeKloud Kubernetes Tutorial

1. minikube start

2. kubectl create -f replicaset.yaml

3. kubectl get replicaset

4. kubectl get pods

## Delete Deployment (and all associated resources)

1. kubectl delete deployment myapp-deployment

2. Verify with:

- kubectl get deployments

- kubectl get replicasets

- kubectl get pods