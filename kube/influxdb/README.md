Create InfluxDB Secret
```
kubectl create secret generic influxdb-creds \
  --from-literal=INFLUXDB_DATABASE=local_monitoring \
  --from-literal=INFLUXDB_USERNAME=root \
  --from-literal=INFLUXDB_PASSWORD=root1234 \
  --from-literal=INFLUXDB_HOST=influxdb
```

Create Persistent Volume
```
kubectl -f create pvc.yaml
```

Create InfluxDB Deployment
```
kubectl -f create deployment.yaml
```

Expose deployment
```
kubectl expose deployment influxdb --port=8086 --target-port=8086 --protocol=TCP --type=ClusterIP
```