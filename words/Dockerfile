# RUN
FROM adoptopenjdk:8-jre

ENTRYPOINT ["java", "-Xmx8m", "-Xms8m", "-jar", "/app/words-1.0-20210729.032531-1.jar"]
EXPOSE 8080

WORKDIR /app
COPY words/codestory/words/1.0-SNAPSHOT/words-1.0-20210729.032531-1.jar .

