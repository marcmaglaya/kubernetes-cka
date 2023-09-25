# allocate existing pods on node to another node
# once drained it will be set to noscheduling
kubectl drain <node_name>

# once the node back online, need to manually remove the noscheduling
kubectl uncordon <node_name>

# to set node to noscheduling 
kubectl cordon <node_name>

# time pods eviction timeout default : 5mins
kube-controller-manager --pod-eviction-timeout=5m0s
