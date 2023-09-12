# Étape de BUILD - Utiliser une image Maven avec Java 17 pour la compilation
FROM maven:3.8.5-openjdk-17 AS build

WORKDIR /workspace

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src ./src
RUN mvn clean package

# Étape de RUN - Utiliser une image OpenJDK légère pour l'exécution
FROM openjdk:17-jdk-slim

WORKDIR /app

COPY --from=build /workspace/target/backend-*.jar ./app.jar

CMD ["java", "-jar", "app.jar"]
