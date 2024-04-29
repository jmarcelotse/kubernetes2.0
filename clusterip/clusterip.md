###ClusterIP###
ClusterIP: Este é o tipo padrão de Service. Ele atribui um IP interno estático ao Service, que é acessível apenas dentro do cluster

kubectl apply -f clusterip/deployment.yaml

kubectl get pods

kubectl get services

kubectl get svc

kubectl run prompt -it --image=ubuntu -- /bin/bash

kubectl get pods -o wide

curl http://10.244.1.1 #diretamente pelo IP

curl http://webcolor #pelo nome do service

 
