# API Documentation

Esta API fornece endpoints para criar, recuperar, atualizar e excluir itens de tarefas. Ela permite gerenciar sua lista de tarefas de forma eficiente, realizando operações CRUD nela.

## URL Base

```
https://localhost:3000/api/
```

## Endpoints

A API suporta os seguintes endpoints:

---

### Nota

**As requisições devem ser feitas com o tipo JSON**

```
Content-Type: application/json
```

---

**Recuperar todas as tarefas**

```HTTP
GET /api/todos
```

- **Resposta**: Array JSON contendo todos os itens de tarefas.
  - Exemplo de resposta:
    ```JSON
    [
      {
        "id": 1,
        "title": "Comprar vegetais",
        "content": "Não se esqueça de comprar vegetais",
        "completed": false
      },
      {
        "id": 2,
        "title": "Passear com o cachorro",
        "content": "Não se esqueça de passear com o cachorro",
        "completed": true
      }
    ]
    ```

**Criar tarefa**

```HTTP
POST /api/todos
```

- **Corpo da requisição**: Objeto JSON contendo os dados do item de tarefa.
  - Exemplo de requisição:
    ```JSON
     {
       "title": "Comprar vegetais",
       "content": "Não se esqueça de comprar vegetais",
       "completed": false
     }
    ```
- **Resposta**: Objeto JSON representando o item de tarefa criado.
  - Exemplo de resposta:
    ```JSON
      {
        "id": 1,
        "title": "Comprar vegetais",
        "content": "Não se esqueça de comprar vegetais",
        "completed": false
      }
    ```

**Recuperar tarefa específica**

```HTTP
GET /api/todos/:id
```

| Parâmetro | Tipo     | Descrição                               |
| :-------- | :------- | :-------------------------------------- |
| `id`      | `string` | O identificador único do item de tarefa |

- **Resposta**: Objeto JSON representando o item de tarefa solicitado.
  - Exemplo de requisição:
    ```HTTP
    GET /api/todos/1
    ```
  - Exemplo de resposta:
    ```JSON
      {
        "id": 1,
        "title": "Comprar vegetais",
        "content": "Não se esqueça de comprar vegetais",
        "completed": false
      }
    ```

**Atualizar tarefa**

```HTTP
PATCH /api/todos/:id
```

| Parâmetro | Tipo     | Descrição                               |
| :-------- | :------- | :-------------------------------------- |
| `id`      | `string` | O identificador único do item de tarefa |

- **Corpo da requisição**: Objeto JSON contendo os dados atualizados do item de tarefa.
  - Exemplo de requisição:
    ```HTTP
    PATCH /api/todos/1
    ```
    ```JSON
      {
        "title": "Comprar vegetais",
        "content": "Não se esqueça de comprar vegetais",
        "completed": false
      }
    ```
- **Resposta**: Objeto JSON representando o item de tarefa atualizado.
  - Exemplo de resposta:
    ```JSON
      {
        "id": 1,
        "title": "Comprar vegetais",
        "content": "Não se esqueça de comprar vegetais",
        "completed": true
      }
    ```

**Excluir tarefa**

```HTTP
DELETE /api/todos/:id
```

| Parâmetro | Tipo     | Descrição                               |
| :-------- | :------- | :-------------------------------------- |
| `id`      | `string` | O identificador único do item de tarefa |

- **Resposta**: Objeto JSON indicando o sucesso ou falha da operação de exclusão.
  - Exemplo de requisição:
    ```HTTP
    DELETE /api/todos/1
    ```
  - Exemplo de resposta:
    ```JSON
    {
      "success": true
    }
    ```

## Erros

Esta API usa os seguintes códigos de erro:

- `400 Bad Request` &rarr; A requisição estava malformada ou faltando parâmetros obrigatórios.
- `404 Not Found` &rarr; O recurso solicitado não foi encontrado.
- `500 Internal Server Error` &rarr; Ocorreu um erro inesperado no servidor.

