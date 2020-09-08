kubectl run nginx --image nginx --restart Always --dry-run -o yaml --port 80 > nginx-deploy.yaml
kubectl get deploy,pods

kubectl expose deploy nginx --port 8080 --dry-run --target-port 80 --type ClusterIP -o yaml > nginx-svc.yaml

kubectl get pods -o wide

kubectl run busybox --image busybox:1.28 --dry-run -o yaml > busybox-deploy.yaml


svc dns --> <svc-name>.<namespace>.svc.cluster.local


to reference crossnamespace services <svc-name>.<namespace>.svc

pod dns --> 10-20-10-23.<namespace>.pod.cluster.local