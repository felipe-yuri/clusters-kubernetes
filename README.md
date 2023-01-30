# Clusters com Kubernetes
Criando cluster com kubernetes (kubectl e minikube)

- O kubernetes é um gerenciador de pods e cada pod gerencia um ou mais containers. 
- Se houver alguma falha com todos os containers do pod, o kubernetes se encarrega de recriar aquele pod defeituoso de forma automática.
- Cada pod possui um ip e cada container dentro dele possui uma porta. Os pods se comunicam através do SVC. 
- O SVC ou services, servem para gerenciar a comunicação entre pods através de ips fixos, DNS e balanceamento de cargas. Esses serviços são: a) ClusterIP; b)NodePort; e, c)LoadBalancer.git config --global core.
  - ClusterIP -> Tem a função de comunicar vários pods dentro do mesmo cluster.
  - NodePort -> Abre comunicação com o mundo externo (fora do cluster).

## Comandos

1. Instalar cluster local com minikube
```bash
minikube start --driver=virtualbox
```
2. Ver nós
```bash
kubectl get nodes
```
3. Ver pods
```bash
kubectl get pods
```
4. Criar pod forma interativa
```bash
kubectl run nome_do_pod --image=nome_imagem_do_dockerhub
```
5. Criar pod forma declarativa
```bash
kubectl apply -f ./nome_arq.yml
```
6. Deletar um pod
```bash
kubectl delete pod nome_do_pod
```
7. Deletar um pod
```bash
kubectl delete pod nome_do_pod
ou
kubectl delete --all pods
```
8. Deletar todos os pods
```bash
kubectl delete --all pods
```
9. Deletar um pod de forma declarativa
```bash
kubectl apply -f./nome_do_arq.yml
```
10. Entrar dentro do container
```bash
kubectl exec -it nome_pod -- bash
```
11. Ver regras firewall do cluster dentro do gcloud
```bash
gcloud compute firewall-rules list --format=json
```
https://cloud.google.com/service-mesh/v1.9/docs/private-cluster-open-port?hl=pt-br


