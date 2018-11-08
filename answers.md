# Answers

Nom: Ly
Prénom: Hervé
NB: 2

## 1.3
command: docker run -it --rm --name my-running-app tp2

## 1.4
answer: la connection au port n'est pas autorisée
command: docker run -it --rm --name my-running-app tp2
docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp my-python-app

## 1.5
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine tp2

## 1.6
answer: le nom de l'image doit correspondre à celui du repository
command: docker login (login dans docker hub)
         docker images (pour trouver l'id de mon image)
         docker tag 7e16e8a015e5 hrvly/tp2 (tag mon appli docker vers son id docker hub)
         docker push hrvly/tp2 (push mon appli vers docker hub)
## 1.7
answer: l'image est introuvable localement, docker va donc le télécharger avant de le lancer
command: sudo docker rmi -f $(docker images -q)
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine hrvly/tp2
command: docker run -it --rm --name my-running-app -p 8080:8080/tcp -p 8080:8080/udp -e ENVIRONMENT=python:3-alpine -d hrvly/tp2

## 1.8
answer: nom de mon container: my-running-app, id: c5948d1876e0
command: docker ps
command: docker rename c5948d1876e0 sens

## 1.9
answer: docker exec -it sens cat /etc/*release
answer: NAME="Alpine Linux"
        ID=alpine
        VERSION_ID=3.8.1
        PRETTY_NAME="Alpine Linux v3.8"
        HOME_URL="http://alpinelinux.org"
        BUG_REPORT_URL="http://bugs.alpinelinux.org"

## 1.11
command: docker run -it --rm --name my-running-app2 -p 8081:8081/tcp -p 8081:8081/udp -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d hrvly/front
answer: You called at : 2018-11-08 13:50:39.092742 (dynamic)
        On environment : python:3-alpine (from env variable)
        With path : bonjour   (from URL path)
        With front : 8b1f466d4822 (from real hostname of front service)
        With back  : a55d101a7459 (from real hostname of back service)
command:

## 2.1
command:

## 2.6
command:
command:
