# syntax=docker/dockerfile:1
FROM eclipse-temurin:17.0.18_8-jdk-noble

# sbt をインストールする (https://www.scala-sbt.org/1.x/docs/ja/Installing-sbt-on-Linux.html)
RUN \
    --mount=type=cache,target=/var/lib/apt,sharing=locked \
    --mount=type=cache,target=/var/cache/apt,sharing=locked \
    apt-get update && apt-get install -y --no-install-recommends \
    curl

RUN <<EOF cat > /etc/apt/sources.list.d/sbt.list
deb https://repo.scala-sbt.org/scalasbt/debian all main
EOF

RUN <<EOF cat > /etc/apt/sources.list.d/sbt_old.list
deb https://repo.scala-sbt.org/scalasbt/debian /
EOF

RUN curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" \
    -o /etc/apt/trusted.gpg.d/sbt.asc

RUN \
    --mount=type=cache,target=/var/lib/apt,sharing=locked \
    --mount=type=cache,target=/var/cache/apt,sharing=locked \
    apt-get update && apt-get install -y --no-install-recommends \
    sbt=1.11.7 \
    git

# sbt launcherがsbtをDLしてくれる
RUN sbt --version
