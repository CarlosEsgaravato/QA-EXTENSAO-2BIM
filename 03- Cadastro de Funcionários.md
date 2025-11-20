## Cenário 03: Cadastro de Funcionários

### Caso de Teste 01: Cadastro de funcionário válido.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT01 | O funcionário será cadastrado com dados completos e válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Estar na página "Cadastrar Funcionário".                      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Funcionário"            |
| **E** preenchemos "Maria Souza" no campo Nome                     |
| **E** preenchemos "123.456.789-00" no campo CPF                   |
| **QUANDO** clicarmos em "Salvar"                                  |
| **ENTÃO** o funcionário será cadastrado com sucesso               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O funcionário deve aparecer na listagem.                        |

---

### Caso de Teste 02: Cadastro de funcionário sem preencher o Nome.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT02 | O cadastro falhará ao tentar salvar sem preencher o Nome.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Estar na página "Cadastrar Funcionário". |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Funcionário"            |
| **E** deixamos o campo Nome em branco                             |
| **E** preenchemos "123.456.789-00" no campo CPF                   |
| **QUANDO** clicarmos em "Salvar"                                  |
| **ENTÃO** aparecerá a mensagem "Nome é obrigatório"               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema não salva o cadastro.                                 |

---

### Caso de Teste 03: Funcionário já cadastrado.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C03-CT03 | O sistema deve impedir funcionários com CPF duplicado.            |

| **Pré-condições**                                                   |
| :------------------------------------------------------------------ |
| Funcionário com CPF "123.456.789-00" já cadastrado.                 |

| **Passos**                                                                     |
| :----------------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Funcionário"                         |
| **E** preenchemos "Maria Souza" no campo Nome                                  |
| **E** preenchemos "123.456.789-00" no campo CPF                                 |
| **QUANDO** clicarmos no botão "Salvar"                                         |
| **ENTÃO** o sistema exibirá a mensagem "Funcionário já cadastrado"             |

| **Critérios de aceitação**                  |
| :------------------------------------------ |
| Não permitir duplicidade de funcionários.   |

## 🔗 Evidências - https://drive.google.com/drive/folders/1DD1VPDQbE-s-hS40vhivYRqze2iaO2mW?usp=sharing
