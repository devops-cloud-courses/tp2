# Answers

Nom: Auger
Prénom: Simon
NB: Groupe5

## 1.3
command: docker build -t tp2 back
	docker run tp2

## 1.4
answer: Le port n'est pas ouvert. 
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer: pas d'erreur
command: export DOCKER_ID_USER="sauger92"
docker tag tp2 $DOCKER_ID_USER/tp2
docker push $DOCKER_ID_USER/tp2

## 1.7
answer: le tag devient sauger92/tp2 au lieu de tp2
command: docker images -a
docker rmi 3911263c1b97 -f
command: docker pull sauger92/tp2
command: docker run -d -p 8080:8080 -e ENVIRONMENT=dev sauger92/tp2

## 1.8
answer: Avec docker ps on a la lister des container actifs. Son nom est quirky_banach
command: docker ps 
command: docker rename quirky_banach tp2_container

## 1.9
answer: Debian GNU/Linux 9
answer:
PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: 
docker run -d -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 $DOCKER_ID_USER/tp2front

## 2.1
command: 
docker-compose run service-tp2
docker-compose up


## 2.6
command: 
command: 


