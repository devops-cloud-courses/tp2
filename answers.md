# Answers

Nom: akherraz 
Prénom: Brahim
NB: 4

## 1.3
command: docker build -t tp2 ./
docker run tp2 

## 1.4
answer: Parce que les ports TCP 8080 est fermé 
command:docker run -p 8080:8080 tp2  

## 1.5
command:docker run -p 8080:8080 -e ENVIRONMENT=dev tp2 

## 1.6
answer:on doit utiliser des tag
command: docker tag tp2 $DOCKER_ID_USER/tp2
docker push brahimakh/tp2

## 1.8
answer: 
command: docker run -p 8080:8080 -e ENVIRONMENT=dev -d tp2
command: docker ps
command: docker rename ID_d_image nouveau_nom 

## 1.7
answer:
command: docker rmi -f $(docker images -q)
command: docker pull brahimakh/tp2

## 1.9
answer:root@8ac4c7fa6ca9:/app/back# cat /etc/*release
PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

answer:Debian 9 stretch

## 1.11
You called at : 2018-11-09 14:09:26.522452 (dynamic)
        On environment : dev (from env variable)
        With path : brahim   (from URL path)
        With front : 89db88ca94d4 (from real hostname of front service)
        With back  : ccfacc578f6c (from real hostname of back service)
docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 tp2


## 2.1
command: docker-compose up
 

## 2.6
command: docker-compose up -d
command: docker-compose logs

## 2.9
command:docker-compose up -d --scale tp2=2
