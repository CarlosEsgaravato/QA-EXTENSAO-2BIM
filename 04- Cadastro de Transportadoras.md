## Cenário 04: Cadastro de Transportadoras

### Caso de Teste 01: Cadastro válido.

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C04-CT01 | A transportadora será cadastrada corretamente com dados válidos.        |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                     |
| :----------------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Transportadora"                      |
| **E** preenchemos "TransLog Brasil" no campo Nome                               |
| **E** preenchemos "12.345.678/0001-90" no campo CNPJ                            |
| **E** preenchemos "endereço" no campo CEP                                       |
| **QUANDO** clicarmos no botão "Salvar"                                          |
| **ENTÃO** a transportadora será cadastrada com sucesso                          |

| **Critérios de aceitação**                |
| :---------------------------------------- |
| A transportadora deve ser registrada.     |

---

### Caso de Teste 02: CNPJ inválido.

| ID       | Descrição                                             |
| :------- | :---------------------------------------------------- |
| C04-CT02 | O cadastro deve falhar quando o CNPJ for inválido.    |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Transportadora"                   |
| **E** preenchemos "TransLog Brasil" no campo Nome                           |
| **E** preenchemos "00.000.000/0000-00" no campo CNPJ                        |
| **E** preenchemos "endereço" no campo CEP                                   |
| **QUANDO** clicarmos no botão "Salvar"                                      |
| **ENTÃO** será exibida a mensagem "CNPJ inválido"                           |

| **Critérios de aceitação**           |
| :----------------------------------- |
| O sistema deve impedir o cadastro.   |

---

### Caso de Teste 03: Transportadora já cadastrada.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C04-CT03 | O sistema deve impedir cadastro com CNPJ já registrado.              |

| **Pré-condições**                                                     |
| :-------------------------------------------------------------------- |
| Transportadora com CNPJ "12.345.678/0001-90" já cadastrada no sistema |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Transportadora"                   |
| **E** preenchemos "TransLog Brasil" no campo Nome                           |
| **E** preenchemos "12.345.678/0001-90" no campo CNPJ                        |
| **E** preenchemos "endereço" no campo CEP                                   |
| **QUANDO** clicarmos no botão "Salvar"                                      |
| **ENTÃO** o sistema exibirá "Transportadora já cadastrada"                  |

| **Critérios de aceitação**          |
| :---------------------------------- |
| Cadastro duplicado deve ser negado. |
