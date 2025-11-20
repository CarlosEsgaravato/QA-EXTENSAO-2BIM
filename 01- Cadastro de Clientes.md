## Cenário 01: Cadastro de Clientes.

### Caso de Teste 01: Cadastro de cliente com dados válidos.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT01 | O cadastro será realizado com todos os dados obrigatórios válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar na tela de cadastro de clientes. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Cliente"                |
| **E** preenchemos "CARLOS" no campo Nome                      |
| **E** preenchemos "123.456.789-00" no campo CPF                   |
| **E** preenchemos "endereço" no campo CEP                         |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** o cliente será cadastrado com sucesso                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente deve ser exibido na lista de clientes após o cadastro.|

---

### Caso de Teste 02: Tentativa de cadastrar cliente com CPF inválido.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT02 | O cadastro falhará quando o CPF informado for inválido.  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Estar na página "Cadastrar Cliente".  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Cliente"                |
| **E** preenchemos "CARLOS" no campo Nome                     |
| **E** preenchemos "11111111111" no campo CPF                      |
| **E** preenchemos "endereço" no campo CEP                         |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** uma mensagem de erro "CPF inválido" será exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema não deve permitir salvar o cadastro.    |

---

### Caso de Teste 03: Tentativa de cadastrar cliente duplicado.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT03 | O sistema deve impedir o cadastro de cliente com CPF já existente. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Cliente com CPF "123.456.789-00" já cadastrado.|

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Cliente"                |
| **E** preenchemos "CARLOS" no campo Nome                      |
| **E** preenchemos "123.456.789-00" no campo CPF                   |
| **QUANDO** clicarmos em "Salvar"                                  |
| **ENTÃO** será exibida a mensagem "Cliente já cadastrado"         |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema não deve criar um novo registro duplicado.            |

## 🔗 Evidências - https://drive.google.com/drive/folders/1d17zallpoxxXi0-iGo_6Jga_Vnb8dzHZ?usp=drive_link
