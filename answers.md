# Answers

Nom: Pasternak
Prénom: Claire
NB: 3

## 1.3
command: 
docker build -t tp2 .

## 1.4
answer: car les ports sont fermés
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -it --rm --name tp2back --env ENVIRONMENT=dev -p 8080:8080 tp2

## 1.6
answer: L'image ne peut pas être poussée car en faisant "docker push clairepas/tp2" on ne sait pas ce qu'il doit etre poussé, il faut rajouter un tag sur l'image
command: On trouve l'id de l'image à taguer en faisant : "docker images"
puis :
docker tag 8f2c1374774d clairepas/tp2
docker push clairepas/tp2

## 1.7
answer: Il doit la pull du repository
command: docker rmi -f $(docker images -q)
command: docker run -it --rm --name tp2back --env ENVIRONMENT=dev -p 8080:8080 clairepas/tp2
command: docker run -it --rm --name tp2back --env ENVIRONMENT=dev -p 8080:8080 -d clairepas/tp2

## 1.8
answer: tp2back
command: docker ps
command: docker rename d054d7b56ad8 tp2-back

## 1.9
answer: debian
answer:
cat: /etc/lsb-release: No such file or directory
PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: docker run -it --rm --name tp2-2front -p 8081:8081/tcp -p 8081:8081/udp --env APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 tp2-2

        You called at : 2018-11-13 18:06:39.889527 (dynamic)
        On environment : dev (from env variable)
        With path : tp2   (from URL path)
        With front : c7b31db1e817 (from real hostname of front service)
        With back  : d054d7b56ad8 (from real hostname of back service)

##1.12
command: docker exec -it d054d7b56ad8 cat logs/my-messages.log

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: 

## 2.9
command:


