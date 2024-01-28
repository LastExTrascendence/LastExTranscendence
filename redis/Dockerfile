# FROM redis

# COPY --chmod=644 conf/redis.conf /usr/local/etc/redis/redis.conf
# RUN mkdir -p /var/lib/redis && \
#     mkdir -p /var/log/redis/ && \
#     touch /var/log/redis/redis.log && \
#     chmod 777 /var/log/redis/redis.log

# CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]

FROM alpine:3.18

RUN apk upgrade --no-cache && \
    apk add --no-cache  redis && \
    mkdir -p /var/lib/redis && \
    mkdir -p /var/log/redis/ && \
    touch /var/log/redis/redis.log && \
    chmod 777 /var/log/redis/redis.log

COPY --chmod=644 conf/redis.conf /etc/redis.conf

ENTRYPOINT ["redis-server", "/etc/redis.conf"]

STOPSIGNAL SIGQUIT
