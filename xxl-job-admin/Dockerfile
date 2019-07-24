#FROM openjdk:7-jre-slim
FROM openjdk:8-jre-alpine
MAINTAINER zhuCan

ENV PARAMS=""

ENV TZ=PRC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD target/xxl-job-admin-*.jar /app.jar

ENTRYPOINT ["sh","-c","java -jar /app.jar $PARAMS"]

EXPOSE 8995