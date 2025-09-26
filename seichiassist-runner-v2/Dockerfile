FROM mikefarah/yq:4.47.2 as yq
FROM eclipse-temurin:25-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
