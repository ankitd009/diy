## Create Sample Workload
```bash
k run web --image=gcr.io/google-samples/hello-app:1.0 --port=8080
k expose deployment web --target-port=8080 --type=NodePort
k get service web
minikube service web
```

## Create Ingress
```bash
k create -f ing.yaml
```

## To Access Ingress
```bash
curl 192.168.99.100 -H 'host: hello-world.info'
```
Or <br>
Create entry in etc.hosts for hello-world.info to point to ingress's IP.