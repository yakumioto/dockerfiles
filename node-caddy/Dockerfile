FROM node

ARG version="0.10.10"
ARG plugins="http.git"

LABEL maintainer="Mioto Yaku <yaku.mioto@gmail.com>"

RUN curl -fsSL "https://caddyserver.com/download/linux/amd64?plugins=${plugins}&license=personal" -o caddy.tar.gz \
    && $(mkdir caddy && cd caddy && tar -xzf ../caddy.tar.gz && mv caddy /usr/bin) \
    && rm -rf caddy.tar.gz caddy

WORKDIR /srv

ENTRYPOINT ["/usr/bin/caddy"]
CMD ["--conf", "/etc/Caddyfile", "--log", "stdout"]