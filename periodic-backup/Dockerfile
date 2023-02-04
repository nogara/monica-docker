FROM alpine:latest

RUN apk update && \
    apk upgrade && \
    apk add --no-cache mariadb-client

COPY ./scripts/daily/* /etc/periodic/daily

RUN chmod a+x /etc/periodic/daily/*
