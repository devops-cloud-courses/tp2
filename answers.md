# Answers

Nom: Bouhi
Prénom: Jeremy
NB: 5

## 1.3
command: docker build -t tp2 back
docker run tp2

## 1.4
answer: Cette adresse ne répond pas parce qu'on a ouvert aucun port pour accéder à l'image
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer: Le nom du tag doit être le même que celui renseigné lors du 'docker build'
command: docker login
docker tag tp2 $DOCKER_ID_USER/tp2
docker push $DOCKER_ID_USER/tp2

## 1.7
answer: Si on relance exactement la même qu'aupravant on : "Unable to find image 'tp2:latest' locally". Pour lancer le run il faut ajouter le $DOCKER_ID_USER devant /tp2
command: docker rmi 209124f8a55c --force
command: docker run -p 8080:8080 -e ENVIRONMENT=dev $DOCKER_ID_USER/tp2
command: docker run -d -p 8080:8080 -e ENVIRONMENT=dev $DOCKER_ID_USER/tp2

## 1.8
answer: En utilisant la commande 'docker ps', on peut facilement voir si le container est up
Nom du container : inspiring_hawking
command: docker ps
command: docker rename inspiring_hawking tp2_container

## 1.9
answer: Debian Linux
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
command: docker run -d -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 $DOCKER_ID_USER/tp2front

You called at : 2018-11-08 17:24:15.279235 (dynamic)
        On environment : dev (from env variable)
        With path : yo   (from URL path)
        With front : 603ee33edf1d (from real hostname of front service)
        With back  : 77873d4c3fb1 (from real hostname of back service)

## 2.1
command: docker-compose run mon-super-service-back

## 2.6
command: 
command: 


