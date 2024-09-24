Task Documentation
==========
"Welcome to Level 1!
   Task: Create a simple Pod running nginx in this namespace.
	To reveal the next level, create a ConfigMap named 'next-level'
    with the data: key: 'unlock' value: 'level2'"
```
kubectl run nginx --image=nginx -n level1
```
```
kubectl create -f yamls/cm.yaml -n level1
```
Welcome to Level 2!
    Task: Create a Deployment with 3 replicas of a simple web application.
    To reveal the next level, create a Secret named 'next-level' with the data:
    key: 'unlock'
    value: 'level3' (base64 encoded)
    
```
kubectl create deployment web-deployment --image=nginx --replicas=3 -n level2
```
```
kubectl create secret generic next-level --from-literal=unlock=level3 -n level2
```

Welcome to Level 3!
Task: Create a StatefulSet with a persistent volume for a database application.
    To reveal the next level, create a Service named 'next-level' with the label:key: 'unlock'value: 'level4'

```
kubectl apply -f yamls/pvc.yaml -n level3

kubectl apply -f yamls/sts.yaml -n level3
```
```
kubectl apply -f yamls/svc.yaml -n level3
```

 Welcome to Level 4! Task: Set up a complete application with frontend, backend, and database services, 
    including proper network policies and resource limits.
    To reveal the next level, create an Ingress resource named 'next-level' with the annotation:
    key: 'kubernetes.io/ingress.class'
    value: 'level5'

```

```
```

```
