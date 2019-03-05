FROM greatbsky/centos7:latest
MAINTAINER architect.bian
LABEL name="RabbitMQ" license="MIT" build-date="20190305"

ENV VERSION 3.7.12

RUN yum update -y && cd /data/softs && wget https://dl.bintray.com/rabbitmq-erlang/rpm/erlang/21/el/7/x86_64/erlang-21.2.6-1.el7.x86_64.rpm && rpm -ivh erlang-21.2.6-1.el7.x86_64.rpm && yum install socat logrotate && wget https://dl.bintray.com/rabbitmq/all/rabbitmq-server/3.7.12/rabbitmq-server-generic-unix-3.7.12.tar.xz && xz -d rabbitmq-server-generic-unix-3.7.12.tar.xz && tar -vxf rabbitmq-server-generic-unix-3.7.12.tar && mv rabbitmq_server-3.7.12 /data/env/ && install -m 0755 -o root -g root -t /usr/bin /data/env/rabbitmq_server-3.7.12/sbin/* && rm -rf /data/softs/*

CMD ["rabbitmq-server"]
