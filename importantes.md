###Comando Importantes###
Listar todos os pods no namespace atual:
kubectl get pods

Listar todos os serviços no namespace atual:
kubectl get services

Listar todos os deployments no namespace atual:
kubectl get deployments

Listar todos os nós (nodes) no cluster:
kubectl get nodes

Listar todos os namespaces no cluster:
kubectl get namespaces

Listar todos os persistent volumes no cluster:
kubectl get pv

Listar todos os persistent volume claims no namespace atual:
kubectl get pvc

Listar todos os ingress no namespace atual:
kubectl get ingress

Listar todos os configmaps no namespace atual:
kubectl get configmaps

Listar todos os secrets no namespace atual:
kubectl get secrets

Esses são apenas alguns exemplos. Você pode adicionar opções adicionais aos comandos kubectl get para filtrar os resultados ou obter informações mais detalhadas. Por exemplo, você pode adicionar -o wide para obter informações adicionais sobre os recursos.

kubectl get deployments -o yam

kubectl get deploy


##############################

Descrever um pod específico:
kubectl describe pod <nome-do-pod>

Descrever um serviço específico:
kubectl describe service <nome-do-serviço>

Descrever um deployment específico:
kubectl describe deployment <nome-do-deployment>

Descrever um nó específico (node):
kubectl describe node <nome-do-nó>

Descrever um namespace específico:
kubectl describe namespace <nome-do-namespace>

Descrever um persistent volume específico:
kubectl describe pv <nome-do-pv>

Descrever um persistent volume claim específico:
kubectl describe pvc <nome-do-pvc>

Descrever um ingress específico:
kubectl describe ingress <nome-do-ingress>

Descrever um configmap específico:
kubectl describe configmap <nome-do-configmap>

Descrever um secret específico:
kubectl describe secret <nome-do-secret>

kubectl describe deploy

#########################################################

Encaminhar uma porta de um pod para a máquina local:
kubectl port-forward <nome-do-pod> <porta-remota>:<porta-local>

Encaminhar várias portas de um pod para a máquina local:
kubectl port-forward <nome-do-pod> <porta-remota1>:<porta-local1> <porta-remota2>:<porta-local2> ...

Encaminhar uma porta aleatória de um pod para a máquina local:
kubectl port-forward <nome-do-pod> <porta-local>

Encaminhar uma porta de um serviço para a máquina local:
kubectl port-forward service/<nome-do-serviço> <porta-remota>:<porta-local>

Encaminhar uma porta de um deployment para a máquina local:
kubectl port-forward deployment/<nome-do-deployment> <porta-remota>:<porta-local>

Encaminhar uma porta de um replicaset para a máquina local:
kubectl port-forward replicaset/<nome-do-replicaset> <porta-remota>:<porta-local>

#########################################################
Recuperar os logs de um pod específico:
kubectl logs <nome-do-pod>

Recuperar os logs de um contêiner específico em um pod com múltiplos contêineres:
kubectl logs <nome-do-pod> -c <nome-do-contêiner>

Recuperar os logs de um pod específico no namespace especificado:
kubectl logs <nome-do-pod> -n <nome-do-namespace>

Recuperar logs de um pod específico e seguir novos logs (modo de acompanhamento):
kubectl logs -f <nome-do-pod>

Recuperar logs de um pod específico em um contêiner específico e seguir novos logs (modo de acompanhamento):
kubectl logs -f <nome-do-pod> -c <nome-do-contêiner>

Recuperar logs anteriores a um período específico de um pod (usando timestamp):
kubectl logs <nome-do-pod> --since-time=<timestamp>

Recuperar logs anteriores a um período específico de um pod (usando um período de tempo relativo):
kubectl logs <nome-do-pod> --since=<duração>

Recuperar logs de um pod específico e exibir logs anteriores ao início do contêiner:
kubectl logs <nome-do-pod> --previous

Recuperar logs de um pod que falhou (apenas logs anteriores ao término do contêiner):
kubectl logs <nome-do-pod> --previous -c <nome-do-contêiner>i

##########################################################
Executar um comando em um contêiner específico dentro de um pod:
kubectl exec <nome-do-pod> -- <comando>
Exemplo:
kubectl exec meu-pod -- ls /app

Executar um comando em um contêiner específico dentro de um pod em um namespace específico:
kubectl exec -n <nome-do-namespace> <nome-do-pod> -- <comando>
Exemplo:
kubectl exec -n minha-empresa meu-pod -- cat /etc/config/config.yaml

Executar um comando em um contêiner específico dentro de um pod interativo (modo interativo):
kubectl exec -it <nome-do-pod> -- <comando>
Exemplo:
kubectl exec -it meu-pod -- bash

Executar um comando em um contêiner específico dentro de um pod em um caminho de diretório específico:
kubectl exec <nome-do-pod> -- <caminho-do-comando>
Exemplo:
kubectl exec meu-pod -- /usr/bin/myscript.sh

Executar um comando em um contêiner específico dentro de um pod em um shell interativo (modo interativo):
kubectl exec -it <nome-do-pod> -- <shell>
Exemplo:
kubectl exec -it meu-pod -- sh

Executar um comando em um contêiner específico dentro de um pod como um usuário diferente (usuário root, por exemplo):
kubectl exec -u <usuário> <nome-do-pod> -- <comando>
Exemplo:
kubectl exec -u root meu-pod -- apt-get update

############################################################################
Criar um deployment a partir de uma imagem Docker:
kubectl run <nome-do-deployment> --image=<imagem-docker>
Exemplo:
kubectl run nginx-deployment --image=nginx

Criar um deployment com um número específico de réplicas:
kubectl run <nome-do-deployment> --image=<imagem-docker> --replicas=<número-de-réplicas>
Exemplo:
kubectl run nginx-deployment --image=nginx --replicas=3

Criar um deployment com etiquetas específicas:
kubectl run <nome-do-deployment> --image=<imagem-docker> --labels=<chave>=<valor>
Exemplo:
kubectl run nginx-deployment --image=nginx --labels=app=nginx

Criar um deployment com comandos ou argumentos específicos:
kubectl run <nome-do-deployment> --image=<imagem-docker> -- <comando> <argumentos>
Exemplo:
kubectl run nginx-deployment --image=nginx -- nginx -g 'daemon off;'

#################################################################################

Excluir um pod específico:
kubectl delete pod <nome-do-pod>

Excluir todos os pods de um determinado label:
kubectl delete pod -l <chave>=<valor>

Excluir um deployment específico:
kubectl delete deployment <nome-do-deployment>

Excluir um serviço específico:
kubectl delete service <nome-do-serviço>

Excluir todos os serviços de um determinado label:
kubectl delete service -l <chave>=<valor>

Excluir um ingress específico:
kubectl delete ingress <nome-do-ingress>

Excluir um configmap específico:
kubectl delete configmap <nome-do-configmap>

Excluir um secret específico:
kubectl delete secret <nome-do-secret>

Excluir todos os recursos de um determinado tipo:
kubectl delete <tipo-de-recurso> --all

Excluir todos os recursos em um namespace específico:
kubectl delete --all -n <nome-do-namespace>

Excluir um nó específico do cluster:
kubectl delete node <nome-do-nó>

Excluir um namespace específico e todos os seus recursos:
kubectl delete namespace <nome-do-namespace>
