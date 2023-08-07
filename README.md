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
$ fly login
# Create and configure a new app from source code or a Docker image.
$ fly launch
$ fly deploy
```
# DOCKER
```
$ docker build -t titanic-user-api-0.0.1.jar .
$ docker images titanic-user-api-0.0.1.jar
REPOSITORY                   TAG       IMAGE ID       CREATED          SIZE
titanic-user-api-0.0.1.jar   latest    375a99fea939   22 minutes ago   494MB

$ docker run --name titanic-api -p 8090:8090 titanic-user-api-0.0.1.jar

$ docker ps
CONTAINER ID   IMAGE                        COMMAND                CREATED          STATUS         PORTS                    NAMES
996f49a82075   titanic-user-api-0.0.1.jar   "java -jar /app.jar"   21 minutes ago   Up 6 seconds   0.0.0.0:8090->8090/tcp   titanic-api
```



### reference
- https://spring.io/guides/topicals/spring-boot-docker/

