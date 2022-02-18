FROM ghcr.io/perara-docker/hadoop/base:hadoop$HADOOP_VERSION-java$JAVA_VERSION

MAINTAINER Per-Arne Andersen <per.andersen@uia.no>

HEALTHCHECK CMD curl -f http://localhost:8042/ || exit 1

ADD run.sh /run.sh
RUN chmod a+x /run.sh

EXPOSE 8042

CMD ["/run.sh"]
