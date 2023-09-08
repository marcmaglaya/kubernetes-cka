Commands : 
  Create:
    kubectl create -f replicaset-definition.yml
  Debug:
    kubectl get replicaset
  Update:
    - update the replicas in definition then run
    kubectl replace -f replicaset-definition.yml

    - or this will change the replicas value in definition
    kubectl scale --replicas=6 -f replicaset-definition.yml
    or 
    kubectl scale --replicas=6 replicaset myapp-replicaset
  Delete:
    kubectl delete replicaset myapp-replicaset * will also delete pods