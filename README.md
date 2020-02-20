# docker-traefik

1. Simple reverse-proxy ([docker-compose.yml](docker-compose.yml)):

To test the proxy run docker container and execute next command on the local :
```
curl -H Host:whoami.localhost http://localhost
Hostname: 3b64e9ee3e38
IP: 127.0.0.1
IP: 172.28.0.2
RemoteAddr: 172.28.0.3:55870
GET / HTTP/1.1
Host: whoami.localhost
User-Agent: curl/7.54.0
Accept: */*
Accept-Encoding: gzip
X-Forwarded-For: 172.28.0.1
X-Forwarded-Host: whoami.localhost
X-Forwarded-Port: 80
X-Forwarded-Proto: http
X-Forwarded-Server: a9dfe96d5877
X-Real-Ip: 172.28.0.1
```

To view the administration dashboard open browser and follow http://localhost:8080

2. Proxy with SSL using Let's Encrypt ([docker-compose-ssl.yml](docker-compose-ssl.yml)):

Will collect a free SSL certificates and save them into acme/acme.json file.

For test purposes uses Staging server. Comment line to use it in production.

3. Proxy with named and secured dashboard ([docker-compose-secure-dashboard.yml](docker-compose-secure-dashboard.yml))

4. Proxy redirected all requests to https scheme ([docker-compose-htts-redirect.yml](docker-compose-htts-redirect.yml))
