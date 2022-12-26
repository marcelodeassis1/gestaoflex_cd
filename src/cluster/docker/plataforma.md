## Criar Imagem, Subir para o Docker Hub

**\* criar imagem a partir do dockerfile \*\***
docker build -t gestaoflex/gateway:2.3.3 .

**\* subir imagem para o hub do docker \*\***
docker push gestaoflex/gateway:2.3.3

**_ deletar imagem local da base _**
docker rmi <codigo da imagem>

**_subir o container com a imagem _**

## PostgreSQL 11.11

docker run --rm --name postgresql --network pfm-net -e POSTGRES_PASSWORD=123456 -d -p 5433:5432 -v //e/docker/volumes/postgresql-11.11:/var/lib/postgresql/data postgres:11.11

rgba(144,147,153,0.3)
