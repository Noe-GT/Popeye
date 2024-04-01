FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder

RUN mkdir /worker_app

WORKDIR /worker_app

COPY . /worker_app

RUN mvn dependency:resolve

RUN mvn package

FROM eclipse-temurin:21-jre-alpine

WORKDIR /worker_app

COPY --from=builder /worker_app/target/worker-jar-with-dependencies.jar ./

CMD ["java", "-jar" , "worker-jar-with-dependencies.jar"]
