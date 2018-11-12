# Answers

Nom: GAIDIER 
Prénom: Clément
NB: 4

## 1.3
command: docker build -t tp2back ./ 
docker run tp2back  

## 1.4
answer: Les ports TCP ne sont pas ouverts 
command: docker run -p 8080:8080 tp2back

## 1.5
command: docker run -p 8080:8080 -e ENVIRONMENT=dev tp2back

## 1.6
answer: L'image n'a pas de tag donc il faut associer un tag à l'image
command: docker tag tp2front clementgaidier/tp2back 
docker push clementgaidier/tp2back

## 1.7
answer: 
command: docker rmi -f $(docker images -a -q) 
command: docker run -p 8080:8080 -e ENVIRONMENT=dev clementgaidier/tp2back
command: docker run -d -p 8080:8080 -e ENVIRONMENT=dev clementgaidier/tp2back

## 1.8
answer: nom de mon container est elastic_golick
command: docker ps  
command: docker rename 557aa82f50ff tp2back

## 1.9
answer:
answer:

## 1.11
command: 
answer:

## 2.1
command: 

## 2.6
command: 
command: 


