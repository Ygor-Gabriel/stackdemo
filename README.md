# stackdemo
Iniciando serviço no seu exame:
docker service create --name registry --publish published=5000,target=5000 registry:2
Iniciando serviço no seu swarm: docker service create --name registry --publish published=5000,target=5000 registry:2

Verificando status: docker service ls

Verifica se ta funcionando: curl http://localhost:5000/v2/

Após criar os arquivos segundo o: https://docs.docker.com/engine/swarm/stack-deploy/

Teste o aplicativo com: docker compose up -d (para testar em background) docker compose up

Verifique se o aplicativo está funcionando: docker compose ps

Teste a porta escolhida para saber se está aparecendo o "Hello wold" com: curl http://localhost:8000

Desligue o aplicativo com: docker-compose down --volumes

Enviar a imagem para o serviço: docker-compose push

Deploy dos arquivos para os integrantes do swarm: docker stack deploy --compose-file docker-compose.yml stackdemo

Verificar se os serviços estão corretos: docker stack services stackdemo

Teste na máquina leader: curl http://localhost:8000

Teste nas máquinas workers: curl http://address-of-other-node:8000
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
 
