# k8s-tracking-project
Project learning K8s

## Vs ECS
- Pod = Task (Ephemeral instance).
- Pods are associated with services via Selector -> Labels (key value pairs).
- ReplicaSets are similar to auto-scaling groups.
- Deployment is a ReplicaSet with rolling deployment
--Can do rollbacks if something goes wrong

## Useful Commands
### kubectl
    ## Get
    - kubectl get all ## List all objects you've created.
    - kubectl get pods --show-labels ## List all pods (includes labels)
    - kubectl get pods --show labels ## Filter
    - kubectl get services ## List all services

    ## Apply
    - kubectl apply -f FILENAME.yaml ## create/update template with contents of file.
    - kubectl apply -f , ## Applys all templates within directory

    ## Describe
    - kubectl describe pod PODNAME ## Describes information about specified pod.
    - kubectl describe replicaset REPLICASETNAME

    ## Exec
    - kubectl exec PODNAME CMD ## execute specified command on pod's container
    - kubectl -it exec PODNAME sh ## Opens an interactive shell session
    - kubectl port-forward service/SERVICENAME NODEPORT:PORT ## 

    ## Delete
    - kubectl delete pod PODNAME ## Deletes pod
    - kubectl delete pod PODNAME --force ## Forcefully deletes the pod
    - kubectl delete replicaset REPLICASETNAME ## deletes replicaset

    ## Deployment
    - kubectl rollout status deployment STACKNAME ## Rolling deployment
    - kubectl rollout history deployment STACKNAME ## Shows you previous versions/deployments
    - kubectl rollout undo deployment STACKNAME ## Revert to previous version.
    - kubectl rollout undo deployment STACKNAME --to-revision=2 ## Revert to version 2

    ## Namespaces
    - kubectl get namespaces
    - kubectl get all -n kube-system # Gets all from the kube-system namespace