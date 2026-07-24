# 🐞 BUG-002 — Campos permanecem preenchidos ao retornar para a tela de cadastro

## 📋 Informações Gerais

| Campo | Valor |
|-------|-------|
| ID | BUG-002 |
| Módulo | Cadastro |
| Funcionalidade | Registro de novo usuário |
| Tipo | Usabilidade |
| Severidade | 🟡 Média |
| Prioridade | 🟡 Média |
| Status | Aberto |

---

# 📝 Descrição

Após realizar um cadastro com sucesso, ao retornar para a tela de cadastro utilizando a opção **"Registrar novamente"**, todos os campos permanecem preenchidos com os dados anteriormente utilizados.

Esse comportamento pode causar confusão ao usuário e facilitar o envio de informações incorretas ou duplicadas.

---

# 🎯 Objetivo do teste

Validar se o formulário é reiniciado corretamente ao iniciar um novo cadastro.

---

# ⚙️ Pré-condições

- Ter concluído um cadastro com sucesso.
- Permanecer na tela de confirmação do cadastro.

---

# 🧪 Passos para reproduzir

1. Realizar um cadastro válido.
2. Aguardar a confirmação do cadastro.
3. Clicar em **Registrar novamente**.

---

# ❌ Resultado encontrado

Os campos permanecem preenchidos com os dados utilizados no cadastro anterior.

---

# ✅ Resultado esperado

Ao iniciar um novo cadastro, todos os campos do formulário devem estar vazios.

---

# 💥 Impacto

- Experiência do usuário prejudicada.
- Possibilidade de envio de dados incorretos.
- Possibilidade de cadastros duplicados.

---

# 💡 Sugestão de melhoria

Limpar automaticamente todos os campos do formulário sempre que o usuário iniciar um novo cadastro.

---

# 📚 Referência

Bug identificado durante a execução dos testes funcionais do projeto BugBank, desenvolvido como atividade prática do workshop **"QA: a porta de entrada mais acessível para o mercado de TI"** da EBAC.
