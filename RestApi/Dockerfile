FROM java:8
FROM maven:alpine

MAINTAINER Dipankar Dutta

WORKDIR /app


COPY . /app

#RUN chmod +x ./start.sh
#RUN chmod +x ./wait-for-it.sh

RUN mvn -v

RUN mvn clean install -DskipTests

EXPOSE 8080



#ADD ./target/RestApi-0.0.1-SNAPSHOT.jar RestApi-0.0.1-SNAPSHOT.jar
ADD /root/.m2/repository/com/example/RestApi/0.0.1-SNAPSHOT/RestApi-0.0.1-SNAPSHOT.jar RestApi-0.0.1-SNAPSHOT.jar 

#ENTRYPOINT ["./start.sh"]

ENTRYPOINT ["java","-jar","RestApi-0.0.1-SNAPSHOT.jar"]


#From openjdk:8
#copy ./target/MyRestApi-0.0.1-SNAPSHOT.jar MyRestApi-0.0.1-SNAPSHOT.jar

#ENTRYPOINT ["java","-jar","MyRestApi-0.0.1-SNAPSHOT.jar"]
