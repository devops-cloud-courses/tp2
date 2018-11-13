# Answers

Nom: Vuong
Prénom: Lisa
NB: 3

## 1.3
command: 
docker build -t img .
docker run img

## 1.4
answer: car les ports ne sont pas ouverts
command: docker run -p 8080:8080 img

## 1.5
command: docker run -e ENVIRONMENT=dev -p 8080:8080 img

## 1.6
answer: car le nom de l'image n'est pas bon
command: docker tag img lisav/img:0.1 --> docker push lisav/img:0.1
         
## 1.7
command: sudo docker rmi -f $(docker images -q)
answer: l'image est "pull" du repository docker lisav/img comme il ne le trouve pas localement
command: docker run -e ENVIRONMENT=dev -p 8080:8080 lisav/img
command: docker run -d -e ENVIRONMENT=dev -p 8080:8080 lisav/img

## 1.8
answer: name = ecstatic_mcnulty and container id = d4fb6f40aa9a. 
command: docker ps  OU docker container ls
command: docker rename ecstatic_mcnulty realcontainersname

## 1.9
answer: L'OS utilisé est Debian GNU/Linux 9.
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
command: docker run -p 8081:8081 -e WS_BACK_URL=172.17.0.1 -e APP_PORT=8081 front
answer:pour le back, ce qui change est :   "result": "path_test"
       pour le front, ce qui change est :   With path : path_test   (from URL path)

## 2.1
command: 

## 2.6
command: 
command: 


