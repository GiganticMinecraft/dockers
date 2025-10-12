FROM mikefarah/yq:4.48.1 as yq
FROM eclipse-temurin:17.0.16_8-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
