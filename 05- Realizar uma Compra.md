## Cenário 05: Realizar uma Compra

### Caso de Teste 01: Compra válida.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C06-CT01 | A compra será registrada corretamente quando os dados forem válidos |

| **Pré-condições** |
| :---------------- |
| Fornecedor e produtos cadastrados. |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na página "Registrar Compra"                                    |
| **E** selecionamos o fornecedor "Intelbras LTDA"                              |
| **E** adicionamos o produto "Camiseta" quantidade "10"                   |
| **QUANDO** clicarmos em "Confirmar Compra"                                           |
| **ENTÃO** a compra será registrada com sucesso                                       |

| **Critérios de aceitação**                     |
| :--------------------------------------------- |
| A compra deve ser salva corretamente no sistema |

---

### Caso de Teste 02: Compra sem fornecedor.

| ID       | Descrição                                                          |
| :------- | :----------------------------------------------------------------- |
| C06-CT02 | O sistema deve impedir registrar compra sem selecionar fornecedor. |

| **Pré-condições** |
| :---------------- |
| Produtos cadastrados. |

| **Passos**                                                                      |
| :------------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Compra"                                |
| **E** não selecionamos nenhum fornecedor                                         |
| **E** adicionamos o produto "Camiseta" quantidade "10"               |
| **QUANDO** clicarmos em "Confirmar Compra"                                       |
| **ENTÃO** deve ser exibida a mensagem "Selecione um fornecedor"                 |

| **Critérios de aceitação**   |
| :--------------------------- |
| O sistema deve bloquear a compra |

---

### Caso de Teste 03: Compra sem produtos.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C06-CT03 | O sistema deve impedir registrar compra sem itens.           |

| **Pré-condições** |
| :---------------- |
| Fornecedor cadastrado. |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que estamos na página "Registrar Compra"                           |
| **E** selecionamos o fornecedor "Intelbras LTDA"                     |
| **E** não adicionamos nenhum produto                                        |
| **QUANDO** clicarmos em "Confirmar Compra"                                  |
| **ENTÃO** será exibida a mensagem "Adicione pelo menos um produto"          |

| **Critérios de aceitação**    |
| :---------------------------- |
| A compra não deve ser registrada |

## 🔗 Evidências - https://drive.google.com/drive/folders/1fZLdpKSTavkdGeDPGD4rSdFHzdLID-iU?usp=drive_link
