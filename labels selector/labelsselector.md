###Labels Selector###

kubectl apply -f Labels\ selector/pod.yaml

kubectl get pods

kubectl get pods -l app=web

kubectl get pods -l versao=blue

kubectl get pods -l versao=green

kubectl delete -f labels\ selector/pod.yaml
