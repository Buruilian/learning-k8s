# go web app

```
docker build -t hellogo:v1.0 .
kubectl apply -f .
curl <nodeip>:<nodeport>

root@k8s-master1:~/kubernetes-yaml/golang# curl 172.31.7.111:30518/health -i
HTTP/1.1 200 OK
Date: Mon, 20 Dec 2021 07:31:01 GMT
Content-Length: 0

root@k8s-master1:~/kubernetes-yaml/golang# curl 172.31.7.111:30518/version
1.2
root@k8s-master1:~/kubernetes-yaml/golang# curl 172.31.7.111:30518
Hello, Go! I'm instance 195 running version 1.2 at 202012-1220-200 1212:207:10
```