# Answers

Nom: PIOVESAN
Prénom: Clément
NB: 2

## 1.3
command: docker build -t cpiovesan/tp2 .
         docker run -it --rm --name my-running-app my-python-app

## 1.4
answer: L'addresse ne répond car nous avons pas autorisé la connection au port 8080
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp my-python-app

## 1.5
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine my-python-app

## 1.6
answer: Il faut changer le nom de son appli et le remplacer par le nom de son dépot Docker Hub (cpiovesan/tp2 dans mon cas)
command: docker login (login dans docker hub)
         docker images (pour trouver l'id de mon image)
         docker tag 5868e2a4e118 cpiovesan/tp2 (tag mon appli docker vers son id docker hub)
         docker push cpiovesan/tp2 (push mon appli vers docker hub)

## 1.7
answer:d
command: docker rmi -f XXXXXXX (id de l'image)
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine cpiovesan/tp2
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine -d cpiovesan/tp2

## 1.8
answer:
command: docker ps (nom de mon container: my-running-app, id: 8898504301e4)
command: docker container rename my-running-app tp2container
         docker restart 8898504301e4

## 1.9
answer: docker exec -i -t 8199a0b3a0bf cat /etc/*release
answer: Il montre que nous utilisons l'OS Alpine Linux
answer: NAME="Alpine Linux"
        ID=alpine
        VERSION_ID=3.8.1
        PRETTY_NAME="Alpine Linux v3.8"
        HOME_URL="http://alpinelinux.org"
        BUG_REPORT_URL="http://bugs.alpinelinux.org"


## 1.11
command: docker run -it --rm -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.20.10.3 cpiovesan/tp2front
answer: You called at : 2018-11-08 13:50:20.982599 (dynamic)
        On environment : python:3-alpine (from env variable)
        With path : write   (from URL path)
        With front : 3cc71ce7cc48 (from real hostname of front service)
        With back  : 96c81aa0efee (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command:
command:
