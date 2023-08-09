# titanic
타이타닉 ML 서비스 MAS SpringBoot API
![LGTM](https://i.lgtm.fun/2j9q.gif)

# Architecture
<img width="841" alt="architect" src="https://github.com/jungssg/titanic/assets/131239981/8bb39af3-79e3-4894-9d81-d9998cc629de">

# DEV
### stack
- java 17
- gradle 8.2.1
- springboot 3.1.2
- docker
  
### build
- gradle clean build

### test
- gradle tast

### package
- gradle bootJar

### package & run
- gradle bootJar
- java -jar build/libs/titanic-user-api-0.0.1.jar

# DEPLOY
- fly.io + docker
```
$ floy login
# Create and configure a new app from source code or a Docker image.
$ fly launch
$ fly deploy
```
-docker
```
$ docker build -t titanic-user-api:0.0.1 .
$ docker images titanic-user-api
REPOSITORY          TAG       IMAGE ID       CREATED          SIZE
titanic-user-api   0.0.1     85e89f18771d   21 seconds ago   326MB

$ docker run -d --name titanic-user-api-001 -p 8090:8090 titanic-user-api:0.0.1

$ docker ps                      
CONTAINER ID   IMAGE                     COMMAND                CREATED          STATUS          PORTS                           
            NAMES
a5d74c4c95c5   titanic-user-api:0.0.1   "java -jar /app.jar"   20 seconds ago   Up 19 seconds   0.0.0.0:8090->8090/tcp, :::8090->8090/tcp   titanic-user-api-001
```
### reference
- https://spring.io/guides/topicals/spring-boot-docker/

