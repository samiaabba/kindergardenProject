# Start with Maven and Java 17 installed
FROM maven:3.9-eclipse-temurin-17

WORKDIR /app

# Copy the build configuration and source code
COPY pom.xml .
COPY src ./src

# Build the Java application
RUN mvn -B package

EXPOSE 5002

# Start the generated JAR file
CMD ["java", "-jar", "target/teacherservice-1.0.0.jar"]