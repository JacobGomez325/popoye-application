#first stage
FROM maven:3.8.4-jdk-11 AS builer
WORKDIR /app
COPY pom.xml ./
RUN mvn dependency:resolve
RUN mvn package
COPY . .

#second stage
FROM openjdk:11-jre-slim
CMD java -jar worker-jar-with-dependencies.jar