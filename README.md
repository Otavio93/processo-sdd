# Processo de Spec-Driven Development

Este repositório reúne um fluxo de trabalho para conduzir uma funcionalidade desde a definição do problema até a implementação, validação de qualidade e revisão do código. Cada etapa está organizada como uma skill, com instruções e templates próprios.

## Etapas

1. **Criar PRD** (`01-criar-prd`) — define problema, objetivos mensuráveis, usuários, escopo e critérios de aceitação.
2. **Criar TechSpec** (`02-criar-techspec`) — transforma o PRD em arquitetura, componentes, contratos e casos de teste.
3. **Criar tasks** (`03-criar-tasks`) — divide a solução em entregas incrementais e rastreáveis até os critérios de aceitação e testes.
4. **Executar task** (`04-executar-task`) — implementa a próxima tarefa e atualiza seu estado após concluir as subtarefas e validações.
5. **Executar QA** (`05-executar-qa`) — verifica critérios de aceitação, testes, acessibilidade e responsividade, corrigindo defeitos encontrados.
6. **Executar review** (`06-executar-review`) — confere a implementação contra as regras do projeto, a TechSpec, as tarefas e os testes.

O fluxo principal é:

```text
PRD → TechSpec → Tasks → Implementação → QA → Code Review
```

## Estrutura

Cada etapa tem um `SKILL.md` com seu fluxo de trabalho. As pastas `references/` contêm os templates usados para produzir os documentos daquela etapa.

```text
processo/
├── 01-criar-prd/
│   ├── SKILL.md
│   └── references/TEMPLATE.md
├── 02-criar-techspec/
│   ├── SKILL.md
│   └── references/TEMPLATE.md
├── 03-criar-tasks/
│   ├── SKILL.md
│   └── references/
│       ├── TEMPLATE_TASKS.md
│       └── TEMPLATE_TASK.md
├── 04-executar-task/SKILL.md
├── 05-executar-qa/
│   ├── SKILL.md
│   └── references/TEMPLATE.md
└── 06-executar-review/
    ├── SKILL.md
    └── references/TEMPLATE.md
```

## Uso

Use a etapa correspondente ao trabalho solicitado. As etapas dependem dos artefatos anteriores: a TechSpec parte de um PRD; a decomposição em tarefas parte do PRD e da TechSpec; a implementação parte dos documentos e tarefas; QA e review avaliam o que foi implementado.

Os documentos de cada funcionalidade são salvos em `tasks/prd-[slug]/`, conforme as instruções de cada skill. Antes de usar este processo em um projeto, adapte os caminhos, regras, comandos de validação e convenções aos arquivos e à stack desse projeto.

## Rastreabilidade

O processo relaciona os critérios de aceitação do PRD (`CA-*`) às decisões e aos casos de teste da TechSpec (`TU-*`, `TI-*` e `E2E-*`) e às tarefas de implementação. Assim, o QA e a revisão podem verificar o que foi especificado, implementado e validado.
