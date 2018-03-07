FROM alpine:latest

LABEL maintainer="yakumioto <yaku.mioto@gmail.com>"

ARG version=0.13.0

RUN set -ex \
    && apk add --no-cache tar curl \
    && curl -sSL https://github.com/fatedier/frp/releases/download/v${version}/frp_${version}_linux_amd64.tar.gz | tar xz \
    && cd frp_${version}_linux_amd64 \
    && cp frpc frps /bin \
    && cd .. \
    && rm -rf frp_${version}_linux_amd64