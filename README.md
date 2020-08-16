# Basic Commands: PODS

To Create replication Controller

`kubectl apply -f <pod definition file>`

To know about how many pods are in running state

`kubectl get pods`

To get detailed report of pods

`kubectl get pods -o wide`

To get complete information about pod details

`kubectl describe pods <pod-name>`


# Relication Controller 

To Create replication Controller

`kubectl create -f <name of the rc definition file >`

Check on the status of the ReplicationController using this command:

`kubectl describe replicationcontrollers <name of the rc>`