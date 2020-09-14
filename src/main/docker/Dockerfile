FROM openjdk:11-jre-slim

ARG ARTIFACT_ID
ARG JAR_FILE

ADD ./target/${JAR_FILE} ${ARTIFACT_ID}.jar

RUN echo ${JAR_FILE}
RUN echo ./target

RUN sleep 5

COPY ${ARTIFACT_ID}.jar app.jar

RUN sleep 5

RUN echo $(ls)

EXPOSE 8080

#ENTRYPOINT ["java", "-jar", "./app.jar"]
