# Answers

Nom: TABEL
Prénom: Eugénie
NB: 6

## 1.3
command: docker build .

## 1.4
answer: L'adresse URL ne répond rien car les ports ne sont pas ouverts. 
command: docker run -p 8080:8080 tp2

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2

## 1.6
answer: L'image ne peut pas être poussée car elle a besoin d'un tag. 
command: 
docker tag c095ac280f56 eugetbl/tp2:premiertest
docker push eugetbl/tp2

## 1.7
answer: il faut ajouter eugetbl/repository1
command: sudo docker rmi -f $(docker images -q ) //Pour supprimery
command: docker run -p 8080:8080 -e ENVIRONMENT=dev eugetbl/tp2:premiertest
command: docker run -p 8080:8080 -e ENVIRONMENT=dev -d eugetbl/tp2:premiertest


## 1.8
answer: En mode détaché, nous pouvons vérifier que le container démarre bien lorsque l'on  relance après avoir fermé le terminal.
command: docker ps
command: 
sudo docker rename  dreamy_shockley containertp2
docker restart containertp2

## 1.9
answer:Debian GNU/Linux 9 (stretch)
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
NAME="Debian GNU/Linux"
VERSION_ID="9"
VERSION="9 (stretch)"
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d imagefront

http://0.0.0.0:8081/eugetbl

Y  ou called at : 2018-11-21 15:20:01.116559 (dynamic)
        On environment : dev (from env variable)
        With path : eugetbl   (from URL path)
        With front : 6c35e3886fcc (from real hostname of front service)
        With back  : 05e02fec5f6f (from real hostname of back service)

## 2.1
command: docker-compose up

## 2.6
command: docker-compose up -d 
command: docker-compose logs


