# HAProxy Setup
## Run the sample service using docker
```
docker run -p 9000:8080 gcr.io/google-samples/hello-app:1.0
```

## Pull the docker image using:
```
docker pull haproxy:2.0
```

## Configure HAProxy config file
Download haproxy.cfg and place it at: 
```
/Users/ankitdeshpande/Desktop/haproxy/haproxy.cfg
```

## To Run HAProxy using docker
```
docker run -p 8001:80 -p 1936:1936  -v /Users/ankitdeshpande/Desktop/haproxy/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg haproxy:2.0 haproxy -f /usr/local/etc/haproxy/haproxy.cfg
```

## Curl Requet: Create new connection every time
```
while true; do
   curl -X GET 127.0.0.1:8001  -H "Connection: keep-alive" -H "Keep-Alive: timeout=5, max=100"
done
```

Telnet Solution: Avoid creating new request everytime
```
while :;do echo -e "GET / HTTP/1.1\nhost: localhost\n\n";sleep 1;done|telnet 127.0.0.1 8001
```