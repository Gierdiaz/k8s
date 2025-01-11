kind create cluster
kind create cluster --name meu-cluster
kind delete cluster --name nome-do-cluster
kind get clusters
kubectl config use-context kind-nome-do-novo-cluster -> caso eu tenha mais de um cluster e queira mudar o contexto
kubectl config use-context kind-fullcycle que é o nome do meu cluster

docker ps
kubectl get nodes

kind create cluster --config=k8s/kind.yaml --name=fullcycle


kubectl config get-clusters

# Docker
docker build -t Schzimmyd/hello-go .
docker run --rm -p 80:80 Schzimmyd/hello-go
docker push schzimmyd/hello-go

nosso container roda dentro de um pod

# para visualizar erros
kubectl describe pod goserver
kubectl logs goserver

# excluir o pod
kubectl delete pod goserver

# verificando se está funcionando
kubectl port-forward pod/goserver 8080:8080 => curl http://localhost:8080


kubectl get pods
kubectl get replicasets
