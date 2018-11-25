# Answers

Nom: FOLLY	
Prénom: Roch	
NB: 5

## 1.3
command: docker build -t tp2 back
command 2: docker run tp2 back

## 1.4
answer: Nous n'avons ouvert aucun port 8080 pour accéder à l'image Docker.
command: docker run -p 8080:8080 tp2 back

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer: Il faut taguer l'image avant de pouvoir la push 
command: docker tag c4a3d2e51af7 rochfolly/tp2
command : docker push rochfolly/tp2

## 1.7
answer: Après avoir supprimé toutes les images, elles n'existement logiquement plus localement. Lorsqu'on essaye de la lancer à nouveau, l'image est pulled avant de démarrer.
command: docker rmi -f $(docker images -q)
command: docker run -p 8080:8080 -e ENVIRONMENT=dev rochfolly/tp2
command: docker run -p 8080:8080 -e ENVIRONMENT=dev -d rochfolly/tp2

## 1.8
answer: On peut vérifier que le container est bien démarré en regardant si il fonctionne avec le terminal fermé. C'est le cas, et son nom est kind_mclaren.
command: docker ps
command: docker rename kind_mclaren detached_tp2

## 1.9
answer: docker exec -i detached_tp2 cat /etc/*release
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"


## 1.11
command: 

## 2.1
command: 

## 2.6
command: 
command: 


