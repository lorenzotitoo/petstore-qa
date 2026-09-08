## TC-019 - Consultar inventário

**Endpoint:** GET /store/inventory

**Tipo:** Positivo

### Pré-condições

Nenhuma.

### Passos

1. Enviar uma requisição GET para `/store/inventory`.
2. Verificar a resposta da API.

### Resultado esperado

A API deve retornar HTTP 200 e apresentar as quantidades de Pets agrupadas por status.

### Resultado obtido

A API retornou HTTP 200 e apresentou os dados do inventário.

### Status

PASS

## TC-020 - Criar pedido

**Endpoint:** POST /store/order

**Tipo:** Positivo

### Pré-condições

Deve existir um Pet disponível para ser associado ao pedido.

### Passos

1. Informar os dados válidos do pedido.
2. Enviar uma requisição POST para `/store/order`.
3. Verificar a resposta da API.

### Resultado esperado

A API deve retornar HTTP 200 e os dados do pedido criado.

### Resultado obtido

A API retornou HTTP 200 e o pedido foi criado corretamente.

### Status

PASS


## TC-021 - Buscar pedido existente

**Endpoint:** GET /store/order/{orderId}

**Tipo:** Positivo

### Pré-condições

Um pedido deve ter sido previamente cadastrado.

### Passos

1. Informar o ID de um pedido existente.
2. Enviar uma requisição GET para `/store/order/{orderId}`.

### Resultado esperado

A API deve retornar HTTP 200 e os dados correspondentes ao pedido solicitado.

### Resultado obtido

A API retornou HTTP 200 e os dados do pedido foram retornados corretamente.

### Status

PASS

## TC-022 - Excluir pedido

**Endpoint:** DELETE /store/order/{orderId}

**Tipo:** Positivo

### Pré-condições

Um pedido existente deve estar disponível para exclusão.

### Passos

1. Informar o ID de um pedido existente.
2. Enviar uma requisição DELETE para `/store/order/{orderId}`.

### Resultado esperado

A API deve retornar HTTP 200, indicando que o pedido foi excluído.

### Resultado obtido

A API retornou HTTP 200 e o pedido foi excluído.

### Status

PASS


## TC-023 - Validar exclusão do pedido

**Endpoint:** GET /store/order/{orderId}

**Tipo:** Positivo

### Pré-condições

Um pedido deve ter sido excluído previamente.

### Passos

1. Informar o ID do pedido excluído.
2. Enviar uma requisição GET para `/store/order/{orderId}`.

### Resultado esperado

A API deve retornar HTTP 404, indicando que o pedido não foi encontrado.

### Resultado obtido

A API retornou HTTP 404.

### Status

PASS


## TC-024 - Buscar pedido inexistente

**Endpoint:** GET /store/order/{orderId}

**Tipo:** Negativo

### Pré-condições

Não deve existir um pedido com o ID utilizado.

### Passos

1. Informar um ID de pedido inexistente.
2. Enviar uma requisição GET para `/store/order/{orderId}`.

### Resultado esperado

A API deve retornar HTTP 404, indicando que o pedido não foi encontrado.

### Resultado obtido

A API retornou HTTP 404.

### Status

PASS

## TC-025 - Buscar pedido com ID inválido

**Endpoint:** GET /store/order/{orderId}

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar um valor em formato inválido no parâmetro `orderId`.
2. Enviar uma requisição GET para `/store/order/{orderId}`.

### Resultado esperado

A API deve rejeitar o valor informado e retornar um erro relacionado ao formato do ID.

### Resultado obtido

A API retornou HTTP 404 com a mensagem "java.lang.NumberFormatException: For input string: \"abc\""

### Status

PASS

## TC-026 - Criar pedido com dados inválidos

**Endpoint:** POST /store/order

**Tipo:** Negativo

### Pré-condições

Nenhuma.

### Passos

1. Informar dados inválidos no corpo da requisição.
2. Enviar uma requisição POST para `/store/order`.
3. Verificar a resposta da API.

### Resultado esperado

A API deve rejeitar os dados inválidos e retornar um código de erro HTTP 404.

### Resultado obtido

A API retornou HTTP 404 com a mensagem "bad input"

### Status

PASS


## TC-027 - Excluir pedido inexistente

**Endpoint:** DELETE /store/order/{orderId}

**Tipo:** Negativo

### Pré-condições

Não deve existir um pedido com o ID utilizado.

### Passos

1. Informar um ID de pedido inexistente.
2. Enviar uma requisição DELETE para `/store/order/{orderId}`.

### Resultado esperado

A API deve retornar HTTP 404, indicando que o pedido não foi encontrado.

### Resultado obtido

A API retornou HTTP 404.

### Status

PASS