# Configure MySQL
```
brew install mysql-client

docker pull mysql:8.4

docker run --name mysql --network host -e MYSQL_ROOT_PASSWORD=secret -e MYSQL_ROOT_HOST=% -e MYSQL_DATABASE=db_local_test -d --rm mysql:8.4

mysql --host 127.0.0.1 --port 3306 -u root -p
```