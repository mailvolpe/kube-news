# kube-news

# Tags e Push 
- 1 - Clonar repositório forkeado do github.
- 2 - Criar Dockerfile na pasta /src com setagem básica da imagem. Atenção às boas práticas (Versão da imagem / .dockerignore)
- 3 - Buildar o container 'docker build -t mailvolpe/kube-news:v1 -f Dockerfile .'
- 4 - Fazer o push da v1 para o Docker Hub com 'docker push mailvolpe/kube-news:v1'
- 5 - Fazer a tag da latest e o push para o Docker Hub com 'docker push mailvolpe/kube-news:latest'

# Deployment com Kubernetes
- 6 - Criar o deployent.yaml
- 7 - Definir a aplicação e o serviço para o Postgres
- 8 - Fazer um port binding e testar o postgres com o Dbeaver
- 9 - Definir a aplicação e o serviço para a imagem mailvolpe/kube-news:v1

# Testando e escalando a aplicação
- 10 - Testar a aplicação na porta 30000 que foi definida para o loadbalancer na criação do cluster.
- 11 - Aumentar o número de replicas e rodar um 'apply -f'
- 12 - Modificar uma view, buildar uma v2 e dar push para o Docker Hub
- 13 - Subir a v2 com Deployment (Zero downtime)
- 14 - Testar um rollback com 'kubectl rollout undo deployment kubenews'
