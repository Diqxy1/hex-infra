# HexCore - INFRA

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

### Ambiente de desenvolvimento

Após clonar o repositório verificar quais containers você deseja subir. Por padrão está habilitado o Mysql e os containers relativos ao Kafka. 
Caso deseja plugar alguma outro container referente a um projeto da HexCore você deve descomentar a linha do serviço e alterar o path 'build:' do mesmo.

Na primeira vez que clonar o  repositório é necessário fazer o build dos containers

    sudo docker-compose build

Após o build você já pode subir os containers

    sudo docker-compose up -d