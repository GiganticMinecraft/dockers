FROM adoptopenjdk:8u282-b08-jdk-openj9-0.24.0

# adoptopenjdk:8u282-b08-jdk-openj9-0.24.0 にはgitがインストールされておらず、CIの利用には不便
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git
