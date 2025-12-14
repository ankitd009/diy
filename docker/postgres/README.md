# Configure Postgres
```
brew install libpq

docker pull postgres:18.1

docker run -d --rm --name postgres --network host \
-v /Users/ankitdeshpande/workspace/tmp/data/postgres/:/var/lib/postgresql/ \
-e POSTGRES_PASSWORD=secret -e POSTGRES_USER=postgres -e POSTGRES_DB=db_local_test postgres:18.1


psql -h 127.0.0.1 -p 5432 -U postgres -W -d db_local_test
```