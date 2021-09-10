# 001 Fintech - INFRA

## Repositórios responsável por manter as configurações de infra:

Este projato fica responsável por instalar o KAFKA e o MYSQL e tambem estender os projetos que  dependam destas ferramentas.

### Pré-requisitos:

Para trabalhar nesse projeto você ira precisar instalar:

*[ Docker ](https://www.docker.com/get-started)		
*[ Docker Compose ](https://docs.docker.com/compose/install/)

### Criando rede Docker 'Core':

Verique se rede 'core' existe no docker
    docker network ls

Se a rede 'core' ainda não existir crie-a com o seguinte comando
    docker network create core -d bridge

### Repositórios relacionados 

*[ Label - API ](https://bitbucket.org/okpago/001-whitelabel-api)
*[ Core Admin - API ](https://bitbucket.org/okpago/001-coreadmin-api)
*[ Sauron - API ](https://bitbucket.org/okpago/001-sauron-api)
*[ ID Provider - API ](https://bitbucket.org/okpago/001-id-provider-api)
*[ Zilean - API ](https://bitbucket.org/okpago/001-ziliean-api)
*[ Services Catalog - API ](https://bitbucket.org/okpago/001-service-catalog)
*[ Core MongoDB ](https://bitbucket.org/okpago/001-mongodb)

### Ambiente de desenvolvimento

Após clonar o repositório verificar quais containers você deseja subir. Por padrão está habilitado o Mysql e os containers relativos ao Kafka. 
Caso deseja plugar alguma outro container referente a um projeto da 001Fintech você deve descomentar  a linha do serviço e alterar o path 'build:' do mesmo.

Na primeira vez que clonar o  repositório é necessário fazer o build dos containers

    sudo docker-compose build

Após o build você já pode subir os containers

    sudo docker-compose up -d