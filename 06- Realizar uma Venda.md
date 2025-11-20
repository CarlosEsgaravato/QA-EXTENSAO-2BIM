## Cenário 06: Realizar uma Venda

### Caso de Teste 01: Venda válida.

| ID       | Descrição                                            |
| :------- | :--------------------------------------------------- |
| C07-CT01 | A venda será registrada corretamente com dados válidos |

| **Pré-condições** |
| :---------------- |
| Cliente e produtos cadastrados. |

| **Passos**                                                                |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                          |
| **E** selecionamos o cliente "João Silva"                                 |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"         |
| **QUANDO** clicarmos em "Finalizar Venda"                                 |
| **ENTÃO** a venda será concluída com sucesso                              |

| **Critérios de aceitação** |
| :-------------------------- |
| A venda deve ser registrada |

---

### Caso de Teste 02: Produto sem estoque.

| ID       | Descrição                                             |
| :------- | :---------------------------------------------------- |
| C07-CT02 | O sistema deve impedir venda quando não há estoque    |

| **Pré-condições** |
| :---------------- |
| Produto com estoque 0. |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                    |
| **E** selecionamos o cliente "João Silva"                           |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"   |
| **QUANDO** clicarmos em "Finalizar Venda"                           |
| **ENTÃO** será exibida a mensagem "Estoque insuficiente"            |

| **Critérios de aceitação**    |
| :---------------------------- |
| A venda deve ser bloqueada     |

---

### Caso de Teste 03: Venda sem cliente.

| ID       | Descrição                                        |
| :------- | :----------------------------------------------- |
| C07-CT03 | O sistema deve impedir venda sem selecionar cliente |

| **Pré-condições** |
| :---------------- |
| Produto com estoque disponível. |

| **Passos**                                                                |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                          |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"         |
| **E** deixamos o campo cliente vazio                                      |
| **QUANDO** clicarmos em "Finalizar Venda"                                 |
| **ENTÃO** será exibida a mensagem "Selecione um cliente"                  |

| **Critérios de aceitação** |
| :--------------------------- |
| O sistema deve impedir concluir a venda |

## 🔗 Evidências - 
