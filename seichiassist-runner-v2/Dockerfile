FROM mikefarah/yq:4.45.4 as yq
FROM eclipse-temurin:17.0.15_6-jdk-jammy

RUN apt-get update && apt-get install nkf \
    && rm -rf /var/lib/apt/lists/*
COPY --from=yq /usr/bin/yq /usr/bin/yq
