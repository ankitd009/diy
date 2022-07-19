```
docker run -d  --rm --name prom  -p 9090:9090 \
  -v /Users/ankit.deshpande/workspace/data/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus
```
