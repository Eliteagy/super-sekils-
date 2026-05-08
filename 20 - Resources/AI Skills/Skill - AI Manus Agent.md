---
tags: [skill, manus, agents, autonomy, execution]
source: https://github.com/Simpleyyt/ai-manus
type: skill-documentation
created: 2026-04-04
---

# Skill: AI Manus Agent Architecture

> **Implementação de agentes autónomos com capacidades de execução real.**

## O que é?
O Manus é um agente focado em "Agency" (capacidade de agir). Ao contrário de chats comuns, ele usa um loop de `Reasoning -> Execution -> Verification`.

## Componentes Técnicos
- **Autonomous Prompting:** Instruções que permitem ao agente decidir quando usar uma ferramenta sem intervenção humana.
- **Tool Integration:** APIs integradas para busca web, leitura de ficheiros e execução de scripts.
- **Workflow Loop:** 
    1. Analisar objetivo.
    2. Decompor em tarefas.
    3. Executar em Sandbox.
    4. Avaliar resultado.

## Aplicação no Apollo AI
- Implementar o "Manus Mode" no Chat do Apollo para quando precisares que a IA execute uma sequência de tarefas de DevOps ou Scraping de forma independente.
