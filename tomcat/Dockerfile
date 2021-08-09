FROM ubuntu:latest
RUN apt-get -y update && apt-get -y upgrade && apt-get -y install openjdk-8-jdk wget && mkdir /usr/local/tomcat
ARG TOMCAT_VERSION
RUN wget https://downloads.apache.org/tomcat/tomcat-8/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz  -O /tmp/tomcat.tar.gz

RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-$TOMCAT_VERSION/* /usr/local/tomcat/
EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run

