FROM openjdk:11.0.12-slim
COPY build/libs/trasier-server-0.1-all.jar /trasier/
RUN chmod a+x /trasier/trasier-server-0.1-all.jar

EXPOSE 8080
CMD java -XX:+UnlockExperimentalVMOptions -Dcom.sun.management.jmxremote -noverify ${JAVA_OPTS} -jar /trasier/trasier-server-0.1-all.jar

