# to check which scheduler used
kubectl get events -o wide
# to check scheduler logs
kubectl logs <scheduler-name> -n kube-system