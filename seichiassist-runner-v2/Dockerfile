FROM mikefarah/yq:4.40.7 as yq
FROM eclipse-temurin:17.0.10_7-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
