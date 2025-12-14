# Configure ProxySQL
```
docker pull proxysql/proxysql:3.0.3
docker run --rm --name proxysql --network host -d -v /Users/ankitdeshpande/workspace/diy/docker/proxysql/proxysql.cnf:/etc/proxysql.cnf proxysql/proxysql:3.0.3

# to check metrics
curl http://localhost:6070/metrics
```