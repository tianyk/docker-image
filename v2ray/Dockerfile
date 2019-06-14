FROM alpine:latest

RUN apk add --no-cache curl 
RUN curl -L -s https://install.direct/go.sh | sh  

COPY config.json /etc/v2ray.json 

CMD ["v2ray", "-config=/etc/v2ray.json"]