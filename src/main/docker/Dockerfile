FROM openjdk:11-jre-slim

ARG ARTIFACT_ID
ARG JAR_FILE

ADD maven/${JAR_FILE} ${ARTIFACT_ID}.jar

RUN echo $(ls)
RUN echo ${JAR_FILE}

RUN sleep 5


ADD maven/${JAR_FILE} app.jar

RUN sleep 5

RUN echo $(ls)

EXPOSE 8080

#ENTRYPOINT ["java", "-jar", "./app.jar"]
