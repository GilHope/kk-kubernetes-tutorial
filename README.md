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

# Listing Resources

To View Nodes
- kubectl get nodes

To View Pods
- kubectl get pods

To View Replicasets
- kubectl get replicaset

To View Deployments
- kubectl get depoyments

To View All
- kubectl get all

# Display The State of Resources

To see details about a specific pods
`kubectl describe pods/[pod-name]`

To see details about all pods
`kubectl describe pods`

To see details about a particular node
`kubectl describe nodes [node-name]`

To see details about a particular pod
`kubectl describe pods [pod-name]`

# Delete Resources

To delete a pod using the type and name  specififed in the pod

To delete all pods, including uninitialized ones
`kubectl delete pods --all`

