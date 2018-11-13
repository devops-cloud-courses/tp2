# Answers

Nom: Kourganoff
Prénom: Adrien
NB: 7

## 1.3
command: docker build -t my-python-app .
docker run NOM_IMAGE

## 1.4
answer: le port n'est pas ouvert 
command: docker run --rm -p 8080:8080 my-python-app   

## 1.5
command: docker run -e ENVIRONMENT='dev' --rm -p 8080:8080 my-python-app   

## 1.6
answer: parce que il 'y a pas de tag   
command: docker tag my-python-app yrandill/my-python-app
docker push yrandill/my-python-app

## 1.7
answer:
command: docker image rm NOM_IMAGE
command: docker pull yrandill/my-python-app
command: docker run -e ENVIRONMENT='dev' --rm -d -p 8080:8080 yrandill/my-python-app

## 1.8
answer: nom = admiring_panini
command: docker ps
command: docker run -e ENVIRONMENT='dev' --rm --name tp2-back -d -p 8080:8080 yrandill/my-python-app

## 1.9
answer: Debian 
answer:PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: docker run -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 --rm --name tp2-front -d -p 8081:8081 tp2-front
answer: You called at : 2018-11-13 16:55:48.526342 (dynamic)
        On environment : 'dev' (from env variable)
        With path : path_Test   (from URL path)
        With front : 184f92d4447d (from real hostname of front service)
        With back  : 8e9c0fe597b4 (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command: 
command: 


