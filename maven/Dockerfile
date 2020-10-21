FROM maven:3.6.0-alpine
RUN apk -U upgrade --update && \
    apk add git
WORKDIR /home/sampleTest
RUN git clone https://github.com/savik1/App42PaaS-Java-MySQL-Sample.git
WORKDIR /home/sampleTest/App42PaaS-Java-MySQL-Sample
RUN mvn package
RUN mkdir /home/war && cp ./target/App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT.war /home/war/
