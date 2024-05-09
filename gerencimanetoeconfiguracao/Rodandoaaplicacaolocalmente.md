/home/marcelotse/tse/kubernetes2.0/app-variaveis-ambiente/src

Exemplos apenas para rotar localmente

npm install (para baixar a dependencias)

node server.js

abrir  o browser para verficar http://localhost:3000/

ou tambem para nao deixar no .env adicionar nas variaveis de ambiente S.O utilizando o export

no linux digitar env para ver

export APP_NAME="Aplicação Tse" 
export APP_NAME==1.1
export APP_NAME=jmarcelotse 

node server.js

### No Kubernetes ###
kubeclt apply -f ./gerencimanetoeconfiguracao/K8S/deployment.yaml 

kubectl get pods

kubectl get services

http://192.168.49.2:30284/

kubectl apply -f ./gerencimanetoeconfiguracao/K8S/deployment2.yaml

kubectl get pods

kubectl get services

kubectl get nodes -o wide

http://192.168.49.2:32006/

app-configuracao-744b767cb4-mkqq7

env


Da forma acima ainda nao 'e uma boa pratica.

### ConfigMap ###

kubectl get configmaps

## Por Referencia ##
kubectl apply -f ./gerencimanetoeconfiguracao/K8S/ConfigMap/deployment.yaml -f ./gerencimanetoeconfiguracao/K8S/ConfigMap/configmap.yaml

kubectl get configmaps

ubectl describe configmaps app-config

kubectl get nodes -o wide

kubectl get all

http://192.168.49.2:31525/

## Por valor ##

