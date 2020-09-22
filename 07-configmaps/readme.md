kubectl exec -it busybox-7d9bd7997b-f5kbh -- env
kubectl create cm mysql-creds --from-literal MYSQL_HOST=192.156.123.123 -o yaml > mysql-cm.yaml