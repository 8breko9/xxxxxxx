# Etap 1: Pobieranie zależności
FROM maven:3.8 AS deps
WORKDIR /app
COPY pom.xml .
RUN mvn dependency:resolve

# Etap 2: Budowanie aplikacji
FROM deps
COPY src ./src
RUN mvn package