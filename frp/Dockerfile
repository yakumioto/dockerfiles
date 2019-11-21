FROM alpine:latest

LABEL maintainer="yakumioto <yaku.mioto@gmail.com>"

ARG version=0.29.1

RUN set -ex \
    && apk add --no-cache tar gzip curl \
    && curl -sSL https://github.com/fatedier/frp/releases/download/v${version}/frp_${version}_linux_amd64.tar.gz | tar xz \
    && cp frp_${version}_linux_amd64/frpc frp_${version}_linux_amd64/frps /usr/bin \
    && rm -rf frp_${version}_linux_amd64