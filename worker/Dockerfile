#first stage
FROM maven:3.8.4-jdk-11 AS builer
WORKDIR /app
COPY . .
RUN mvn dependency:resolve
RUN mvn package

#second stage
FROM openjdk:11-jre-slim
RUN java -jar worker-jar-with-dependencies.jar