# tatiatic-user-api
타이타닉 ML 서비스 MAS SpringBoot API

![LGTM](https://i.lgtm.fun/2j9j.png)

# Architecture
- user-api : https://github.com/blahxblah/titanic / https://titanic-user-api-kjh.fly.dev
- webapp : https://github.com/blahxblah/titanic-webapp / https://titanic-webapp-kjh.fly.dev
- ml-api : https://github.com/blahxblah/titanic-ml-api / https://titanic-ml-api-kjh.fly.dev

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
$ flyctl launch
$ flyctl deploy
```
- docker
```
$ docker build -t titanic:0.1.0 .
$ docker images titanic
REPOSITORY   TAG       IMAGE ID       CREATED          SIZE
titanic      0.1.0     6f01351e6fc3   21 seconds ago   326MB

$ docker run -d --name titanic-api-010 -p 9010:9876 titanic:0.1.0

$ docker ps                      
CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                                              NAMES
093d80e9536e   titanic:0.1.0           "java -jar /app.jar"     4 minutes ago   Up 4 minutes   0.0.0.0:9010->9876/tcp                             titanic-api-010
```

### reference
- https://spring.io/guides/topicals/spring-boot-docker/
