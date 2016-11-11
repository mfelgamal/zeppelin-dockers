FROM mahmoudelgamal/zeppelin-base:latest
MAINTAINER Mahmoud Elgamal <mahmoudf.elgamal@gmail.com>


RUN apk update && apk upgrade && \
    apk add --no-cache git tar openjdk7 nodejs ttf-dejavu fontconfig && \
    curl -L https://npmjs.org/install.sh | sh && npm install --silent -g gulp-cli grunt-cli bower && \
    wget http://www.eu.apache.org/dist/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz && \
    tar -zxf apache-maven-3.3.9-bin.tar.gz -C /usr/local/ && ln -s /usr/local/apache-maven-3.3.9 /usr/local/mvn && \
    rm -rf /var/cache/apk/*

ENV M2_HOME=/usr/local/mvn
ENV M2=$M2_HOME/bin
ENV PATH $PATH:$M2_HOME:$M2

RUN git clone https://git-wip-us.apache.org/repos/asf/zeppelin.git "/usr/local/zeppelin" && cd /usr/local/zeppelin/ && git checkout v0.6.1 && mvn clean package -DskipTests


