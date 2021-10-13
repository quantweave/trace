FROM openjdk:8-jdk-alpine
COPY target/trasier-example-offer-0.1.0-SNAPSHOT.jar app.jar
RUN chmod a+x /app.jar
ENTRYPOINT ["sh", "-c", "java ${JAVA_OPTS} -jar /app.jar"]