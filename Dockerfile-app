FROM gradle:7.6.1-jdk17  AS builder 
WORKDIR /bmart-app
COPY gradlew . 
COPY gradle gradle 
COPY build.gradle .
COPY settings.gradle . 
COPY src src
RUN chmod +x ./gradlew 
RUN ./gradlew build

FROM openjdk:17-alpine
COPY --from=builder /bmart-app/build/libs/*.jar app.jar

ENTRYPOINT ["java","-jar","/app.jar"] 
