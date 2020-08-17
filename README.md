# # Basic Commands: get

To know about how many pods are in running state

`kubectl get pods`

To get detailed report of pods

`kubectl get pods -o wide`

To get definition of pod

`kubectl get pods <podname> -o yaml`

# Basic Commands: delete

To delete a pod

`kubectl delete pods <podname>`

# Basic Commands: describe

To get more details about a pod
`kubectl describe pods <podname>`

# Basic Commands: run


Create a pod using `kubectl run`

`kubectl run --generator=run-pod/v1 nginx --image=nginx`

Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)

`kubectl run --generator=run-pod/v1 nginx --image=nginx --dry-run -o yaml`

Create a deployment

`kubectl create deployment --image=nginx nginx`

Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)

`kubectl create deployment --image=nginx nginx --dry-run -o yaml`

Generate Deployment YAML file (-o yaml). Don't create it(--dry-run) with 4 Replicas (--replicas=4)

`kubectl create deployment --image=nginx nginx --replicas=4 --dry-run -o yaml > nginx-deployment.yaml`



# Basic Commands: PODS

To Create replication Controller

`kubectl apply -f <pod definition file>`

To get complete information about pod details

`kubectl describe pods <pod-name>`


# Relication Controller 

To Create replication Controller

`kubectl create -f <name of the rc definition file >`

Check on the status of the ReplicationController using this command:

`kubectl describe replicationcontrollers <name of the rc>`


# ReplicaSet

To create ReplicaSet

`kubectl create -f replicaset-definition-1.yaml`

To get the details about Replicasets created

`kubectl get rs`

`kubectl get replicaset`

To get details about how to create replicaset
`kubectl explain replicaset`

To update Existing ReplicaSet
`kubectl edit replicaset new-replica-set`

To Scale Replicas to certain number

`kubectl scale replicaset new-replica-set --replicas=5`

To autoscale replicas

`kubectl autoscale rs frontend --max=10 --min=3 --cpu-percent=50`

# Namespaces

To get current Namespace

`kubectl get ns`

To Create namespace

`kubectl create namespace <namespace-name>`

To delete a namespace.

`kubectl delete namespace <namespace name>`

Change Namespace

`kubectl config set-context --current --namespace=my-namespace`

# Services

To get current Namespace

`kubectl get services` `kubectl get svc`
