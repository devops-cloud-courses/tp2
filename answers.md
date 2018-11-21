# Answers

Nom: Monomakhoff
Prénom: Victor
NB: 1

## 1.3
command: docker run tp2_back

## 1.4
answer: Le port 8080 est fermé :/
command: docker run -p 8080:8080 -e ENVIRONMENT=back tp2_back

## 1.5
command: ENVIRONMENT=back

## 1.6
answer: An image does not exist locally with the tag: vmonomakhoff/tp2
command: docker images
	 docker tag b84636daa55d vmonomakhoff/tp2

## 1.7
answer: L'image est pull avant que l'image redémarre
command: docker rmi -f $(docker images -q)
command: docker run -p 8080:8080 -e ENVIRONMENT=back vmonomakhoff/tp2
command: docker run -p 8080:8080 -e ENVIRONMENT=back -d vmonomakhoff/tp2

## 1.8
answer: zealous_bhabha
command: docker ps
command: docker rename zealous_bhabha TP2Back
	 docker restart TP2Back

## 1.9
answer: docker exec -it TP2Back cat /etc/*release
answer: docPRETTY_NAME="Debian GNU/Linux 9 (stretch)"
	NAME="Debian GNU/Linux"
	VERSION_ID="9"
	VERSION="9 (stretch)"
	ID=debian
	HOME_URL="https://www.debian.org/"
	SUPPORT_URL="https://www.debian.org/support"
	BUG_REPORT_URL="https://bugs.debian.org/"


## 1.11
command: docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d vmonomakhoff/tp2_f
answer: With path : toto   (from URL path)

## 2.1
command: docker-compose run tp2

## 2.6
command: docker-compose run -d back 
command: docker-compose run -d front


