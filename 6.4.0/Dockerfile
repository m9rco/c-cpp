FROM m9rco/alpine:3.8
LABEL maintainer="m9rco <pushaowei0727@gmail.com>"
ARG GCC_VSERSION=gcc-6.4.0-r9
ARG GPP_VERSION=g++-6.4.0-r9


RUN apk add -U --no-cache ca-certificates \
    gcc=${GCC_VSERSION} \
    g++=${GCC_VSERSION} \
    && rm -rf /var/cache/apk/* 


ADD rootfs /
ENTRYPOINT ["/sbin/tini", "--"]

CMD ["/bin/sh"]

WORKDIR /app
