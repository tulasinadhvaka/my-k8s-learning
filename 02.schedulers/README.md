# Scheduler

By specifying the Name of the node in pod definition file it is possible to schedule the pods on selected nodes



# Lables



To get total objects related to label(inclues pods, deployments, services, replicasets etcs)

`kubectl get all  --selector env=prod`

To use multiple selectors at a time

`kubectl get pods --selector env=prod,bu=finance,tier=frontend`


# Taints and Tolerants

To Taint the nodes Node (restrict pods to run on it unless pod has tolerance)
kubectl taint nodes node1 key=value:NoSchedule

To Untaint the node
kubectl taint nodes node1 key=value:NoSchedule-

eg: tolerance 

```tolerations:
- key: "key"
  operator: "Equal"
  value: "value"
  effect: "NoSchedule" ```
