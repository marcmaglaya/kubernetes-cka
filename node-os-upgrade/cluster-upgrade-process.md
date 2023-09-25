# strategy 1 - upgrade all nodes in 1 go : require down time
# strategy 2 - rolling update
# strategy 3 - bring up new node that have new os version then bring downm old node

# kubeadm upgrade 
kubeadm upgrade plan

step 1 :
# upgrade kubeadm first
apt-get upgrade -y kubeadm=version 

# upgrade cluster
kubeadm upgrade apply v1.12.0

step 2 : 
# upgrade kubelet 
apt-get upgrade -y kubelet=version

systemctl restart kubelet

step 3 : 
# upgrade node worker
kubectl drain node-1

apt-get upgrade -y kubeadm=1.12.0-00 
apt-get upgrade -y kubelet=1.12.0-00

kubeadm upgrade node config --kubelet-version v1.12.0

systemctl restart kubelet

kubectl uncordon node-1