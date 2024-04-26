###Deployment###

kubectl apply -f deployment/deployment.yaml

kubectl get all

kubectl get pod

kubectl get deployments

kubectl describe deployments.apps meudeployment

kubectl apply -f deployment/deployment.yaml && watch 'kubectl get po'

kubectl port-forward pod/meudeployment-679878584b-4v9bq 8080:80

###Rollout###
ubectl get replicasets                                        
NAME                       DESIRED   CURRENT   READY   AGE
meudeployment-679878584b   10        10        10      4m11s = green
meudeployment-7dc4495757   0         0         0       8m7s = blue

kubectl describe replicasets.apps meudeployment-7dc4495757

kubectl rollout history deployment meudeployment

kubectl rollout undo deployment meudeployment  && watch 'kubectl get deploy,rs,pod'
