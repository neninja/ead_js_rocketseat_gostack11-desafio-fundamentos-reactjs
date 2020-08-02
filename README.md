# Desafio
## initial setup
```sh
# criação do container
docker run --name gostack_postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres
# caso ele já exista:
# docker start gostack_postgres

# download de dependências js
yarn

# criação de tabelas
yarn typeorm migration:run

# popular o banco
# enviar para localhost:3333/transactions/import
# multiform: file => arquivio.csv
```
## after initial setup
```sh
# caso o container não esteja rodando
docker start gostack_postgres
# para finalizar
# docker stop gostack_gobarber

# para ver a aplicação
yarn dev:server

# para testar
yarn test --noStackTrace
```
