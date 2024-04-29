###NodePort###
NodePort: Este tipo de Service expõe o Service em um número de porta fixo em cada nó (node) do cluster. Ele também cria um ClusterIP que encaminha para este NodePort.

kubectl apply -f nodeport/deployment.yaml

kubectl get svc

kubectl run prompt --rm -it --image=ubuntu -- /bin/bash

docker container ls

docker container inspect c426a95f22bb

kubectl get nodes -o wide

192.168.49.2

http://192.168.49.2:31956/

curl http://192.168.49.2:31956/
