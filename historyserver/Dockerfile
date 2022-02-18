ARG JAVA_VERSION
ARG HADOOP_VERSION
FROM ghcr.io/perara-docker/hadoop/base:hadoop$HADOOP_VERSION-java$JAVA_VERSION

MAINTAINER Per-Arne Andersen <per.andersen@uia.no>

HEALTHCHECK CMD curl -f http://localhost:8188/ || exit 1

ENV YARN_CONF_yarn_timeline___service_leveldb___timeline___store_path=/hadoop/yarn/timeline
RUN mkdir -p /hadoop/yarn/timeline
VOLUME /hadoop/yarn/timeline

ADD run.sh /run.sh
RUN chmod a+x /run.sh

EXPOSE 8188

CMD ["/run.sh"]
