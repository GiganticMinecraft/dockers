# syntax=docker/dockerfile:1
FROM mikefarah/yq:4.52.2 as yq
FROM eclipse-temurin:17.0.18_8-jdk-noble

RUN \
    --mount=type=cache,target=/var/lib/apt,sharing=locked \
    --mount=type=cache,target=/var/cache/apt,sharing=locked \
    apt-get update && apt-get install -y --no-install-recommends \
    nkf
COPY --from=yq /usr/bin/yq /usr/bin/yq
