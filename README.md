# API Testing — Swagger Petstore

Projeto de testes funcionais de API desenvolvido utilizando
Postman, com foco na validação de endpoints, respostas HTTP,
regras de negócio e cenários positivos e negativos.

## Objetivo

Praticar e demonstrar conceitos de testes de API, incluindo:

- Criação e execução de casos de teste
- Testes positivos e negativos
- Validação de códigos HTTP
- Validação do corpo das respostas
- Uso de variáveis de ambiente
- Scripts de teste no Postman
- Encadeamento de requisições
- Identificação e documentação de defeitos
- Execução de uma coleção de testes

## Tecnologias e ferramentas

- Postman
- JavaScript
- REST API
- JSON
- GitHub

## API utilizada

Swagger Petstore

Base URL:

`https://petstore.swagger.io/v2`

## Recursos testados

### User

- Criação de usuário
- Consulta de usuário
- Validação de campos obrigatórios
- Validação de body
- Username duplicado

### Pet

- Criação de Pet
- Consulta de Pet
- Atualização de Pet
- Upload de imagem
- Exclusão de Pet
- Cenários com IDs inválidos ou inexistentes

### Store

- Consulta de inventário
- Criação de pedido
- Consulta de pedido
- Exclusão de pedido
- Cenários negativos

## Estrutura do projeto

postman-qa/
├── postman/
│   └── Petstore.postman_collection.json
├── test-cases/
│   ├── user-test-cases.md
│   ├── pet-test-cases.md
│   └── store-test-cases.md
├── bug-reports/
├── test-matrix.md
└── README.md