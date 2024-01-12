# k8s-tracking-project
Project learning K8s

# Useful Commands
## kubectl
    - kubectl get all ## List all objects you've created.
    - kubectl apply -f FILENAME.yaml ## create/update template with contents of file.
    - kubectl describe pod PODNAME ## Describes information about specified pod.
    - kubectl exec PODNAME CMD ## execute specified command on pod's container
    - kubectl -it exec PODNAME sh ## Opens an interactive shell session