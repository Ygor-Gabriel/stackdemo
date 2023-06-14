# stackdemo
Iniciando serviço no seu exame:
docker service create --name registry --publish published=5000,target=5000 registry:2

Verificando  status:
docker service ls

Verifica se ta funcionando:
curl http://localhost:5000/v2/

Após criar os arquivos segundo o: https://docs.docker.com/engine/swarm/stack-deploy/

Teste o aplicativo com:
docker compose up -d (para testar em background)
docker compose up

Verifique se o aplicativo está funcionando:
docker compose ps

Teste a porta escolhida para saber se está aparecendo o "Hello wold" com:
curl http://localhost:8000

Desligue o aplicativo com:
 docker-compose down --volumes
 
