## Build 

```
docker build -t tianyk/shadowsocks:1.0.0 . 
```

### Run 

```
docker run --name shadowsocks --restart=always -d -p 4434:4433 tianyk/shadowsocks:1.0.0
```