FROM greatbsky/openjdk:latest
MAINTAINER architect.bian
LABEL name="logstash" license="MIT" build-date="20190326"

ENV VERSION 6.6.2

RUN cd /data/softs && wget https://artifacts.elastic.co/downloads/logstash/logstash-$VERSION.tar.gz && tar -zxf logstash-$VERSION.tar.gz && mkdir -p /data/env/elastic/logstash && mv logstash-$VERSION/* /data/env/elastic/logstash && rm -rf /data/softs/*

EXPOSE 5044
EXPOSE 9600
WORKDIR /data/env/elastic/logstash

CMD ["bin/logstash"]