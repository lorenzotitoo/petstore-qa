# API Testing — Swagger Petstore

Projeto de testes funcionais de API desenvolvido utilizando
Postman, com foco na validação de endpoints, respostas HTTP,
regras de negócio e cenários positivos e negativos.

## Objetivo

- Praticar testes de API utilizando Postman;
- Criar e organizar casos de teste;
- Validar status codes e respostas da API;
- Desenvolver testes positivos e negativos;
- Trabalhar com variáveis de ambiente e dados dinâmicos;
- Realizar upload de arquivos através da API;
- Identificar e documentar comportamentos inesperados;
- Automatizar a execução da Collection através do Postman CLI;
- Integrar os testes ao GitHub Actions;
- Gerar relatórios de execução em HTML e JUnit.

## Tecnologias e ferramentas

- **Postman** — criação e execução dos testes de API;
- **Postman CLI** — execução automatizada da Collection;
- **Git / GitHub** — versionamento do projeto;
- **GitHub Actions** — integração contínua (CI);
- **YAML** — configuração do workflow;
- **HTML** — relatório visual dos testes;
- **JUnit XML** — relatório estruturado para integração com ferramentas de CI/CD.


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

## 📊 Matriz de testes

Os casos de teste estão documentados na matriz:

```text
test-matrix.md
```

A matriz apresenta informações como:

- ID do caso de teste;
- Cenário;
- Endpoint;
- Resultado esperado;
- Resultado obtido;
- Status do teste.

---

## ⚙️ Automação

Os testes podem ser executados localmente utilizando o **Postman CLI**.

Exemplo:

```bash
cd postman

postman collection run "PetStore.postman_collection.json" \
  --environment "PetStore.postman_environment.json"
```

A execução utiliza a mesma Collection criada no Postman, permitindo automatizar os testes sem depender da interface gráfica.

---

## 🚀 CI/CD — GitHub Actions

O projeto possui um workflow de **GitHub Actions** responsável por executar automaticamente os testes.

O pipeline é executado quando ocorre:

- Push na branch `main`;
- Pull Request direcionado para `main`.

## 📄 Relatórios

Ao final da execução, são gerados dois tipos de relatório:

### HTML

Relatório visual da execução dos testes.

```text
postman-report.html
```

### JUnit XML

Relatório estruturado para integração com ferramentas de CI/CD.

```text
postman-report.xml
```

Os relatórios são disponibilizados através do **Artifact `postman-test-reports`** em cada execução do GitHub Actions.

