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