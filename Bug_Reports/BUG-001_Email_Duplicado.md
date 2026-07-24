# 🐞 BUG-001 — Cadastro permite utilização de e-mail já cadastrado

## 📋 Informações Gerais

| Campo | Valor |
|-------|-------|
| ID | BUG-001 |
| Módulo | Cadastro |
| Funcionalidade | Registro de novo usuário |
| Tipo | Regra de negócio |
| Severidade | 🔴 Alta |
| Prioridade | 🔴 Alta |
| Status | Aberto |

---

# 📝 Descrição

Durante a validação da funcionalidade de cadastro, foi identificado que o sistema permite criar uma nova conta utilizando um endereço de e-mail já existente na base de dados.

Esse comportamento viola a regra de unicidade do e-mail, podendo gerar inconsistências nos dados e conflitos de autenticação.

---

# 🎯 Objetivo do teste

Validar que o sistema impede o cadastro de usuários utilizando um e-mail previamente registrado.

---

# ⚙️ Pré-condições

- Existir um usuário previamente cadastrado no sistema.
- Estar na tela de cadastro.

---

# 🧪 Passos para reproduzir

1. Acessar a tela de cadastro.
2. Informar um e-mail já cadastrado.
3. Preencher o campo **Nome**.
4. Informar uma senha válida.
5. Confirmar a senha.
6. Clicar em **Cadastrar**.

---

# ❌ Resultado encontrado

O sistema permite concluir o cadastro utilizando um e-mail que já havia sido utilizado anteriormente.

---

# ✅ Resultado esperado

O sistema deve impedir a criação de uma nova conta utilizando um e-mail já cadastrado.

O usuário deve receber uma mensagem informando que não foi possível concluir o cadastro.

**Exemplo:**

> Não foi possível concluir o cadastro.  
> Verifique os dados informados e tente novamente.

---

# 💥 Impacto

Este comportamento pode causar:

- Duplicidade de usuários.
- Inconsistência na base de dados.
- Conflitos durante autenticação.
- Problemas na recuperação de senha.
- Possíveis riscos relacionados à segurança da aplicação.

---

# 🔒 Observação de Segurança

Aplicações com requisitos de segurança normalmente evitam informar explicitamente que um e-mail já está cadastrado.

Mensagens genéricas ajudam a reduzir o risco de enumeração de usuários, dificultando a identificação de contas existentes por terceiros.

---

# 💡 Sugestão de melhoria

Implementar uma validação de unicidade do e-mail antes da criação do usuário.

Caso o e-mail já exista, bloquear a operação e apresentar uma mensagem de erro amigável ao usuário.

---

# 📚 Referência

Bug identificado durante a execução dos testes funcionais do projeto BugBank, desenvolvido como atividade prática do workshop **"QA: a porta de entrada mais acessível para o mercado de TI"** da EBAC.****
