FROM eclipse-temurin:17.0.7_7-jdk-jammy

RUN apt-get update && apt-get install nkf
ADD https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 /usr/bin/yq
RUN chmod +x /usr/bin/yq
