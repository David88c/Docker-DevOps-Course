FROM maven:3-openjdk-11 AS build
WORKDIR /app
COPY pom.xml .
COPY src src
RUN mvn clean package

#FROM adoptopenjdk/openjdk11:jdk-11.0.9.1_1
WORKDIR /app
#COPY --from=build /app/target/jb-hello-world-maven-0.2.0.jar ./app.jar
CMD [ "java", "-jar", "jb-hello-world-maven-0.2.0.jar" ]



