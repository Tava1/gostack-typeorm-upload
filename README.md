# Desafio 06 - Back-end Node.js, TypeORM e Upload de arquivos

Aplicando os conhecimentos de Node.js e TypeScript.

Repositório front-end: <a href="https://github.com/Tava1/gostack-typeorm-upload">Desafio 07 - Fundamentos ReactJS :atom_symbol:</a>


## Utilizando o projeto
Após clonar, certifique-se de estar na raíz do projeto.

### Instalação de dependências :arrow_down: :
Basta rodar o comando ```yarn``` e aguardar a instalação de todas as depêndencias.

### Configuração do banco de dados :minidisc:
Para este back-end utilizei o ```POSTGRES``` como banco de dados.

Logo, é necessário possuír uma base de dados ```POSTGRES``` para que a aplicação funcione de imediato.

- Recomendo utilizar um container docker.

Com uma instância do ```POSTGRES``` ativa em ```localhost:5432``` devemos prepara-lá para receber os dados.

#### Criando o banco e as tabelas :minidisc:

- Crie um banco de dados com o nome ```gostack_desafio06``` .

- Na raiz do projeto, abra o terminal e execute o comando ```yarn typeorm migration:run``` . Este comando é responsável por criar todas as tabelas necessárias da aplicação.

Se houver necessidade de modificar a conexão do banco de dados, sugiro análizar o arquivo ```ormconfig.json```

```
{
  "type": "postgres",
  "host": "localhost",
  "port": 5432,
  "username": "postgres",
  "password": "docker",
  "database": "gostack_desafio06",
  "entities": ["./src/models/*.ts"],
  "migrations": ["./src/database/migrations/*.ts"],
  "cli": {
    "migrationsDir": "./src/database/migrations"
  }
}
```

### Inicialização do projeto :arrow_up: :
Aṕos concluir o passo anterior, para inicializar o servidor digite o comando ```yarn dev:server``` no terminal.
