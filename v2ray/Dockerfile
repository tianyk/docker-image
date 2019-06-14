FROM alpine:latest

RUN bash <(curl -L -s https://install.direct/go.sh)

COPY config.json /etc/v2ray.json 

CMD ["v2ray", "-config=/etc/v2ray.json"]