# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

WORKDIR '/appl'

# Add Maintainer Info
MAINTAINER Manish Pundir <mapundir7@gmail.com>

# Add a volume pointing to /tmp
VOLUME /appl/tmp

# Make port 8080 available to the world outside this container
#EXPOSE 8080

# The application's jar file
ARG JAR_FILE=websocket-demo-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} /appl/web-talk.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","-Dserver.port=8080","web-talk.jar"]

