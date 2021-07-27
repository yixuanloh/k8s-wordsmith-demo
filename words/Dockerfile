# RUN
FROM adoptopenjdk:8-jre

WORKDIR /app
COPY codestory/words/1.0-SNAPSHOT/words-1.0-20210727.030607-1.jar /app

ENTRYPOINT ["java", "-Xmx8m", "-Xms8m", "-jar", "/app/words-1.0-20210727.030607-1.jar"]
EXPOSE 8080


