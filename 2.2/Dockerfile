FROM mongo:2.2
MAINTAINER QingHai <qinghai@gmail.com>

RUN apt-get update && \
    apt-get install -y pwgen

VOLUME /data/db

ENV AUTH yes
ENV JOURNALING yes
ENV SMALLFILES no

ADD run.sh /run.sh
ADD set_mongodb_password.sh /set_mongodb_password.sh

EXPOSE 27017 28017

CMD ["/run.sh"]
