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
# Create and configure a new app from source code or a Docker image.
$ fly launch
```

### reference
- https://spring.io/guides/topicals/spring-boot-docker/

