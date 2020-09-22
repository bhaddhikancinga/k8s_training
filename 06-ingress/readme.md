
### install Helm
https://helm.sh/docs/intro/install/

### Install ingress

kubectl create ns nginx-ingress

helm repo add stable https://kubernetes-charts.storage.googleapis.com

helm repo update

helm install nginx-ingress \   
   --namespace nginx-ingress \                                 
   --set controller.service.type LoadBalancer
    stable/nginx-ingress

kubectl get svc -n nginx-ingress -w

curl  -L http://35.225.80.89


### Excersice

RUn a NodeJS app as a deployment
expose the  port as a clusterIP service
Write an ingress file poinitng to that service

