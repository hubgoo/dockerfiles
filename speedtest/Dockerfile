FROM alpine:3.11

RUN apk add --no-cache ca-certificates python3

ENV SPEEDTEST_VERSION 2.1.2

RUN pip3 install --no-cache-dir speedtest-cli==$SPEEDTEST_VERSION

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]

CMD ["speedtest-cli"]
