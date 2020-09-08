docker run -p 3306:3306 -e MYSQL_ROOT_PASSWORD=pass -v $(pwd)/004-recap/data-dir:/var/lib/mysql mysql:5.7


dump of data from mysql 5.7
apt-get upgrade mysql8 (c++, g, libsql)

import data from the dump

ERROR!!! cannot import from the dump

ROLLBACK to 5.7



kubectl run demo-app --image  nj93/webinar-demo:v1 --port 8080 --dry-run -o yaml > deploy.yaml
kubectl run demo-app --image  nj93/webinar-demo:v1 --restart Never --port 8080 --dry-run -o yaml
kubectl run demo-app --image  nj93/webinar-demo:v1 --restart Always --port 8080 --dry-run -o yaml


kubectl run demo-app --image  nj93/webinar-demo:v1 --restart OnFailure --port 8080 --dry-run -o yaml
kubectl run demo-app --image  nj93/webinar-demo:v1 --restart OnFailure --port 8080 --dry-run -o yaml --schedule "* * * *"