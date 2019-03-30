FROM greatbsky/openjdk:latest
MAINTAINER architect.bian
LABEL name="elasticsearch" license="MIT" build-date="20190330"

ENV VERSION 6.7.0
ENV USER elastic
ENV GROUP elastic

RUN groupadd -r $GROUP && useradd -r -g $GROUP $USER && cd /data/softs && wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-$VERSION.tar.gz && tar -zxf elasticsearch-$VERSION.tar.gz && mkdir -p /data/env/elastic/search && mv elasticsearch-$VERSION/* /data/env/elastic/search && chown -R $USER:$GROUP /data/env/elastic/ && rm -rf /data/softs/*

export ES_JAVA_OPTS="-Des.cgroups.hierarchy.override=/ $ES_JAVA_OPTS"
EXPOSE 9200
WORKDIR /data/env/elastic/search
USER $USER

CMD ["bin/elasticsearch"]