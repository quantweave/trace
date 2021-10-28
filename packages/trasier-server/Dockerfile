FROM openjdk:11.0.12-slim
ENV version=0.3
COPY build/libs/trasier-server-$version-all.jar /trasier/
RUN chmod a+x /trasier/trasier-server-$version-all.jar

EXPOSE 8080
CMD java -Djava.security.egd=file:/dev/urandom ${JAVA_OPTS} -jar /trasier/trasier-server-$version-all.jar

