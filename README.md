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

## Taints

To Check for Taints on a Node:
`kubectl describe node <node-name> | grep -i taint`
Using grep in this way will output just the line pertaining to the word being searched, this case 'taint'.

To add a taint to a node:
`kubectl taint nodes <node-name> <taint-key>=<key-value>:<effect>`

To remove a taint from a node:
`kubectl taint nodes <node-name> <taint_key>=<value>:<effect>-`

## Node Selectors

Under spec section.

Node selectors are used to determine whihc nodes should run a particular pod. They allow you to constrain which nodes your pod is eligable to be scheduled on based on labels assigned to nodes.

Node selectors rely on labels assigned to the nodes. Labels are key-value pairs attached to K8s objects, inlcuding nodes. These can be named anything you desire.

When you define a pod, you can specify a node selector that includes a set of labels and their corresponding values. This selector defines the criteria by which a node must meet in order for that pod to be scheduled on it.

when K8s schedules a pod, it looks for nodes which satisfy the criteria specified in the pod's node selector. If the node's label matches the selector then the pod is scheduled on that node.

To label a node from the commandline:
`kubectl label nodes <node-name> <label-key>=<label-value>`

## Node Affinity

Node affinity is a concept in K8s that allows you to constrain whihc nodes your pod is eligable to be scheduled on based on labels or other node attributes. In doing so you are able to influence the scheduling of pods onto specific nodes that meet the criteria.

Node affinity consists of two main components: Node Selectors and Node Affinity Rules.


