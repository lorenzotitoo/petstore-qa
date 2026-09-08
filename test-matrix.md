# Matriz de Testes — Swagger Petstore

| ID | Recurso | Endpoint | Cenário | Tipo | Status |
|---|---|---|---|---|---|
| TC-001 | User | POST /user | Criar usuário com dados válidos | Positivo | PASS |
| TC-002 | User | GET /user/{username} | Buscar usuário existente | Positivo | PASS |
| TC-003 | User | POST /user | Criar usuário com nome vazio | Negativo | FAIL |
| TC-004 | User | POST /user | Criar usuário com email vazio | Negativo | FAIL |
| TC-005 | User | POST /user | Criar usuário com body vazio | Negativo | FAIL |
| TC-006 | User | POST /user | Criar usuário com username duplicado | Negativo | FAIL |
| TC-007 | User | POST /user | Criar usuário com password vazio | Negativo | FAIL |
| TC-008 | Pet | POST /pet | Criar Pet com dados válidos | Positivo | PASS |
| TC-009 | Pet | GET /pet/{petId} | Buscar Pet existente | Positivo | PASS |
| TC-010 | Pet | PUT /pet | Atualizar Pet existente | Positivo | PASS |
| TC-011 | Pet | GET /pet/{petId} | Validar atualização do Pet | Positivo | PASS |
| TC-012 | Pet | POST /pet/{petId}/uploadImage | Realizar upload de imagem | Positivo | PASS |
| TC-013 | Pet | DELETE /pet/{petId} | Excluir Pet existente | Positivo | PASS |
| TC-014 | Pet | GET /pet/{petId} | Buscar Pet com ID inexistente | Negativo | PASS |
| TC-015 | Pet | GET /pet/{petId} | Buscar Pet com ID inválido | Negativo | PASS |
| TC-016 | Pet | POST /pet | Criar Pet com ID inválido | Negativo | PASS |
| TC-017 | Pet | PUT /pet | Atualizar Pet inexistente | Negativo | FAIL |
| TC-018 | Pet | DELETE /pet/{petId} | Excluir Pet inexistente | Negativo | PASS |
| TC-019 | Store | GET /store/inventory | Consultar inventário | Positivo | PASS |
| TC-020 | Store | POST /store/order | Criar pedido com dados válidos | Positivo | PASS |
| TC-021 | Store | GET /store/order/{orderId} | Buscar pedido existente | Positivo | PASS |
| TC-022 | Store | DELETE /store/order/{orderId} | Excluir pedido existente | Positivo | PASS |
| TC-023 | Store | GET /store/order/{orderId} | Validar pedido após exclusão | Negativo | PASS |
| TC-024 | Store | GET /store/order/{orderId} | Buscar pedido com ID inexistente | Negativo | PASS |
| TC-025 | Store | GET /store/order/{orderId} | Buscar pedido com ID inválido | Negativo | PASS |
| TC-026 | Store | POST /store/order | Criar pedido com dados inválidos | Negativo | PASS |
| TC-027 | Store | DELETE /store/order/{orderId} | Excluir pedido inexistente | Negativo | PASS |

## Resumo

| Indicador | Quantidade |
|---|---:|
| Total de casos de teste | 27 |
| PASS | 21 |
| FAIL | 6 |
| Taxa de aprovação* | 78% |

