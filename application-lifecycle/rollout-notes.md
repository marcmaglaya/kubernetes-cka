# rollout command
# check status
kubectl rollout status deployment/<deployment_name>

# check history
kubectl rollout history deployment/<deployment_name>

# rollback

kubectl rollout undo deployment/<deployment_name>