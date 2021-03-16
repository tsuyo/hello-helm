# Step 1 Kubernetes Only
Deploy
```
git checkout v1
kubectl apply -n demo -f deployment.yaml
kubectl apply -n demo -f service.yaml
kubectl apply -n demo -f ingress.yaml
```
Delete
```
kubectl delete -n demo ingress hello
kubectl delete -n demo service hello
kubectl delete -n demo deployment hello
```

# Step 2 Create Helm Chart
Deploy
```
git checkout v2
helm list -n demo
helm upgrade hello -i -n demo ./hello
```