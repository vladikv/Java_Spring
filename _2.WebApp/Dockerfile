
FROM eclipse-temurin:26-jdk-alpine

# Робоча директорія в контейнері
WORKDIR /app

# Копіюємо зібраний JAR
COPY target/spu123.jar app.jar

# Порт Spring Boot
EXPOSE 8080

# Запуск
CMD ["java", "-jar", "app.jar"]