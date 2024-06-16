FROM mikefarah/yq:4.44.2 as yq
FROM eclipse-temurin:17.0.11_9-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
