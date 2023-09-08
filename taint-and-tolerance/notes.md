# Taint is like repelant spray, only pods that can tolerate the repellant can be deploy
# To taint nodes
kubectl taint nodes node-name key=value:taint-effect
# taint effects 
1. NoSchedule
2. PreferNoSchedule
3. NoExecute

# sample command
kubectl taint nodes node1 app=blue:NoSchedule

# commnad to check taints 
kubectl describe node kubemaster | grep Taint