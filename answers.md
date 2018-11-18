# Answers

Nom: Benguigui
Prénom: Thomas
NB: Groupe 3

## 1.3
command: docker run tp2
On a créé l'image docker avec  "docker build -t tp2 ./"

## 1.4
answer: La machine n'autorise pas la connexion car les ports sont fermés.
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer: L'image n'a pas un nom qui correspond à celui du repo docker.
command: docker tag tp2 tombenpotter/microservices-tp2:0.1
docker push tombenpotter/microservices-tp2:0.1

## 1.7
answer: L'image n'est pas trouvée localement, donc docker va la télécharger sur le hub avant de la lancer.
command: docker rmi $(docker images -q)
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tombenpotter/tp2:0.1
command: docker run -d -p 8080:8080 -e ENVIRONMENT=dev tombenpotter/tp2:0.1

## 1.8
answer: Il faut utiliser la commande ci-dessous, car le container est en mode détaché. Le nom du container est : 2049f02f297b
command: docker ps -a
command: docker rename [id] back

## 1.9
answer: docker exec -it back bash
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: docker run -d -p 1010:1010 -e APP_PORT=1010 -e WS_BACK_URL=172.17.0.1 tombenpotter/microservices-tp2-front
answer: You called at : 2018-11-11 22:03:42.533379 (dynamic)
        On environment : dev (from env variable)
        With path : test   (from URL path)
        With front : 1a27478114c6 (from real hostname of front service)
        With back  : 018cde991272 (from real hostname of back service)

## 1.11 bis
command: docker exec -it [back_container_id] bash

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: docker-compose logs

## 2.9
command:
