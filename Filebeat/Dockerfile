FROM greatbsky/centos7:latest
MAINTAINER architect.bian
LABEL name="filebeat" license="MIT" build-date="20190326"

ENV VERSION 6.6.2

RUN cd /data/softs && wget https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-$VERSION-linux-x86_64.tar.gz && tar -zxf filebeat-$VERSION-linux-x86_64.tar.gz && mkdir -p /data/env/elastic/filebeat && mv filebeat-$VERSION-linux-x86_64/* /data/env/elastic/filebeat && rm -rf /data/softs/*

WORKDIR /data/env/elastic/filebeat

CMD ["./filebeat"]