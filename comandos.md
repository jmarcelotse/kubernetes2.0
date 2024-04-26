https://kubernetes.io/docs/tasks/tools/

###k3d

k3d cluster create

kubectl cluster-info                                                                                                             
Kubernetes control plane is running at https://192.168.49.2:8443
CoreDNS is running at https://192.168.49.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

kubectl cluster-info dump

k3d cluster list 

k3d cluster create meucluster

k3d cluster delete

k3d cluster create k3d-tse --servers 3 --agents 3

k3d cluster create k3d-tse --servers 1 --agents 3 -p "8080:30000@loadbalancer"


