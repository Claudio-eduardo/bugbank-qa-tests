# Casos de Teste — Cadastro de Usuário

## Sistema testado

BugBank

## Objetivo

Validar o funcionamento da tela de cadastro de usuários, contemplando o fluxo principal de criação de conta e cenários de erro relacionados à validação de dados, usabilidade e regras de negócio.

---

# CT-001 — Cadastro realizado com dados válidos

**Tipo:** Happy Path

## Cenário

O usuário preenche todos os campos obrigatórios com dados válidos e realiza o cadastro com sucesso.

## Pré-condição

O e-mail utilizado não deve estar previamente cadastrado no sistema.

## Dados de teste

| Campo | Valor |
|-------|-------|
| E-mail | teste@email.com |
| Nome | Usuário Teste |
| Senha | Senha@123 |
| Confirmar senha | Senha@123 |
| Criar conta com saldo | Opcional |

## Passos

1. Acessar a tela de login.
2. Clicar em **Registrar**.
3. Preencher todos os campos obrigatórios.
4. Selecionar ou não a opção **Criar conta com saldo**.
5. Clicar em **Cadastrar**.

## Resultado esperado

O sistema deve criar a conta com sucesso e apresentar uma mensagem de confirmação.

---

# CT-002 — Tentativa de cadastro com e-mail já utilizado

**Tipo:** Teste Negativo

## Cenário

O usuário tenta criar uma nova conta utilizando um e-mail já cadastrado.

## Pré-condição

Deve existir uma conta cadastrada utilizando o e-mail informado.

## Passos

1. Acessar a tela de cadastro.
2. Informar um e-mail já existente.
3. Preencher o campo **Nome**.
4. Informar uma senha válida.
5. Confirmar a senha.
6. Clicar em **Cadastrar**.

## Resultado encontrado

O sistema permite criar uma nova conta utilizando um e-mail já cadastrado.

## Resultado esperado

O sistema deve impedir a criação da conta e informar que não foi possível concluir o cadastro.

**Exemplo de mensagem:**

> Não foi possível concluir o cadastro. Verifique os dados informados e tente novamente.

### Observação de Segurança

Em aplicações que possuem requisitos de segurança, recomenda-se utilizar mensagens genéricas para evitar a enumeração de usuários, impedindo que terceiros descubram se um e-mail está ou não cadastrado no sistema.

---

# CT-003 — Campos permanecem preenchidos ao acessar novamente o cadastro

**Tipo:** Teste Funcional

## Cenário

O usuário realiza um cadastro, não efetua login e acessa novamente a tela de cadastro.

## Pré-condição

O formulário deve ter sido preenchido e enviado anteriormente.

## Passos

1. Acessar a tela de cadastro.
2. Preencher todos os campos.
3. Clicar em **Cadastrar**.
4. Não realizar login.
5. Acessar novamente a tela de cadastro.

## Resultado encontrado

Os campos permanecem preenchidos com os dados utilizados anteriormente.

## Resultado esperado

Todos os campos devem ser exibidos vazios ao acessar novamente a tela de cadastro, evitando reutilização ou exposição indevida das informações do usuário.

---

# CT-004 — Campo Nome aceita somente números

**Tipo:** Teste de Validação

## Cenário

O usuário tenta realizar um cadastro preenchendo o campo **Nome** apenas com números.

## Pré-condição

O usuário deve estar na tela de cadastro.

## Dados de teste

| Campo | Valor |
|-------|-------|
| Nome | 12345 |
| E-mail | teste@email.com |
| Senha | Senha@123 |
| Confirmar senha | Senha@123 |

## Passos

1. Acessar a tela de cadastro.
2. Informar apenas números no campo **Nome**.
3. Preencher os demais campos corretamente.
4. Clicar em **Cadastrar**.

## Resultado encontrado

O sistema aceita o cadastro mesmo com o campo Nome contendo apenas números.

## Resultado esperado

O sistema deve impedir o cadastro e solicitar um nome válido.

O campo Nome deve aceitar letras, espaços, acentos, hífens e apóstrofos.

Exemplos válidos:

- João da Silva
- Ana Paula
- José Antônio
- Maria D'Ávila

---

# CT-005 — Ícone "Voltar ao login" não executa ação

**Tipo:** Teste Funcional

## Cenário

O usuário tenta retornar para a tela de login clicando apenas no ícone de seta localizado ao lado da opção **Voltar ao login**.

## Pré-condição

O usuário deve estar na tela de cadastro.

## Passos

1. Acessar a tela de cadastro.
2. Localizar a opção **Voltar ao login**.
3. Clicar somente no ícone de seta.

## Resultado encontrado

Nenhuma ação é executada.

## Resultado esperado

O ícone de seta e o texto **Voltar ao login** devem funcionar como uma única área clicável e redirecionar o usuário para a tela de login.

---

# CT-006 — Tentativa de cadastro com campos obrigatórios vazios

**Tipo:** Teste Negativo

## Cenário

O usuário tenta realizar o cadastro sem preencher os campos obrigatórios.

## Pré-condição

O usuário deve estar na tela de cadastro.

## Passos

1. Acessar a tela de cadastro.
2. Deixar todos os campos obrigatórios vazios.
3. Clicar em **Cadastrar**.

## Resultado encontrado

O sistema bloqueia o cadastro.

## Resultado esperado

O sistema deve impedir o cadastro e indicar claramente quais campos obrigatórios precisam ser preenchidos.

**Status:** ✅ Aprovado

---

# Resumo da Execução

| ID | Caso de Teste | Resultado |
|----|---------------|-----------|
| CT-001 | Cadastro com dados válidos | ✅ Aprovado |
| CT-002 | Cadastro com e-mail já utilizado | ❌ Bug encontrado |
| CT-003 | Campos permanecem preenchidos | ❌ Bug encontrado |
| CT-004 | Campo Nome aceita somente números | ❌ Bug encontrado |
| CT-005 | Ícone Voltar ao login não funciona | ❌ Bug encontrado |
| CT-006 | Campos obrigatórios vazios | ✅ Aprovado |
