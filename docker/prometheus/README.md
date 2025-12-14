```
docker run -d  --rm --name prom --network host \
  -v /Users/ankitdeshpande/workspace/tmp/data/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus
```
