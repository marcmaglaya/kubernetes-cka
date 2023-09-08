# create pods and expose 
kubectl run httpd --image=httpd:alpine --port=80 --expose=true

# search with selector
kubectl get pods --selector app=App1

kubectl get pods --selector app=foo,k8s-app=bar

# count number of pods
kubectl get pods --selector env-dev --no-headers | wc -l

# check pods which controlled by nodes
kubectl get pods --all-namespaces -o custom-columns=NAME:.metadata.name,CONTROLLER:.metadata.ownerReferences[].kind,NAMESPACE:.metadata.namespace
or 
check the pods name which ends with node name

# directory holding the static pod definition files
cat /var/lib/kubelet/config.yaml | grep staticPodPath

