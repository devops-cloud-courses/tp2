# Answers

Nom: Valais
Prénom: Alexia
NB: 1

## 1.3
command: docker run python_image

## 1.4
answer: On ne peut pas accéder à l'URL car le port 8080 est fermé. On doit préciser sur quel port on veut écouter.
command: docker run -p 8080:8080 python_image

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=back python_image

## 1.6
answer: L'image ne peut pas être envoyée telle qu'elle est car elle n'est pas trouvée localement. Il faut que son tag corresponde au nom du repo docker hub.
command: docker login
         docker tag python_image avalais/tp2
         docker push avalais/tp2

## 1.7
answer: Lorsque l'on run l'image, elle est d'abord cherchée localement. Comme elle n'est pas trouvée, on la télécharge à partir du repo docker.
command: docker rmi $(docker images -a -q) => on récupère les ids de toutes les images
command: docker run -p 8080:8080 -e ENVIRONMENT=back avalais/tp2
command: docker run -d -p 8080:8080 -e ENVIRONMENT=back avalais/tp2

## 1.8
answer: On peut voir si le container est bien lancé et ses détails en faisant la commande docker ps. Le nom de mon container est vigilant_lalande.
command: docker ps
command: docker rename vigilant_lalande tp2_container

## 1.9
answer: L'OS utilisée par le container est Debian comme on peut le voir dans les caractéristiques.
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"


## 1.11
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d  avalais/tp2_front
answer: With path : alexia   (from URL path)

## 2.1
command: docker-compose up

## 2.6
command: 
command: 


