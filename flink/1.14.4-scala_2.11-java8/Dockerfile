FROM openjdk:8-jre

ENV FLINK_VERSION=1.14.4
ENV FLINK_HOME=/opt/flink-$FLINK_VERSION
ENV PATH=$FLINK_HOME/bin:$PATH

# 安装 flink
# ADD flink-1.14.4-bin-scala_2.11.tgz /opt/
RUN curl -s https://docker-1252933230.cos.ap-shanghai.myqcloud.com/soft/flink/flink-1.14.4-bin-scala_2.11.tgz \
    --output flink-1.14.4-bin-scala_2.11.tgz \
    && tar -xf flink-1.14.4-bin-scala_2.11.tgz -C /opt/ \
    && rm -rf flink-1.14.4-bin-scala_2.11.tgz

COPY flink-conf.yaml $FLINK_HOME/conf/

WORKDIR $FLINK_HOME

# 高可用目录 检查点目录
RUN mkdir -p /data/flink/ha \
    /data/flink/checkpoints \
    /data/flink/savepoints

# Configure container
COPY docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
EXPOSE 6123 8081
CMD ["help"]