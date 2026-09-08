## TC-001 - Criar usuário

**Endpoint:** POST /user

**Tipo:** Positivo

### Pré-condições

Nenhuma.

### Passos

1. Informar dados válidos para o usuário.
2. Enviar uma requisição POST para `/user`.

### Resultado esperado

A API deve retornar HTTP 200 e uma resposta indicando que o usuário foi criado com sucesso.

### Resultado obtido

A API retornou HTTP 200 e confirmou a criação do usuário.

### Status

PASS

## TC-002 - Buscar usuário existente

**Endpoint:** GET /user/{username}

**Tipo:** Positivo

### Pré-condições

Um usuário deve estar previamente cadastrado na API.

### Passos

1. Informar o username de um usuário existente.
2. Enviar uma requisição GET para `/user/{username}`.
3. Verificar os dados retornados.

### Resultado esperado

A API deve retornar HTTP 200 e os dados correspondentes ao usuário solicitado.

### Resultado obtido

A API retornou HTTP 200 e os dados do usuário foram retornados corretamente.

### Status

PASS

## TC-003 - Criar usuário com nome vazio

**Endpoint:** POST /user

**Tipo:** Negativo

### Pré-condições
FAILInformar um usuário com o campo `firstName` vazio.
2. Manter os demais dados válidos.
3. Enviar uma requisição POST para `/user`.

### Resultado esperado

A API deve rejeitar o cadastro devido ao campo `firstName` estar vazio e retornar um código de erro apropriado.

### Resultado obtido

API retornou 200 e criou o usuário

### Status

FAIL


## TC-004 - Criar usuário com email vazio

**Endpoint:** POST /user

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar um usuário com o campo `email` vazio.
2. Manter os demais dados válidos.
3. Enviar uma requisição POST para `/user`.

### Resultado esperado

A API deve rejeitar o cadastro devido ao campo `email` estar vazio e retornar um código de erro apropriado.

### Resultado obtido

API retornou 200 e criou o usuário

### Status

FAIL


## TC-005 - Criar usuário com body vazio

**Endpoint:** POST /user

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Enviar uma requisição POST para `/user` sem conteúdo no corpo da requisição.
2. Verificar a resposta da API.

### Resultado esperado

A API deve rejeitar a requisição devido à ausência dos dados necessários para criação do usuário.

### Resultado obtido

API retornou 200 e criou o usuário

### Status

FAIL


## TC-006 - Criar usuário com username duplicado

**Endpoint:** POST /user

**Tipo:** Negativo

### Pré-condições

Deve existir um usuário cadastrado com o username utilizado no teste.

### Passos

1. Criar um usuário com um username válido.
2. Enviar novamente uma requisição POST utilizando o mesmo username.
3. Verificar a resposta da API.

### Resultado esperado

A API deve rejeitar a criação do segundo usuário devido ao username já estar cadastrado.

### Resultado obtido

API retornou 200 e criou o usuário

### Status

FAIL


## TC-007 - Criar usuário com password vazio

**Endpoint:** POST /user

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar um usuário com o campo `password` vazio.
2. Manter os demais dados válidos.
3. Enviar uma requisição POST para `/user`.

### Resultado esperado

A API deve rejeitar o cadastro devido ao campo `password` estar vazio e retornar um código de erro apropriado.

### Resultado obtido

API retornou 200 e criou o usuário

### Status

FAIL