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
$ flyctl launch
$ flyctl deploy
```

### reference
- https://spring.io/guides/topicals/spring-boot-docker/