# Answers

Nom: GAIDIER 
Prénom: Clément
NB: 4

## 1.3
command: docker build -t tp2back ./ 
docker run tp2back  

## 1.4
answer: Les ports TCP ne sont pas ouverts 
command: docker run -p 8080:8080 tp2back

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2back

## 1.6
answer: L'image n'a pas de tag donc il faut associer un tag à l'image
command: docker tag tp2back clementgaidier/tp2back 
docker push clementgaidier/tp2back

## 1.7
answer: 
command: docker rmi -f $(docker images -a -q) 
command: docker run -p 8080:8080 -e ENVIRONMENT=dev clementgaidier/tp2back
command: docker run -d -p 8080:8080 -e ENVIRONMENT=dev clementgaidier/tp2back

## 1.8
answer: nom de mon container est mystifying_cohen
command: docker ps  
command: docker rename 26f620eee85b tp2back

## 1.9
answer: Debian 9 (stretch)
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"


## 1.11
command: docker run -d -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 clementgaidier/tp2front
answer: You called at : 2018-11-13 14:32:08.315980 (dynamic)
        On environment : dev (from env variable)
        With path : write   (from URL path)
        With front : 8f0ff760d00d (from real hostname of front service)
        With back  : 59e6de57fb02 (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: docker-compose logs

## 2.9
command: 


