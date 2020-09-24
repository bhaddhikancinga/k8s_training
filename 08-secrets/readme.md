kubectl create secret generic mysecret --from-literal=mysqlpw=123 --dry-run -o yaml  > mysecret.yaml

https://github.com/bitnami-labs/sealed-secrets
https://katacoda.com/hashicorp

Generic - Opaque
TLS  kubernetes.io/tls   
ImagePullSecrets -  kubernetes.io/dockerconfigjson 
Service Account Tokens -  kubernetes.io/service-account-token 