FROM openjdk:8-jdk-alpine
RUN apk --no-cache add curl
COPY target/apm-example-offer-0.1.0-SNAPSHOT.jar app.jar
RUN curl --insecure -L -o elastic-apm-agent-1.26.0.jar https://search.maven.org/remotecontent?filepath=co/elastic/apm/elastic-apm-agent/1.26.0/elastic-apm-agent-1.26.0.jar
RUN chmod a+x /app.jar /elastic-apm-agent-1.26.0.jar
ENTRYPOINT ["sh", "-c", "java -javaagent:/elastic-apm-agent-1.26.0.jar ${JAVA_OPTS} -jar /app.jar"]