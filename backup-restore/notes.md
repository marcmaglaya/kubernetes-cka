# Backup - Resource config
kubectl get all --all-namespaces -o yaml > all-deploy-services.yaml

use VELERO backup tool

# Backup - ETCD
check the --data-dir=/var/lib/etcd in etcd.service


export ETCDCTL_API=3
# backup
    etcdctl \
    snapshot save snapshot.db \
    --endpoint=https://127.0.0.1:2379 \
    --cacert=/etc/etcd/ca.crt \
    --cert=/etc/etc/etcd.server.crt \
    --key=/etc/etcd/etcd-server.key

# check status
    etcdctl \
    snapshot status snapshot.db

# Restore
1. service kube-apiserver stop

2. etcdctl \
      snapshot restore snapshot.db \
      --data-dir /var/lib/etcd-from-backup

3. change the --data-dir path to snapshot.db in etcd.service

4. systemctl daemon-reload\
5. service etcd restart
6. service kube-apiserver start