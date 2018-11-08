# Answers

Nom: TEXIER
Prénom: Hadrien
NB: 2

## 1.3
command: docker run -it --rm --name my-running-app my-python-app

## 1.4
answer: Les ports ne sont pas ouverts
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp my-python-app


## 1.5
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine  my-python-app

## 1.6
answer: Le nom de l'image ne correspond au repo il faut donc faire un docker tag
command:docker tag 408808fb1a9e docker.com/hadtex/dockert2pece
docker push hadtex/dockert2pece


## 1.7
answer: l'image n'est pas en local donc il la pull
command: docker rmi -f  [NUMIMAGE]
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine  hadtex/dockert2pece
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine -d hadtex/dockert2pece

## 1.8
answer: my-ruining-app et id ebcf709953f5
command: docker ps
command: docker restart ebcf709953f5
docker rename ebcf709953f5 sens


## 1.9
answer: docker exec -it ebcf709953f5 cat /etc/*release
answer: NAME="Alpine Linux"

## 1.11
command: You called at : 2018-11-08 13:50:39.092742 (dynamic)
        On environment : python:3-alpine (from env variable)
        With path : bonjour   (from URL path)
        With front : 8b1f466d4822 (from real hostname of front service)
        With back  : a55d101a7459 (from real hostname of back service
answer: docker run -it --rm --name my-running-app -p 8081:8081/tcp -p 8081:8081/udp -e APP_PORT=8081 -e WS_BACK_URL=0.0.0.0 my-python-app

## 2.1
command:

## 2.6
command:
command:

command: 
command: 

## 2.9
command: 
