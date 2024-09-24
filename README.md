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
