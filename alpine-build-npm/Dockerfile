FROM bhuisgen/alpine-build:latest
MAINTAINER Boris HUISGEN <bhuisgen@hbis.fr>

RUN apk add --update --repository http://dl-3.alpinelinux.org/alpine/edge/main/ --allow-untrusted nodejs && \
    rm -rf /var/cache/apk/*

COPY root /

ENTRYPOINT ["/init"]
CMD []
