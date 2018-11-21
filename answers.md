# Answers

Nom: TRBOVIC
Prénom: Alexandre
NB: 7

## 1.3
command: docker run 092db6b799e9
(docker build .  
avec un cd tp2/app/back)

## 1.4
answer: Probleme de variable d'environnement 
command: docker run -it --rm --name my-running-app -p 8080:8080 my-python-app

## 1.5
command: docker run -it -e ENVIRONMENT='dev' --rm --name my-running-app -p 8080:8080 my-python-app

## 1.6
answer: il fallait rajouter le tag
command: docker push alexandretrb/my-python-app

## 1.7
answer: docker rmi -f 48c172c969dc
command: docker run -p 8080:8080 -e ENVIRONMENT=dev alexandretrb/back
command: docker run -p 8080:8080 -e ENVIRONMENT=dev -d alexandretrb/back (pour lancer en mode détaché le container)

## 1.8
answer: docker ps   
command: nom du container : adoring_bartik
command: docker rename adoring_bartik nomquiadusens

## 1.9
answer: docker exec -it 9e9263e66d0e bash
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
command: docker run -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -p 8081:8081 alexandretrb/front
answer:  http://0.0.0.0:8081/aaa  ==>>  With path : aaa   (from URL path)
		 http://0.0.0.0:8081/write/testwritelog

## 2.1
command: 

## 2.6
command: 
command: 


