FROM openjdk:11-jre-slim

ARG ARTIFACT_ID
ARG JAR_FILE

ADD ./target/${JAR_FILE} ${ARTIFACT_ID}.jar


RUN sleep 5

COPY ./target/${JAR_FILE} app.jar


RUN echo $(ls)

EXPOSE 8080

#ENTRYPOINT ["java", "-jar", "./app.jar"]
