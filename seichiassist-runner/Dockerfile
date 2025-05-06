FROM mikefarah/yq:4.45.2 as yq
FROM adoptopenjdk:8u282-b08-jdk-hotspot

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
