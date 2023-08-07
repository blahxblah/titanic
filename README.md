# tatiatic-user-api
타이타닉 ML 서비스 MAS SpringBoot API

![LGTM](https://i.lgtm.fun/2j9j.png)

# Architecture
![image](https://github.com/dMario24/tatiatic-user-api/assets/134017660/31ade392-602a-4aaa-ba60-ea9ed8c40349)

# DEV
### stack
- java 17
- gradle 8.2.1
- springboot 3.1.2
- docker

### build
- gradle clean build

### test
- gradle test

### package
- gradle bootJar

### package & run
- gradle bootJar
- java -jar build/libs/titanic-0.1.0.jar

# DEPLOY
- fly.io + docker
```
# Create and configure a new app from source code or a Docker image.
$ fly launch
```
- docker
```
$ docker build -t tatiatic-user-api:0.1.0 .
$ docker images tatiatic-user-api
REPOSITORY          TAG       IMAGE ID       CREATED          SIZE
tatiatic-user-api   0.1.0     85e89f18771d   21 seconds ago   326MB

$ docker run -d --name tatiatic-user-api-010 -p 9010:9876 tatiatic-user-api:0.1.0

$ docker ps                      
CONTAINER ID   IMAGE                     COMMAND                CREATED          STATUS          PORTS                           
            NAMES
a5d74c4c95c5   tatiatic-user-api:0.1.0   "java -jar /app.jar"   20 seconds ago   Up 19 seconds   0.0.0.0:9010->9876/tcp, :::9010->9876/tcp   tatiatic-user-api-010
```

### reference
- https://spring.io/guides/topicals/spring-boot-docker/
