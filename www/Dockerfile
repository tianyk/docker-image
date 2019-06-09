FROM node:10-alpine

WORKDIR /usr/src/app

RUN apk add --no-cache git \
    && git clone https://github.com/tianyk/note.git \
    && apk del git \
    && cd note \ 
    && npm i \
    && npx hexo g 

WORKDIR /usr/src/app/note

EXPOSE 8080
CMD [ "npx",  "http-server", "-s" "-p 8080", "./public" ]