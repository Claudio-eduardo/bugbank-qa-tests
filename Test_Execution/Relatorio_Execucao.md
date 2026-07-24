# Relatório de Execução dos Testes - BugBank

## 1. Objetivo

Este documento apresenta os resultados obtidos durante a execução dos testes funcionais realizados no módulo de cadastro da aplicação BugBank.

---

# 2. Informações Gerais

| Item | Descrição |
|------|-----------|
| Projeto | BugBank |
| Tipo de Teste | Teste Funcional Manual |
| Módulo | Cadastro de Usuários |
| Executor | Claudio Eduardo |
| Ferramenta de documentação | GitHub + Markdown |

---

# 3. Resumo da Execução

| Métrica | Quantidade |
|----------|-----------:|
| Casos de teste planejados | 5 |
| Casos executados | 5 |
| Casos aprovados | 1 |
| Casos reprovados | 4 |

---

# 4. Resultado por Caso de Teste

| ID | Caso de Teste | Resultado |
|----|---------------|-----------|
| CT-001 | Cadastro com dados válidos | ✅ Aprovado |
| CT-002 | Cadastro utilizando e-mail já existente | ❌ Reprovado |
| CT-003 | Validação do campo Nome | ❌ Reprovado |
| CT-004 | Limpeza do formulário após cadastro | ❌ Reprovado |
| CT-005 | Navegação para tela de Login | ❌ Reprovado |

---

# 5. Bugs Identificados

| ID | Descrição |
|----|-----------|
| BUG-001 | Cadastro permite utilização de e-mail já cadastrado |
| BUG-002 | Campos permanecem preenchidos após novo cadastro |
| BUG-003 | Campo Nome aceita números |
| BUG-004 | Ícone "Voltar ao login" não responde ao clique |

---

# 6. Conclusão

Durante a execução dos testes funcionais do módulo de cadastro foram identificadas inconsistências relacionadas à validação de dados, usabilidade e navegação.

Os bugs encontrados foram registrados individualmente para facilitar sua rastreabilidade e futura correção.

Apesar de o fluxo principal de cadastro funcionar corretamente, recomenda-se a correção das falhas identificadas antes da disponibilização da funcionalidade em ambiente de produção.
