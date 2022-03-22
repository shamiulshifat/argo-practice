1. ARGO UI: 
```
kubectl -n argo port-forward deployment/argo-server 2746:2746
```
2. GRAFANA UI:

```
sudo microk8s kubectl port-forward -n monitoring service/grafana --address 0.0.0.0 3000:3000
```

3. MINIO UI: 
```
sudo ./minio server /minio
```

4. PROMETHEUS UI:

```
sudo microk8s kubectl port-forward -n monitoring service/prometheus-k8s --address 0.0.0.0 9090:9090
```

5. WEBHOOK TITANIC:
```
kubectl -n argo port-forward $(kubectl -n argo get pod -l eventsource-name=webhook-titanic -o name) 8080:8080 &
```

6.
