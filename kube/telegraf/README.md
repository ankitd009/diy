Create Secret
```
kubectl -f create secret.yaml
```
Create Config
```
kubectl create -f config.yaml
```
Create Deployment
```
kubectl -f create depolyment.yaml
```

Expose telegraf deployment
```
kubectl expose deployment telegraf --port=8125 --target-port=8125 --protocol=UDP --type=NodePort
```

Expose on minikube
```
minikube service telegraf --namespace monitoring
```

