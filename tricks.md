# To create yaml file e.g pod
kubectl run bee --image=nginx --dry-run=client -o yaml > bee.yml
kubectl get pod webapp -o yaml >> new-webapp.yaml3