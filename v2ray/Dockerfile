FROM alpine:latest

RUN apt-get update
RUN apt-get install curl -y
RUN bash <(curl -L -s https://install.direct/go.sh)

COPY config.json /etc/v2ray.json 

CMD ["v2ray", "-config=/etc/v2ray.json"]