# Lista de Tarefas (Todo List)
API simples que possui operações básicas de CRUD (Criar, Ler, Atualizar e Deletar) para gerenciar uma lista de tarefas.

## Começando
Estas instruções irão te ajudar a obter uma cópia do projeto rodando em sua máquina local para fins de desenvolvimento e teste.

Além disso, você precisará ler a [**Documentação da API**](https://github.com/elysonsarmento/todo-api-nodejs/blob/master/Documentation.md).

### Pré-requisitos
- Baixar e instalar [Node.js](https://nodejs.org/en)
- Baixar e instalar [PostgreSQL](https://www.postgresql.org/download/) e como instalá-lo usando [Docker](https://www.docker.com/) através do [Docker Hub](https://hub.docker.com/_/postgres)
- Um navegador web (por exemplo, Google Chrome, Mozilla Firefox, Microsoft Edge)
- Um editor de texto (por exemplo, Visual Studio Code, Sublime Text)
- Uma plataforma para testar APIs como o [Postman](https://www.postman.com/downloads/)
- Motor de banco de dados (por exemplo, [DBeaver](https://dbeaver.io/download/), [DataGrip](https://www.jetbrains.com/datagrip/download/))

### Instalação
1. Clone o repositório para sua máquina local:
    ```bash
    https://github.com/elysonsarmento/todo-api-nodejs.git
    ```
2. Instale os [pacotes necessários] com:
    ```bash
    npm install
    ```
3. Configure as variáveis de ambiente, como a URL do banco de dados.
4. Execute:
    ```bash
    npm run build
    npm run start
    ```
   ou use:
    ```bash
    npm run dev
    ```

## Ferramentas & Tecnologias
- TypeScript
- Node.js
  - Express.js
- PostgreSQL
- Prisma (ORM)
