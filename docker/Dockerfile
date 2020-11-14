FROM alpine
MAINTAINER Akira <e.akimoto.akira@gmail.com>

RUN set -ex \
        && apk update && apk upgrade\
<<<<<<< HEAD
        && apk add --no-cache tzdata git nodejs npm\
        && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
        && echo "Asia/Shanghai" > /etc/timezone

RUN git clone https://github.com/lxk0301/scripts /scripts \
=======
        && apk add --no-cache tzdata moreutils git nodejs npm\
        && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
        && echo "Asia/Shanghai" > /etc/timezone

RUN git clone https://github.com/lxk0301/jd_scripts /scripts \
>>>>>>> origin/main
        && cd /scripts \
        && mkdir logs \
        && npm install \
        && cd ~ \
        && npm install request

<<<<<<< HEAD
ENV CDN_JD_DAILYBONUS true

RUN crontab /scripts/docker/crontab_list.sh

WORKDIR /scripts

CMD ["node"]
=======
ENV CRONTAB_LIST_FILE crontab_list_ts.sh

RUN crontab /scripts/docker/crontab_list_ts.sh

WORKDIR /scripts

CMD ["node"]
>>>>>>> origin/main
