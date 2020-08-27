kubectl run nginx --image nginx --restart Never --port 80 -o yaml --dry-run > nginx-pod.yaml

kubectl run nginx --image nginx --restart Always --port 80 -o yaml --dry-run > nginx-deploy.yaml


kubectl explain pod.spec == kubectl explain deployemnt.spec.template.spec
kubectl explain pod ~= kubectl explain deployment.spec.template

kubectl apply -f nginx-deploy.yaml

kubectl get deployment
kubectl get deployments
kubectl get deploy

kubectl describe deploy nginx

kubectl get pods -w

kubectl get rs

kubectl rollout history deploy/nginx

kubectl rollout undo  deploy/nginx --to-revision 2

kubectl set image deploy/nginx nginx=nginx:latest --record

Question

Part 1:

Create a namespace called ghost
Run a deployment called ghost inside the ghost ns, image is ghost:alpine port is 2368
Port Forward the pod created and bind it to your 8080 on localhost

Save the YAMLS

Part 2:

update the deployment with following configs
Requests: 500m, 200Mi
Limits: 1CPU, 500Mi

Part 3:

update the deployemnt with following

Add a new container in addition to ghost called nginx, and run the image nginx:latest exposing the port 80

Part 4:

open 2 shells and stream logs seperately for both ghost and nginx containers
