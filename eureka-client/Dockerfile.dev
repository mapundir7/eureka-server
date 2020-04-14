# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

WORKDIR '/app'

# Add Maintainer Info
MAINTAINER Manish Pundir <mapundir7@gmail.com>

# The application's jar file
# https://vsupalov.com/docker-arg-env-variable-guide/
ARG JAR_FILE=DockerEurekaClient-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} /app/app.jar

# Run the jar file
# http://www.littlebigextra.com/use-spring-profiles-docker-containers/ 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","app.jar"]