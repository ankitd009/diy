Create Grafana Secret
```
kubectl create -f secret.yaml
```

Create Grafana Deployment
```
kubectl create -f deployment.yaml
```

Expose Deployment
```
kubectl expose deployment grafana --type=LoadBalancer --port=3000 --target-port=3000 --protocol=TCP
```

Expose on Minikube
```
minikube service grafana --namespace monitoring
```