FROM openjdk:11-jre-slim
ARG ARTIFACT_ID
ARG PROJECT_ID
ARG JAR_FILE

WORKDIR application
ADD ./target/${JAR_FILE} ${ARTIFACT_ID}.jar

FROM openjdk:11-jre-slim
LABEL PROJECT_NAME=${ARTIFACT_ID} \
      PROJECT=${PROJECT_ID}

EXPOSE 8080

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "org.springframework.boot.loader.JarLauncher"]