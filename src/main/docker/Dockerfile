FROM openjdk:11-jre-slim

ARG JAR_FILE

COPY ./target/${JAR_FILE} app.jar

RUN echo $(ls)

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "/app.jar"]
