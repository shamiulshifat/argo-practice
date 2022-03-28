1. first apply resource-quota yaml:
```
kubectl apply -f <yaml github link> --namespace=argo
```
2. Now check if deployed successfully:
```
kubectl describe quota <quota name> --namespace=argo
```
3. apply a limit range policy for workflow containers:
```
kubectl apply -f <yaml github link> --namespace=argo
```
Now we can watch live rq, limit of argo namespace using quota:
```
watch kubectl describe quota mem-cpu-argo --namespace=argo
```
also using resource-capacity:

```
watch kubectl resource-capacity -n argo --util --pods --containers

```
