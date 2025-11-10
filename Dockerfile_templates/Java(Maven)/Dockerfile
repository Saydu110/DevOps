# build
FROM maven:3.9.0-eclipse-temurin-17 AS build
WORKDIR /build
COPY pom.xml .
COPY src ./src
RUN mvn -q -DskipTests package

# runtime
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY --from=build /build/target/myapp.jar ./app.jar
EXPOSE 8080
CMD ["java", "-jar", "app.jar"]
