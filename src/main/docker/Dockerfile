FROM openjdk:11-jre-slim

ARG JAR_FILE

ADD maven/${JAR_FILE} app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "./app.jar"]
