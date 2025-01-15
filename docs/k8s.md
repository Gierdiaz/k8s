kind create cluster
kind create cluster --name meu-cluster
kind delete cluster --name nome-do-cluster
kind get clusters
kubectl config use-context kind-nome-do-novo-cluster -> caso eu tenha mais de um cluster e queira mudar o contexto
kubectl config use-context kind-fullcycle que é o nome do meu cluster

docker ps
kubectl get nodes

# Criando um cluster
kind create cluster --config=k8s/kind.yaml --name=fullcycle


kubectl apply -f k8s

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
kubectl port-forward pod/goserver 8080:8080 => curl http://localhost:8080 => chamando de um pod


kubectl get pods
kubectl get replicasets
kubectl delete replicasets goserver



deployment -> replicasets -> pods
kubectl get deployments
kubectl get replicasets


# mudando a versão anterior caso alguma coisa dê errado
kubectl rollout history deployment goserver-deployment
kubectl rollout undo deployment goserver-deployment --to-revision=2 (o número vai depender de qual voce quer entrar)

kubectl get services ou svc 
kubectl port-forward svc/goserver-service 8080:8080 => chamando de um service


api kubernetes:
kubectl --proxy --port=8080