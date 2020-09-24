EmptyDir
HostPath
PersistentVolumes
NFS
secret
configmaps

--
kubectl explain pod.spec.volumes

PersistentVolumes

1. ReadOnly
2. ReadWriteOnly - Everything else
3. ReadWriteMany - NFS and GlusterFS


PersistentVolume
PersistentVolumeClaim

https://velero.io/

https://openebs.io/
https://rancher.com/products/longhorn/
https://rook.io/docs/rook/v1.4/ceph-storage.html

NFS