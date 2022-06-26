FROM gradle:jdk11 AS build

WORKDIR /app

COPY . ./

RUN ./gradlew build

FROM openjdk:11-jdk-slim-buster

# Set JAR_FILE
ARG JAR_FILE=app/build/libs/\*.jar

# Copy JAR
COPY --from=build ${JAR_FILE} /app/app.jar

# RUN APPLICATION
ENTRYPOINT [ "java", "-jar", "/app/app.jar" ]