FROM mikefarah/yq:4.40.5 as yq
FROM eclipse-temurin:17.0.9_9-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
