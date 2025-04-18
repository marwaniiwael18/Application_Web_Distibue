FROM openjdk:17-jdk-alpine
RUN apk --no-cache add curl
VOLUME /tmp
COPY target/config-server-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]