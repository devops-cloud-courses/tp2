# Answers

Nom: Asmar	
Prénom: Estelle
NB: 6

## 1.3
command: docker build .

## 1.4
answer:L'adresse URL ne répond rien car les ports ne sont pas ouverts.
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer:Mon image ne peut pas être poussée telle qu'elle est car elle nécessite un TAG.
command:
docker tag 1354c1ef075e ab12cd34/repository1:premiertest
docker push ab12cd34/repository1

## 1.7
answer: Il faut ajouter ab12cd34/repository1
command:sudo docker rmi -f $(docker images -q) 
command:docker run -p 8080:8080 -e ENVIRONMENT=dev ab12cd34/repository1:premiertest
command:docker run -p 8080:8080 -e ENVIRONMENT=dev -d ab12cd34/repository1:premiertest

## 1.8
answer: En mode détaché, nous pouvons vérifier que le container démarre bien lorsqu'on le relance une fois que nous ayons quitté le terminal.
command: docker ps
command: sudo docker rename stoic_sinoussi dockername
	 docker restart dockername

## 1.9
answer: L'OS utilisé dans le container est Debian GNU/Linux 9

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
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d tp2front

http://0.0.0.0:8081/estelle
"With path : estelle   (from URL path)"

## 2.1
command: docker-compose run -p 8080:8080 -e ENVIRONMENT=dev service-back

## 2.6
command: 
command: 


