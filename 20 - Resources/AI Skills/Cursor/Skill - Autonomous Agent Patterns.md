---
tags: [cursor, agents, automation, patterns, orchestration]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - Autonomous Agent Patterns

Esta skill define os padrões e estratégias para construir e orquestrar agentes de codificação autónomos dentro do ecossistema do Cursor.

## 🚀 O que faz?
Estabelece uma estrutura de trabalho para que a IA possa agir com maior autonomia e menos supervisão constante:
- **Task Decomposition**: Divide grandes problemas em sub-tarefas atómicas.
- **Self-Correction Loops**: Define protocolos para o agente testar o seu próprio código e corrigir erros.
- **Memory Management**: Estratégias para manter o contexto relevante em sessões longas.
- **Tool Selection**: Ajuda o agente a decidir quando usar o terminal, ler arquivos ou pesquisar na web.

## 🛠️ Como Implementar no Cursor

```markdown
# Autonomous Coding Agent Pattern

1. Break down user request into objective sub-tasks.
2. Execute tasks iteratively with verification steps.
3. If error occurs, analyze logs and execute self-correction.
4. Report final results with a brief summary of actions.
```

## 📈 Vantagens
- **Alta Produtividade**: Permite que o desenvolvedor se foque na lógica de alto nível enquanto a IA executa o "trabalho sujo".
- **Redução de Erros**: O loop de auto-correção garante que o código entregue já passou por verificações básicas.
- **Consistência**: Mantém o mesmo padrão de implementação em todo o projeto.

> [!TIP]
> Use estes padrões quando tiver uma tarefa repetitiva ou bem definida (ex: criar 10 componentes UI baseados num design system).
