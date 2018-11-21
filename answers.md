# Answers

Nom: Ong
Prénom: Philippe
NB: 6

## 1.3
command: 
docker build -t tp2back .
docker run tp2back

## 1.4
answer: Nous n'avons pas ouvert le port 8080 pour accéder au service.
command: docker run -p 8080:8080 tp2back

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2back

## 1.6
answer: Il est nécessaire d'ajouter un tag à notre image avant de push
command: 
docker tag e58e15377c01 ongphil/tp2back
docker push ongphil/tp2back

## 1.7
answer: L'image n'existe pas localement puisqu'on l'a supprimé. Il faut essayer de récupérer l'image de notre repo en ajoutant notre nom d'utilisateur : ongphil/tp2back
command: docker rmi -f $(docker images -q) 
command: docker run -p 8080:8080 -e ENVIRONMENT=dev ongphil/tp2back
command: docker run -p 8080:8080 -e ENVIRONMENT=dev -d ongphil/tp2back

## 1.8
answer: En lançant en mode détaché, notre back est toujours fonctionnel même si on ferme le terminal.
Le nom du contenur est relaxed_turing
command: docker ps
command: docker rename relaxed_turing detached_tp2back

## 1.9
Pour ouvrir une session interactive et afficher les informations sur l'OS :
docker exec -i detached_tp2back bash
cat /etc/*release
answer: l'OS utilisé est Debian GNU/Linux 9 (stretch).
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
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 ongphil/tp2front
answer:
http://localhost:8081/philippe
You called at : 2018-11-09 13:39:23.380670 (dynamic)
        On environment : dev (from env variable)s
        With path : philippe   (from URL path)
        With front : 4615afcaacdf (from real hostname of front service)
        With back  : abe9cad70252 (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d
command: docker-compose logs

## 2.9
command: docker-compose up -d --scale tp2back=2

