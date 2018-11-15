FROM greatbsky/xtraos:latest
MAINTAINER architect.bian
LABEL name="ethereum" license="MIT" build-date="20181115"

RUN yum update -y && cd /data/softs && wget https://gethstore.blob.core.windows.net/builds/geth-linux-amd64-1.8.18-58632d44.tar.gz && tar -zvxf geth-linux-amd64-1.8.18-58632d44.tar.gz && install -m 0755 -o root -g root -t /usr/bin geth-linux-amd64-1.8.18-58632d44/geth && rm -rf /data/softs/*
COPY geth.conf /root/.ethereum/geth.conf
RUN sed -i '$d' /etc/rc.local && echo 'geth --config /root/.ethereum/geth.conf' >> /etc/rc.local

CMD ["/etc/rc.local"]
