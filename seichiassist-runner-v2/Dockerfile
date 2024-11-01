FROM mikefarah/yq:4.44.3 as yq
FROM eclipse-temurin:17.0.13_11-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
