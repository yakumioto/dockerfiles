FROM ubuntu:17.10

LABEL maintainer="yakumioto <yaku.mioto@gmail.com>"

ARG version="3.1.0"

RUN apt update \
    && apt-get install -y --no-install-recommends \
                shadowsocks-libev \
                build-essential \
                autoconf \
                libtool \
                libssl-dev \
                libpcre3-dev \
                libc-ares-dev \
                libev-dev \
                asciidoc \
                xmlto \
                automake \
                git \
    && git clone https://github.com/shadowsocks/simple-obfs.git \
    && (cd simple-obfs \
    && git submodule update --init --recursive \
    && ./autogen.sh && ./configure \
    && make && make install) \
    && rm simple-obfs && apt-get clean && apt-get autoclean