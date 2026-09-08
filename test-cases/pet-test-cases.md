## TC-008 - Criar Pet

**Endpoint:** POST /pet

**Tipo:** Positivo

### Pré-condições

Nenhuma.

### Passos

1. Informar os dados válidos do Pet.
2. Enviar uma requisição POST para `/pet`.

### Resultado esperado

A API deve retornar HTTP 200 e os dados do Pet criado.

### Resultado obtido

A API retornou HTTP 200 e os dados do Pet foram retornados corretamente.

### Status

PASS

## TC-009 - Buscar Pet existente

**Endpoint:** GET /pet/{petId}

**Tipo:** Positivo

### Pré-condições

Um Pet deve estar previamente cadastrado na API.

### Passos

1. Informar o ID de um Pet existente.
2. Enviar uma requisição GET para `/pet/{petId}`.

### Resultado esperado

A API deve retornar HTTP 200 e os dados correspondentes ao Pet solicitado.

### Resultado obtido

A API retornou HTTP 200 e os dados do Pet foram retornados corretamente.

### Status

PASS

## TC-010 - Atualizar Pet existente

**Endpoint:** PUT /pet

**Tipo:** Positivo

### Pré-condições

Um Pet deve estar previamente cadastrado na API.

### Passos

1. Informar os dados atualizados do Pet.
2. Enviar uma requisição PUT para `/pet`.

### Resultado esperado

A API deve retornar HTTP 200 e os dados atualizados do Pet.

### Resultado obtido

A API retornou HTTP 200 e os dados do Pet foram atualizados corretamente.

### Status

PASS


## TC-011 - Validar atualização do Pet

**Endpoint:** GET /pet/{petId}

**Tipo:** Positivo

### Pré-condições

Um Pet deve ter sido atualizado previamente através do endpoint PUT /pet.

### Passos

1. Informar o ID do Pet atualizado.
2. Enviar uma requisição GET para `/pet/{petId}`.
3. Verificar os dados retornados.

### Resultado esperado

A API deve retornar HTTP 200 e apresentar os dados atualizados do Pet.

### Resultado obtido

A API retornou HTTP 200 e os dados atualizados foram confirmados.

### Status

PASS

## TC-012 - Upload de imagem do Pet

**Endpoint:** POST /pet/{petId}/uploadImage

**Tipo:** Positivo

### Pré-condições

Um Pet existente e um arquivo de imagem válido devem estar disponíveis.

### Passos

1. Informar o ID de um Pet existente.
2. Selecionar uma imagem para upload.
3. Enviar uma requisição POST para `/pet/{petId}/uploadImage`.
4. Verificar a resposta da API.

### Resultado esperado

A API deve retornar HTTP 200 e uma mensagem confirmando o upload do arquivo.

### Resultado obtido

A API retornou HTTP 200 e a mensagem confirmou o upload do arquivo.

### Status

PASS

## TC-013 - Excluir Pet

**Endpoint:** DELETE /pet/{petId}

**Tipo:** Positivo

### Pré-condições

Um Pet existente deve estar disponível para exclusão.

### Passos

1. Informar o ID de um Pet existente.
2. Enviar uma requisição DELETE para `/pet/{petId}`.

### Resultado esperado

A API deve retornar HTTP 200, indicando que o Pet foi excluído.

### Resultado obtido

A API retornou HTTP 200 e o Pet foi excluído.

### Status

PASS

## TC-014 - Buscar Pet com ID inexistente

**Endpoint:** GET /pet/{petId}

**Tipo:** Negativo

### Pré-condições

Não deve existir um Pet cadastrado com o ID utilizado.

### Passos

1. Informar um ID que não existe na API.
2. Enviar uma requisição GET para `/pet/{petId}`.

### Resultado esperado

A API deve retornar HTTP 404, indicando que o Pet não foi encontrado.

### Resultado obtido

A API retornou HTTP 404.

### Status

PASS

## TC-015 - Buscar Pet com ID inválido

**Endpoint:** GET /pet/{petId}

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar um valor em formato inválido no parâmetro `petId`.
2. Enviar uma requisição GET para `/pet/{petId}`.

### Resultado esperado

A API deve rejeitar o valor informado e retornar um erro relacionado ao formato do ID.

### Resultado obtido

A API retornou HTTP 404 e a resposta indicou erro de conversão do ID.

### Status

PASS

## TC-016 - Criar Pet com ID inválido

**Endpoint:** POST /pet

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar um ID em formato inválido no corpo da requisição.
2. Enviar uma requisição POST para `/pet`.

### Resultado esperado

A API deve rejeitar os dados inválidos e retornar HTTP 400.

### Resultado obtido

A API retornou HTTP 400 com a mensagem `bad input`.

### Status

PASS

## TC-017 - Atualizar Pet inexistente

**Endpoint:** PUT /pet

**Tipo:** Negativo

### Pré-condições

Não deve existir um Pet com o ID informado.

### Passos

1. Informar um ID de Pet que não existe.
2. Enviar uma requisição PUT para `/pet`.
3. Verificar a resposta da API.

### Resultado esperado

A API deve informar que o Pet não foi encontrado, caso o endpoint seja destinado exclusivamente à atualização de recursos existentes.

### Resultado obtido

A API retornou HTTP 200 e aparentemente criou um novo Pet com o ID informado.

### Status

FAIL

### Observação

O comportamento observado deve ser analisado para verificar se está de acordo com o requisito esperado para o endpoint.


## TC-018 - Excluir Pet inexistente

**Endpoint:** DELETE /pet/{petId}

**Tipo:** Negativo

### Pré-condições

Não deve existir um Pet com o ID utilizado.

### Passos

1. Informar um ID de Pet inexistente.
2. Enviar uma requisição DELETE para `/pet/{petId}`.

### Resultado esperado

A API deve retornar HTTP 404, indicando que o Pet não foi encontrado.

### Resultado obtido

A API retornou HTTP 404.

### Status

PASS