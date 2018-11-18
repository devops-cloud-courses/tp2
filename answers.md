# Answers

Nom: de Solms
Prénom: Jean
NB: 1

## 1.3
command: docker run tp2_container

## 1.4
answer: Cette adresse ne répond pas car nous n'avons pas exposé le port 8080 et ne pouvons donc pas accéder à l'adresse via ce port.
command: docker run -p 8080:8080  -e ENVIRONMENT=dev tp2_container

## 1.5
command: docker run -p 8080:8080  -e ENVIRONMENT=dev tp2_container

## 1.6
answer: Il faut lier l'image à notre compte pour éviter de potentiels doublons
command: docker tag c47ee72e5257 jeandslms/tp2_container:back_end

## 1.7
answer: L'image n'étant pas présente en local, docker va la récupérer sur docker hub afin de pouvoir runner l'image
command: docker rmi $(docker images -a -q)
command: docker run -p 8080:8080  -e ENVIRONMENT=dev jeandslms/tp2_container:back_end
command: docker run -d -p 8080:8080  -e ENVIRONMENT=dev jeandslms/tp2_container:back_end

## 1.8
answer: En faisant "docker ps" nous pouvons observer que le container est bien démarré. Le nom de mon container est "infallible_panini" ceci n'est pas très explicite...
command: docker ps
command: docker rename infallible_panini back_end

## 1.9
answer:L'os utilisé est un linux debian
answer:
```
root@a532421514a6:/app/back# cat /etc/*release
PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"
```

## 1.11
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 jeandslms/front_container:front
answer: Pour trouver l'adresse de WS_BACK_URL il faut faire un ifconfig, on trouve alors l'adresse ip du container.
Contenu :
"
You called at : 2018-11-08 21:24:14.369606 (dynamic)
On environment : dev (from env variable)
With path : coucou   (from URL path)
With front : 330e3fde2377 (from real hostname of front service)
With back  : d6abf7effd9b (from real hostname of back service)
"

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: docker-compose logs (-f for follow)

##2.9
command: docker-compose up --scale back_service=2 
