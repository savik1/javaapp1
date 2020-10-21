# Use a minimal image as parent
FROM openjdk:8-jdk-alpine

# instal db config
WORKDIR /opt/ROOT
RUN wget https://github.com/savik1/App42PaaS-Java-MySQL-Sample/blob/master/WebContent/Config.properties

WORKDIR /opt

# install tomcat
RUN wget https://apache-mirror.rbc.ru/pub/apache/tomcat/tomcat-8/v8.5.59/bin/apache-tomcat-8.5.59.tar.gz && \
    tar xvzf apache-tomcat-8.5.59.tar.gz && \
    mv apache-tomcat-8.5.59 tomcat

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
