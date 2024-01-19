# k8s-tracking-project
Project learning K8s

## Vs ECS
- Pod = Task (Ephemeral instance).
- Pods are associated with services via Selector -> Labels (key value pairs).
- ReplicaSets are similar to auto-scaling groups.

## Useful Commands
### kubectl
    - kubectl get all ## List all objects you've created.
    - kubectl get pods --show-labels ## List all pods (includes labels)
    - kubectl get pods --show labels ## Filter
    - kubectl get services ## List all services
    - kubectl apply -f FILENAME.yaml ## create/update template with contents of file.
    - kubectl apply -f , ## Applys all templates within directory
    - kubectl describe pod PODNAME ## Describes information about specified pod.
    - kubectl describe replicaset REPLICASETNAME
    - kubectl exec PODNAME CMD ## execute specified command on pod's container
    - kubectl -it exec PODNAME sh ## Opens an interactive shell session
    - kubectl port-forward service/SERVICENAME NODEPORT:PORT ## 
    - kubectl delete pod PODNAME ## Deletes pod
    - kubectl delete pod PODNAME --force ## Forcefully deletes the pod