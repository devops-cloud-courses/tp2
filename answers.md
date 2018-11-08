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
answer: L'image ne peut pas être envoyée telle qu'elle est car elle n'est pas trouvée localement. Il faut que son nom corresponde au nom du repo docker hub.
command: docker login
         docker tag python_image avalais/tp2
         docker push avalais/tp2

## 1.7
answer:
command: 
command: 
command: 

## 1.8
answer:
command: 
command: 

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


