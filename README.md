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

## Deployments - Update and Rollback Commands

To Create a Deployment
- kubectl create -f example-deployment.yml

To Get a Deployment
- kubectl get deployments

To Update a Deployment
- kubectl apply -f example-deployment.yml

- kubectl set image deployment/example-deployment nginx=nginx:1.9.1

To Check the Status of a Deployment
- kubectl rollout status deployment/example-deployment

- kubectl rollout history deployment/example-deployment

To Rollback a Deployment
- kubectl rollout undo deployment/example-deployment

To Delete a Deployment
- kubectl delete deployment example-deployment

## To View Infrastructure

To View Pods
- kubectl get pods

To View Replicasets
- kubectl get replicaset

To View Deployments
- kubectl get depoyments

To View All
- kubectl get all