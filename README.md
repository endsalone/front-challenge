# Task App

## Desafio

Você pode ajudar os usuários a controlarem suas tarefas do dia-a-dia com uso do Angular conforme o wireframe abaixo:
![wireframe](https://github.com/endsalone/front-challenge/blob/master/assets/desafio-entrevista.jpg?raw=true)

Recomendamos o uso do [Angular Material](https://material.angular.io/guide/getting-started) para facilitar o desenvolvimento, caso sinta-se a vontade com outra lib de componentes estilizados sinta-se a vontade de fazer uso.

Também recomendamos que a aplicação esteja integrada com o backend conforme listado na sessão de contrato, caso não consiga, tudo bem! Você pode usar o localstorage e abusar do data binding 😃.

## Regras
- A aplicação não deve permitir que o usuário insira um texto que contenha caractere especial [{(!@#$%^&*()_+)\}] com exceção de acentos (ãéçô...)
- Ao clicar no select a aplicação deve sinalizar que a tarefa foi concluída, enviando um PUT para a API com o a opção de "done" como true
- Ao clicar no botão de excluir o item deve ser removido da lista e o request com DELETE deve ser enviado para a API
- A API possuí limite de 100 itens não deve permitir mais isso

### Contratos da API
A collection do POSTMAN está na pasta "postman-collection"  

Listagem de Tarefas

    GET /api/v1/tasks HTTP/1.1
    Host: 61088c1dd73c6400170d3981.mockapi.io
    
    Response 200
    {
        "items": [
            {
                "item": "lorem",
                "done": false,
                "id": "1"
            }
        ]
    }

Criar Tarefa

    POST /api/v1/tasks HTTP/1.1
    Host: 61088c1dd73c6400170d3981.mockapi.io
    
    Body
    {
        "item": "lorem",
        "done": false
    }

Atualizar Tarefa para Feito "done"

    PUT /api/v1/tasks/{id} HTTP/1.1
    Host: 61088c1dd73c6400170d3981.mockapi.io
    
    Body
    {
        "item": "lorem",
        "done": true
    }

Deletar Tarefa

    DELETE /api/v1/tasks/{id} HTTP/1.1
    Host: 61088c1dd73c6400170d3981.mockapi.io
    
    Response
    {
        "item": "lorem",
        "done": false,
        "id": 11,
    }


### O que será avaliado?
- Qualidade do Software
- Testes Unitários e Teste Funcional


## Entrega do projeto
- Envie o link do projeto GIT para o email que recebeu este desafio.

Desejamos boa sorte e que a força esteja contigo 🖖🤓
