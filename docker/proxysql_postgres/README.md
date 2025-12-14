# Configure ProxySQL
```
docker pull proxysql/proxysql:3.0.3

docker run --rm --name proxysql_pg --network host -d -v /Users/ankitdeshpande/workspace/diy/docker/proxysql_postgres/proxysql.cnf:/etc/proxysql.cnf proxysql/proxysql:3.0.3

psql -h 127.0.0.1 -p 6133 -U postgres -W -d db_local_test

# to check metrics
curl http://localhost:6170/metrics
```