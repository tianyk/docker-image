FROM openjdk:8-jre

RUN sed -i -E 's/(deb|security).debian.org/mirrors.aliyun.com/g' /etc/apt/sources.list \
    && apt update \
    && apt-get install gettext-base -y \
    && rm -rf /var/lib/apt/lists/*