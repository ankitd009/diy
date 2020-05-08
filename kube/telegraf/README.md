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
Telegraf Service
Use this if only statsD 8125 port is needed
```
kubectl expose deployment telegraf --port=8125 --target-port=8125 --protocol=UDP --type=NodePort
```
Or Create Service if multiple ports are needed
```
kubectl create -f service.yaml
```

Expose on minikube
```
minikube service telegraf --namespace monitoring
```

