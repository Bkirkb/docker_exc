# build from the Maven image, which has a maven environment pre-configured
FROM maven:latest
#copy the application in
COPY . /build
#Change the working directory to where we are building the app
WORKDIR /build
#Use maven to build the application
RUN mvn clean package
#Create a new build stage from the Java image which has java installed already
FROM java:8
#Change the workdir to where the app will be installed
WORKDIR /opt/hello-world
#Copy the JAR file created previously
COPY --from=0 /build/target/hello-world-1.0.0.jar app.jar
#Create an entrypoint to run the application
ENTRYPOINT ["/usr/bin/java", "-jar", "app.jar"]

