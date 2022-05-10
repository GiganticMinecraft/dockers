FROM adoptopenjdk:8u282-b08-jdk-openj9-0.24.0

# sbt をインストールする (https://www.scala-sbt.org/1.x/docs/ja/Installing-sbt-on-Linux.html)
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y apt-transport-https curl gnupg

RUN echo "deb https://repo.scala-sbt.org/scalasbt/debian all main" | tee /etc/apt/sources.list.d/sbt.list
RUN echo "deb https://repo.scala-sbt.org/scalasbt/debian /" | tee /etc/apt/sources.list.d/sbt_old.list
RUN curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" \
    | sudo -H gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/scalasbt-release.gpg --import
RUN chmod 644 /etc/apt/trusted.gpg.d/scalasbt-release.gpg

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y sbt=1.6.2

# sbt launcherがsbtをDLしてくれる
RUN sbt --version

# adoptopenjdk:8u282-b08-jdk-openj9-0.24.0 にはgitがインストールされておらず、CIの利用には不便
RUN apt-get install -y git
