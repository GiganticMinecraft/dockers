FROM adoptopenjdk:8u282-b08-jdk-openj9-0.24.0

# sbt をインストールする (https://www.scala-sbt.org/1.x/docs/ja/Installing-sbt-on-Linux.html)
RUN apt-get update && apt-get upgrade -y

# apt-key addに必要
RUN apt-get install -y gnupg

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" |\
    apt-key add && \
    apt-get update && apt-get upgrade -y

RUN apt-get install -y sbt=1.4.9
# sbt launcherがsbtをDLしてくれる
RUN sbt --version

# adoptopenjdk:8u282-b08-jdk-openj9-0.24.0 にはgitがインストールされておらず、CIの利用には不便
RUN apt-get install -y git
