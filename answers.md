# Answers

Nom: Marchand
Prénom: Adrien
NB: 3

## 1.3
command: docker build -t tp2 ./

## 1.4
answer: Elle ne répond rien parce qu'elle n'autorise pas la connexion : les ports sont fermés.
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=python:3-alpine tp2

## 1.6
answer: Parce qu'elle n'a pas le bon nom.
command: docker tag tp2 admar/tp2:0.1 --> docker push admar/tp2:0.1

## 1.7
answer: l'image est introuvable localement, docker va la télécharger avant de la lancer.
command: sudo docker rmi -f $(docker images -q)
command: docker run -p 8080:8080 -e ENVIRONMENT=python:3-alpine tp2
command: docker run -p 8080:8080 -e ENVIRONMENT=python:3-alpine -d tp2

## 1.8
answer: nom de mon containe : tp2, id : b752ca30cdc8
command: docker ps
command: docker rename b752ca30cdc8 contp2

## 1.9
answer:NAME="Alpine Linux"
ID=alpine
VERSION_ID=3.8.1
PRETTY_NAME="Alpine Linux v3.8"
HOME_URL="http://alpinelinux.org"
BUG_REPORT_URL="http://bugs.alpinelinux.org"

## 1.11
command: docker run -p 8080:8080 -e APP_PORT=8080 -e WS_BACK_URL=172.17.0.1 admar/tp2_container:tp2 
answer: You called at : 2018-11-11 22:34:12.552369 (dynamic) On environment : dev (from env variable) With path : test (from URL path) With front : 1a26378314c6 (from real hostname of front service) With back : 018cde996282 (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d command: docker-compose logs

## 2.6
command: docker-compose up --scale back_service=2


