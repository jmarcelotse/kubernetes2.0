###Primeia Aplicacao###
Fazer o deploy simple em um Cluster Kubernetes

Criar o Dockerfile para criar a imagem e subir no dockerkub
##
FROM node:18.16.0
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]
##

docker build -t jmarcelotse/conversao-temperatura:v1 --push .

Criar o deploy dentro do kubernetes
Primeira 'e criar o manifesto 

kubectl apply -f /home/marcelotse/tse/kubernetes2.0/aplicacao/deployment.yaml

kubectl get all

kubectl get replicasets

No mesmo manifesto tambem tem o service

kubectl apply -f /home/marcelotse/tse/kubernetes2.0/aplicacao/deployment.yaml 

kubectl get nodes -o wide

http://192.168.49.2:30407/
