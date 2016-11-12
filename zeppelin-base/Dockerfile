FROM alpine:3.4
MAINTAINER Mahmoud Elgamal <mahmoudf.elgamal@gmail.com>

ENV SCALA_VERSION="2.11.8"
ENV SCALA_HOME="/usr/share/scala"
ENV JAVA_HOME /usr/lib/jvm/java-1.7-openjdk
ENV PATH $PATH:$JAVA_HOME/bin

RUN apk add --update bash curl openjdk7-jre wget ca-certificates python build-base make gcc g++ java-cacerts openssl && \
    rm /usr/lib/jvm/java-1.7-openjdk/jre/lib/security/cacerts && \
    ln -s /etc/ssl/certs/java/cacerts /usr/lib/jvm/java-1.7-openjdk/jre/lib/security/cacerts && \
    cd "/tmp" && \
    wget "https://downloads.typesafe.com/scala/${SCALA_VERSION}/scala-${SCALA_VERSION}.tgz" && \
    tar xzf "scala-${SCALA_VERSION}.tgz" && \
    mkdir "${SCALA_HOME}" && \
    rm "/tmp/scala-${SCALA_VERSION}/bin/"*.bat && \
    mv "/tmp/scala-${SCALA_VERSION}/bin" "/tmp/scala-${SCALA_VERSION}/lib" "${SCALA_HOME}" && \
    ln -s "${SCALA_HOME}/bin/"* "/usr/bin/" && \
    rm -rf "/tmp/"* && \
    curl --silent \
    --location https://github.com/sgerrand/alpine-pkg-R/releases/download/3.3.1-r0/R-3.3.1-r0.apk --output /var/cache/apk/R-3.3.1-r0.apk && \
    apk add --update --allow-untrusted /var/cache/apk/R-3.3.1-r0.apk && \
    curl --silent \
    --location https://github.com/sgerrand/alpine-pkg-R/releases/download/3.3.1-r0/R-dev-3.3.1-r0.apk --output /var/cache/apk/R-dev-3.3.1-r0.apk && \
    apk add --update --allow-untrusted /var/cache/apk/R-dev-3.3.1-r0.apk && \
    R -e "install.packages('knitr', repos = 'http://cran.us.r-project.org')" && \
    rm -rf /var/cache/apk/*

RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64
RUN chmod +x /usr/local/bin/dumb-init

# ports for zeppelin
EXPOSE 8080 8081 7077

ENTRYPOINT ["/usr/local/bin/dumb-init"]
