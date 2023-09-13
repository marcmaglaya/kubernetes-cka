# Deploy metric server 
git clone https://github.com/kubernetes-incubator/metrics-serve

kubectl create -f deploy/1.8+/

kubectl top node

kubectl top pod

# Application log
kubectl logs -f event-simulator-pod event-simulator

kubectl -n <namespace> -it <pods_name> -- cat /log/app.log