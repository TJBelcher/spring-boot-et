#  FROM maven:3.8.4-openjdk-11-slim as BUILDER
#  cd c:/users/tom/documents/spring-boot-et/booting-web
#  docker build --platform windows/amd64 -t booting-web .
#  docker build -t booting-web .
FROM maven:3.6.3-openjdk-11-slim as BUILDER
#  FROM maven:3.8.4-openjdk-11-slim as BUILDER
ARG VERSION=0.0.1-SNAPSHOT
WORKDIR /build/
COPY pom.xml /build/
COPY src /build/src/

RUN mvn clean package
# RUN mvn clean package  
# COPY target/booting-web-${VERSION}.jar target/application.jar 

# FROM openjdk:11.0.8-jre-slim
# WORKDIR /app/

# COPY --from=BUILDER /build/target/application.jar /app/
# CMD java -jar /app/application.jar
