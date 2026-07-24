# 🐞 BUG-004 — Ícone "Voltar ao login" não responde ao clique

## 📋 Informações Gerais

| Campo | Valor |
|-------|-------|
| ID | BUG-004 |
| Módulo | Cadastro |
| Funcionalidade | Navegação |
| Tipo | Usabilidade |
| Severidade | 🟢 Baixa |
| Prioridade | 🟡 Média |
| Status | Aberto |

---

# 📝 Descrição

Durante a validação da tela de cadastro, foi identificado que o ícone de seta localizado ao lado da opção **"Voltar ao login"** não executa nenhuma ação quando clicado.

Embora o link de texto funcione corretamente, o ícone não possui comportamento interativo, causando inconsistência na experiência do usuário.

---

# 🎯 Objetivo do teste

Validar se todos os elementos utilizados para navegação entre as telas respondem corretamente às ações do usuário.

---

# ⚙️ Pré-condições

- Estar na tela de cadastro de usuários.

---

# 🧪 Passos para reproduzir

1. Acessar a tela de cadastro.
2. Localizar o ícone de seta ao lado do texto **"Voltar ao login"**.
3. Clicar apenas sobre o ícone.

---

# ❌ Resultado encontrado

Nenhuma ação é executada ao clicar sobre o ícone.

---

# ✅ Resultado esperado

O ícone deve possuir o mesmo comportamento do texto **"Voltar ao login"**, redirecionando o usuário para a tela de autenticação.

---

# 💥 Impacto

- Experiência de navegação inconsistente.
- Possível confusão para o usuário.
- Redução da usabilidade da interface.

---

# 💡 Sugestão de melhoria

Associar o mesmo evento de clique do link **"Voltar ao login"** ao ícone de seta, garantindo que ambos executem a mesma ação de navegação.

---

# 📚 Referência

Bug identificado durante a execução dos testes funcionais do projeto BugBank, desenvolvido como atividade prática do workshop **"QA: a porta de entrada mais acessível para o mercado de TI"** da EBAC.
