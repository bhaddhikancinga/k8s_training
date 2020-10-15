firewall-cmd --permanent --add-port=6443/tcp
firewall-cmd --permanent --add-port=2379-2380/tcp
10250/tcp
firewall-cmd --permanent --add-port=10251/tcp
firewall-cmd --permanent --add-port=10252/tcp
10255/tcp
8472/udp
https://medium.com/platformer-blog/kubernetes-on-centos-7-with-firewalld-e7b53c1316af


swap disabled
ip forwarding

Docker Installed
Kubeadm
CNI

NFS utils


sh kubernetes-prerequisites-ubuntu.sh  1.19.3-00


kubeadm
rke
kubespray
kops




kubeadm init --config kubeadm-config.yaml --upload-certs



    kubectl apply -f https://docs.projectcalico.org/v3.11/manifests/calico.yaml