FROM redis:6.0.9

COPY redis.conf /usr/local/etc/redis/redis.conf
COPY redis.override.conf /usr/local/etc/redis/redis.override.conf
WORKDIR /usr/local/etc/redis
RUN cat redis.conf redis.override.conf > tmpfile && mv tmpfile redis.conf

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]
