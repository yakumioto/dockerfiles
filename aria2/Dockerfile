FROM alpine:latest

LABEL maintainer="yakumioto <yaku.mioto@gmail.com>"

RUN set -ex \
    && apk update \
    && apk add --no-cache curl wget aria2

WORKDIR /downloads