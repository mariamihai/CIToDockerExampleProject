FROM openjdk:11-jre-slim as builder

#Defined by the Maven Build Arguments in POM File
ARG ARTIFACT_ID
ARG JAR_FILE

WORKDIR application
ADD ./target/${JAR_FILE} ${ARTIFACT_ID}.jar
#RUN java -Djarmode=layertools -jar ${project.artifactId}.jar extract

FROM openjdk:11-jre-slim
LABEL PROJECT_NAME=${project.artifactId} \
      PROJECT=${project.id}

EXPOSE 8080

WORKDIR application
COPY --from=builder application/dependencies/ ./
COPY --from=builder application/spring-boot-loader/ ./
COPY --from=builder application/snapshot-dependencies/ ./
COPY --from=builder application/application/ ./
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "org.springframework.boot.loader.JarLauncher"]