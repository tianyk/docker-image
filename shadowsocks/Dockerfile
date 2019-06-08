FROM golang:1.12-alpine

RUN apk add --no-cache git mercurial \
    && go get github.com/shadowsocks/shadowsocks-go/cmd/shadowsocks-server \
    && apk del git mercurial
    
COPY ss.json /etc/ss.json

EXPOSE 4433
CMD [ "shadowsocks-server", "-c", "/etc/ss.json" ]