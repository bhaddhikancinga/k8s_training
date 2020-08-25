kubectl get namespace
kubectl get namespaces
kubectl get ns

kubectl create ns ncinga
kubectl delete ns ncinga

kubectl run nginx --image nginx --restart Never --port 80 

# namespace scoped

kubectl get pods
kubectl get po

kubectl describe pod nginx
kubectl get pods -o wide

kubectl run nginx --image nginx --restart Never --port 80 --dry-run -o yaml > nginx-pod.yaml

kubectl apply -f nginx-pod.yaml 

kubectl port-forward po/nginx-pod 8080:80

kubectl edit pod nginx-pod

kubectl explain pod.spec.containers

kubectl get pods --show-labels

kubectl get pods -l company=ncinga

kubectl get pods -n ncinga

kubectl exec -it nginx-pod  -- /bin/sh

kubectl logs nginx-pod

kubectl logs nginx-pod -f

kubectl get pods -A

kubectl get pods --all-namespaces

kubectl get pods -n kube-system

kubectl top pods

# cluster scoped

kubectl get nodes
kubectl get nodes -o wide
kubectl top nodes


## Question

Part 1:

Create a namespace called ghost
Run a pod called ghost inside the ghost ns, image is ghost:alpine port is 2368
Port Forward the pod and bind it to your 8080 on localhost

Save the YAMLS

Part 2:

Delete the pod, recreate with following configs
Requests: 500m, 200Mi
Limits: 1CPU, 500Mi

Part 3:

Delete the pod and update the yaml with the following config

Add a new container in addition to ghost called nginx, and run the image nginx:latest exposing the port 80

Part 4:

open 2 shells and stream logs seperately for both ghost and nginx containers

part 5:

Create a health check on nginx for http port 80 http path / run this check every 60 seccs
HINT: use kubectl explain pod.spec.containers
HINT: health check is called readinessProbe in Kubernetes