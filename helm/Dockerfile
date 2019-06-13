FROM alpine:latest

LABEL maintainer="yakumioto <yaku.mioto@gmail.com>"

ARG version=v2.14.0

RUN set -ex \
    && apk add --no-cache bash gzip curl openssl \
    && curl -LO https://git.io/get_helm.sh \
    && chmod 700 get_helm.sh \
    && ./get_helm.sh \ 
    && mkdir -p /root/.helm/repository/local \
    && rm -rf ./get_helm.sh

EXPOSE 8879

CMD [ "helm", "serve" ]