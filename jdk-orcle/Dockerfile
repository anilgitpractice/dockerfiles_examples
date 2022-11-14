# this docker file  is for building jdk-orcle image 
FROM komljen/ubuntu

MAINTAINER anil anilserfexel@gmail.com

ENV JAVA_VERSION 7
RUN apt-get install --reinstall ca-certificates

RUN \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get -y install \
          oracle-java${JAVA_VERSION}-installer && \
  echo oracle-java${JAVA_VERSION}-installer shared/accepted-oracle-license-v1-1 select true \
       | /usr/bin/debconf-set-selections && \
  rm -rf /var/lib/apt/lists/* && \
  rm /var/cache/oracle-jdk${JAVA_VERSION}-installer/jdk-*.tar.gz

RUN update-alternatives --display java
