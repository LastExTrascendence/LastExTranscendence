FROM redis
COPY --chmod=644 conf/redis.conf /usr/local/etc/redis/redis.conf
CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]

# FROM alpine:3.18

# RUN apk upgrade --no-cache && \
#     apk add --no-cache  redis

# COPY --chmod=644 conf/redis.conf /etc/redis.conf

# ENTRYPOINT ["redis-server", "/etc/redis.conf"]

# STOPSIGNAL SIGQUIT
