FROM alpine:3.9

ARG version="1.1.1-r0"

LABEL maintainer="Mioto Yaku <yaku.mioto@gmail.com>"

RUN echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories \
    && apk update \
    && apk add --no-cache polipo
ENTRYPOINT [ "polipo" ]