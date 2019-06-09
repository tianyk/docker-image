FROM node:10-alpine

WORKDIR /usr/src/app

COPY www www 

RUN apk add --no-cache git \
    && git clone https://github.com/tianyk/note.git \
    && apk del git \
    && chmod +x www 

EXPOSE 8080
CMD [ "./www" ]