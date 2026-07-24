# Plano de Testes - BugBank

## 1. Objetivo

Este documento tem como objetivo definir o planejamento dos testes funcionais realizados no módulo de cadastro da aplicação BugBank, descrevendo o escopo, estratégia, critérios e ambiente utilizados durante a execução dos testes.

---

# 2. Escopo

Os testes contemplam exclusivamente a funcionalidade de cadastro de usuários.

Foram avaliados:

- Cadastro com dados válidos;
- Validação de campos obrigatórios;
- Validação de e-mail duplicado;
- Validação do campo Nome;
- Navegação entre telas;
- Comportamento do formulário após o cadastro.

---

# 3. Tipo de Teste

Os testes realizados neste projeto são classificados como:

- Teste Funcional Manual;
- Teste de Validação;
- Teste de Interface (UI);
- Teste Negativo;
- Teste Positivo.

---

# 4. Ambiente de Testes

| Item | Descrição |
|------|-----------|
| Sistema | BugBank |
| Plataforma | Web |
| Navegador | Google Chrome |
| Tipo de teste | Manual |

---

# 5. Critérios de Entrada

Para iniciar a execução dos testes é necessário:

- Sistema disponível;
- Página de cadastro acessível;
- Ambiente funcionando normalmente.

---

# 6. Critérios de Saída

A execução será considerada concluída quando:

- Todos os casos de teste forem executados;
- Os bugs encontrados forem documentados;
- Os resultados forem registrados.

---

# 7. Casos de Teste Planejados

| ID | Descrição |
|----|-----------|
| CT-001 | Cadastro realizado com sucesso |
| CT-002 | Cadastro utilizando e-mail já existente |
| CT-003 | Validação do campo Nome |
| CT-004 | Campos permanecem preenchidos |
| CT-005 | Navegação para tela de Login |

---

# 8. Riscos

Os principais riscos considerados durante os testes são:

- Instabilidade da aplicação;
- Alterações na interface durante a execução;
- Mudanças nas regras de negócio.

---

# 9. Entregáveis

Ao final da atividade serão entregues:

- Plano de Testes;
- Casos de Teste;
- Relatório de Bugs;
- Relatório de Execução dos Testes.

---

# 10. Considerações

Este plano foi elaborado para documentar a estratégia utilizada durante os testes funcionais do módulo de cadastro da aplicação BugBank, servindo como referência para organização, execução e rastreabilidade das atividades de Quality Assurance.
