kubectl run busybox --image busybox --restart OnFailure --dry-run -o yaml

kubectl run busybox --image busybox --restart OnFailure --schedule "* * * * *" --dry-run -o yaml

https://crontab.guru/#*/10_*_*_*_*


