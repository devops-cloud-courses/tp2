# Answers

Nom: JACQUIN
Prénom: Théo
NB: 1

## 1.3
command: docker build -t tp2 ./

## 1.4
answer: Elle ne répond pas car les ports sont fermés. Il faut run pour ouvrir les ports et pour qu'elle autorise la connexion.
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080  -e ENVIRONMENT=dev my-python-app

## 1.6
answer: parce qu'il faut tagger l'image
command: docker tag my-python-app tolsk/micro-services-classes
         (docker login)
         docker push tolsk/micro-services-classes

## 1.7
answer: l'image se télécharge avant de démarrer
command: docker rmi $(docker images -a -q)
command: docker run -p 8080:8080 -e ENVIRONMENT=3-alpine tolsk/micro-services-classes
command: 

## 1.8
answer: en mode détacher on peut savoir si le container est bien démarré en rafraichissant la page ou en utilisant la commande docker ps
command: docker rename nom_du_container nouveau_nom
command: docker restart nouveau_nom

## 1.9
answer: Debian GNU/Linux
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: docker run -p 8081:8081  -e APP_PORT=8081 -e WS_BACK_URL=10.9.177.183 tp2_front
0.0.0.0:8081/patheo

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: docker-compose logs


