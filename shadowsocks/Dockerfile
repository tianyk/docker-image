FROM golang:1.12-alpine

RUN go get github.com/shadowsocks/shadowsocks-go/cmd/shadowsocks-server

COPY ss.json /etc/ss.json

EXPOSE 4433
CMD [ "shadowsocks-server", "-c", "/etc/ss.json" ]