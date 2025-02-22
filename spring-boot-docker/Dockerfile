FROM maven:3.8.7-eclipse-temurin-8 AS builder
RUN git clone https://github.com/kkenan/basic-microservices.git /repo \
 && cd /repo/spring-boot-app \
 && mvn clean package

FROM openjdk:8-jdk-alpine
COPY --from=builder /repo/spring-boot-app/target/spring-boot-app-1.0-SNAPSHOT.jar /spring-boot-app.jar

CMD ["java", "-jar", "/spring-boot-app.jar"]
