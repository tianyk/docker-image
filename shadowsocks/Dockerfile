FROM python:2.7.5-alpine

RUN pip install shadowsocks

COPY ss.json /etc/ss.json

EXPOSE 4433
CMD [ "ssserver", "-d", "start", "-c", "/etc/ss.json" ]