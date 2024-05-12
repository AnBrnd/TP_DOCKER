FROM openjdk:21

WORKDIR /app

COPY . /usr/src/app
COPY application-docker.properties /usr/src/app/

EXPOSE 8080

CMD ["java", "-jar", "bff.jar"]


