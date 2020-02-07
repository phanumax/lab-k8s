# Running first app on k8s
```
$ kubectl run kubia --image=phanumax/kubia \
--port=8080 --generator=run/v1
```
# List pods
```
$ kubectl get pods
```
# Pods is managed by ReplicationController
```
$ kubectl get ReplicationController
```
# Increasing the desired replica count
```
$ kubectl scale rc kubia --replicas=3
```
# Access you web application
```
$ kubectl expose rc kubia --type=LoadBalancer \
--name kubia-http
```
# Listing services
```
$ kubectl get services
```
# Connecting to the pod through the port forwarder
```
$ kubectl port-forward kubia-manual 8888:8080
```
