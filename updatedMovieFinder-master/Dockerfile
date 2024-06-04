FROM maven:3.8.5-openjdk-19 AS build
COPY . .


FROM openjdk:19.0.1-jdk-slim AS runtime
COPY --from=build /target/<movie-data-finder-0.0.1-SNAPSHOT> /app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app.jar"]