# jobportalbackend

This mongo DB image will allow all the user to connect and read/write data
hence DB username and password is not required

To dockerize application
Application.properties
spring.data.mongodb.host=host.docker.internal
spring.data.mongodb.port=27017

Dokerfile
FROM openjdk:18
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/app.jar"]

Commands
  23 mvn clean compile
  24 ./mvnw clean
  25 mvn clean compile
  26 mvn clean install
  27 mvn spring-boot:run
  28 mvn clean install
  29 docker build -t springbootimg .
  30 docker images
  31 docker pull mongo
  32 docker images
  33 docker run -d --name mongo-on-docker -p 27017:27017 mongo
  34 docker run -d --name springapplication-on-docker -p 8080:8080 springbootimg
  35 docker run -d --name react-on-docker -p 3000:3000 react
Docker images
 
Docker container: Running image in docker container
 



 

 

Pushed image to docker hub
  38 docker images
  39 docker tag a108904af6b6 pankajdets/springbootimg
  40 docker push pankajdets/springbootimg
  41 docker tag c8b57c4bf7e3  pankajdets/mongo
  42 docker push pankajdets/mongo
 

Docker compose file to start all 3 services using one single command
 
docker compose up
 
