Commands : 
  Create:
    kubectl create -f service-definition.yml
  Debug:
    kubectl get services

kubectl create service clusterip redis-service --tcp=6379

kubectl expose service nginx --port=443 --target-port=8443 --name=nginx-https

kubectl expose service redis-service --port=6379

