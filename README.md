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
Delete
```
helm uninstall hello -n demo
```

# Step 3 Template Helm Chart
`Update application image to 0.0.2`

Deploy
```
git checkout v3
helm upgrade hello -i -n demo ./hello
```

# Step 4 Update and Rollback Helm Chart
Deploy
```
git checkout v4
helm upgrade hello -i -n demo ./hello
helm list -n demo
helm history hello -n demo
helm rollback hello 1 -n demo
helm history hello -n demo
helm rollback hello 2 -n demo
```
