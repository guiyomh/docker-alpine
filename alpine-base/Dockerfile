FROM alpine:3.4
MAINTAINER Boris HUISGEN <bhuisgen@hbis.fr>

ENV S6OVERLAY_VERSION=v1.18.1.5 \
    S6_BEHAVIOUR_IF_STAGE2_FAILS=1 \
    LANG=en_US.UTF-8 \
    LC_ALL=en_US.UTF-8 \
    LANGUAGE=en_US.UTF-8 \
    TERM=xterm

RUN apk update && \
    apk upgrade && \
    apk add bash bind-tools ca-certificates curl jq tar && \
    curl -sSL https://github.com/just-containers/s6-overlay/releases/download/${S6OVERLAY_VERSION}/s6-overlay-amd64.tar.gz | tar xz -C / && \
    apk del tar && \
    rm -rf /var/cache/apk/* /src

COPY root /
