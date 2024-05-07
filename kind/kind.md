###Kind###
kind create cluster: Cria um novo cluster Kubernetes usando o Kind.
kind delete cluster: Exclui um cluster Kubernetes criado com o Kind.
kind get clusters: Lista os clusters Kubernetes criados com o Kind.
kind load docker-image: Carrega uma imagem Docker em um nó do cluster Kind.
kind export kubeconfig: Exporta o kubeconfig do cluster Kind para que você possa usá-lo com o kubectl.
kind version: Mostra a versão do Kind instalada

O comando kind create cluster é utilizado para criar um novo cluster Kubernetes usando o Kind. Aqui estão alguns dos principais argumentos que podem ser passados para este comando, permitindo a configuração personalizada do cluster:

--name: Define um nome para o cluster.
--config: Especifica um arquivo de configuração YAML para configurar o cluster.
--image: Define a imagem do nó do cluster a ser usada.
--kubeconfig: Especifica o caminho para o arquivo kubeconfig a ser usado.
--wait: Aguarda até que o cluster esteja pronto antes de retornar.
--retain: Mantém os nós do cluster após sua conclusão.
Aqui está um exemplo simples de como usar o comando kind create cluster:
kind create cluster --name meu-cluster
Isso criará um novo cluster Kubernetes chamado "meu-cluster" usando as configurações padrão do Kind.

Claro, aqui estão alguns exemplos de como usar o comando kind create cluster com diferentes opções:

Criar um cluster sem especificar um nome:
kind create cluster
Isso criará um novo cluster Kubernetes usando as configurações padrão do Kind e um nome gerado automaticamente.

Criar um cluster e especificar um nome:
kind create cluster --name meu-cluster
Isso criará um novo cluster Kubernetes chamado "meu-cluster".

Criar um cluster e especificar um arquivo de configuração YAML:
kind create cluster --config config.yaml
Isso criará um novo cluster Kubernetes usando as configurações definidas no arquivo config.yaml.

Criar um cluster e definir uma imagem específica para os nós do cluster:
kind create cluster --image kindest/node:v1.22.2
Isso criará um novo cluster Kubernetes usando a imagem kindest/node:v1.22.2 para os nós do cluster.

Criar um cluster e especificar o caminho para o arquivo kubeconfig:
kind create cluster --kubeconfig ~/mykubeconfig
Isso criará um novo cluster Kubernetes e salvará o arquivo kubeconfig em ~/mykubeconfig.

Criar um cluster e aguardar até que o cluster esteja pronto:
kind create cluster --wait 5m
Isso criará um novo cluster Kubernetes e aguardará até que esteja pronto ou até que o tempo limite de 5 minutos seja atingido.

Esses são apenas alguns exemplos de como você pode usar o comando kind create cluster para criar clusters Kubernetes com o Kind. Você pode combinar essas opções conforme necessário para atender aos requisitos do seu ambiente de desenvolvimento ou teste.

kind get clusters

kind delete cluster

kind delete cluster --name kind-multinodes

###Criando um cluster com arquivo de manifesto###
kind create cluster --name tse --config ./kind/tse-config.yaml

kind get clusters 

kubectl get nodes

docker container ls 

kubectl apply -f /home/marcelotse/tse/kubernetes2.0/kind/deployment.yaml

kubectl get pods

kubectl get services

kubectl port-forward services/conversaotemperatura 8080:80

kind create cluster --name tse --config /home/marcelotse/tse/kubernetes2.0/kind/tse-config1.yaml

kubectl get nodes

kubectl cluster-info --context kind-tse

docker container ls

kubectl apply -f /home/marcelotse/tse/kubernetes2.0/kind/deployment.yaml

watch 'kubectl get pods

https://github.com/kubernetes-sigs/kind/releases

kind create cluster --name tse --config /home/marcelotse/tse/kubernetes2.0/kind/tse-config2.yaml

kind create cluster --name tse --config /home/marcelotse/tse/kubernetes2.0/kind/tse-config2.yaml

kind create cluster --name tse --config /home/marcelotse/tse/kubernetes2.0/kind/tse-config3.yaml

kubectl apply -f https://raw.githubusercontent.com/projectcalico/calico/v3.26.4/manifests/calico.yaml 

kubectl get pods -A 

kubectl get nodes -o wide

docker build -t jmarcelotse/conversao-temperatura-kind:v1 --push .

docker image ls

kubectl apply -f /home/marcelotse/tse/kubernetes2.0/aplicacao1/deployment.yaml

 kubectl get pods

kubectl delete -f /home/marcelotse/tse/kubernetes2.0/aplicacao1/deployment.yaml

kind load --name tse docker-image jmarcelotse/conversao-temperatura-kind:v1

kubectl apply  -f /home/marcelotse/tse/kubernetes2.0/aplicacao1/deployment.yaml
