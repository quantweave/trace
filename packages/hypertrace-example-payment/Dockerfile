FROM openjdk:8-jdk-alpine
RUN apk --no-cache add curl
COPY target/hypertrace-example-payment-0.1.0-SNAPSHOT.jar app.jar
RUN curl --insecure -L -o hypertrace-agent-1.1.10-all.jar https://github.com/hypertrace/javaagent/releases/download/1.1.10/hypertrace-agent-1.1.10-all.jar
RUN chmod a+x /app.jar /hypertrace-agent-1.1.10-all.jar
ENTRYPOINT ["sh", "-c", "java -javaagent:/hypertrace-agent-1.1.10-all.jar ${JAVA_OPTS} -jar /app.jar"]