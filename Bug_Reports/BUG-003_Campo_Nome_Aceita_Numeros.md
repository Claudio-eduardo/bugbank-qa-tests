# 🐞 BUG-003 — Campo "Nome" permite inserção de números

## 📋 Informações Gerais

| Campo | Valor |
|-------|-------|
| ID | BUG-003 |
| Módulo | Cadastro |
| Funcionalidade | Validação do formulário |
| Tipo | Validação de entrada |
| Severidade | 🟡 Média |
| Prioridade | 🟡 Média |
| Status | Aberto |

---

# 📝 Descrição

Durante a validação do formulário de cadastro, foi identificado que o campo **Nome** aceita valores numéricos, permitindo a criação de usuários com informações inválidas.

Esse comportamento compromete a qualidade dos dados armazenados e indica ausência de validação adequada para o campo.

---

# 🎯 Objetivo do teste

Validar que o campo **Nome** aceite apenas caracteres compatíveis com nomes de pessoas.

---

# ⚙️ Pré-condições

- Estar na tela de cadastro.

---

# 🧪 Passos para reproduzir

1. Acessar a tela de cadastro.
2. Informar apenas números no campo **Nome**.
3. Preencher os demais campos com dados válidos.
4. Clicar em **Cadastrar**.

---

# ❌ Resultado encontrado

O sistema aceita valores numéricos no campo **Nome** e permite concluir o cadastro.

---

# ✅ Resultado esperado

O sistema deve validar o conteúdo do campo **Nome**, impedindo a inserção de valores inválidos.

Caso seja identificado um valor incompatível, deve exibir uma mensagem orientando o usuário a informar um nome válido.

---

# 💥 Impacto

- Baixa qualidade dos dados cadastrados.
- Inconsistência nas informações dos usuários.
- Possibilidade de registros inválidos na base de dados.

---

# 💡 Sugestão de melhoria

Implementar validação no campo **Nome**, permitindo apenas caracteres compatíveis com nomes de pessoas, conforme as regras definidas para a aplicação.

---

# 📚 Referência

Bug identificado durante a execução dos testes funcionais do projeto BugBank, desenvolvido como atividade prática do workshop **"QA: a porta de entrada mais acessível para o mercado de TI"** da EBAC.
