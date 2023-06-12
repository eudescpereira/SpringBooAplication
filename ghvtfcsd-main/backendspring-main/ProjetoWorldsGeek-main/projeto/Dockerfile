FROM maven:3.8.7-amazoncorretto-17 AS build
COPY . .
RUN mvn clean package

FROM amazoncorretto:17
COPY --from=build /target/spring-bootapplication-0.0.1.jar spring-bootapplication-0.0.1.jar

EXPOSE 8080
ENTRYPOINT ["java", "-jar", "spring-bootapplication-0.0.1.jar"]
