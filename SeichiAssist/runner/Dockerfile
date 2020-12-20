FROM openjdk:8-jdk

RUN apt-get update
RUN apt-get install nkf
ADD https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 /usr/bin/yq
RUN chmod +x /usr/bin/yq

