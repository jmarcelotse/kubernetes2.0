###ReplicaSet###

kubectl apply -f replicaset/replicaset.yaml 

kubectl get pods

kubectl get replicasets

kubectl describe replicasets.apps meureplicaset

kubectl describe pods meureplicaset-zjsp7

kubectl apply -f replicaset/replicaset.yaml && watch 'kubectl get rs,po'

kubectl delete pod/meureplicaset-zjsp7

kubectl get pods -o wide

kubectl apply -f replicaset/replicaset.yaml

kubectl describe replicasets.apps meureplicaset
