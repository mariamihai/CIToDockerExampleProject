FROM openjdk:11-jre-slim

ARG ARTIFACT_ID
ARG PROJECT_ID
ARG JAR_FILE

ADD ./target/${JAR_FILE} ${ARTIFACT_ID}.jar

EXPOSE 8080

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "org.springframework.boot.loader.JarLauncher"]