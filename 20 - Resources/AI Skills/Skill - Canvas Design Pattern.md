---
tags: [skill, anthropic, canvas, design, layout]
source: https://github.com/anthropics/skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Canvas Design Pattern

> **Padrões para interfaces de "tela infinita" e organização espacial de IA.**

## O que é?
Este padrão ensina a IA a gerir não apenas texto, mas a posição e relação de elementos num espaço visual (Canvas).

## Princípios de Design
- **Spatial Hierarchy:** Elementos mais importantes são maiores e centralizados.
- **Relational Lines:** Usar conectores visuais para mostrar fluxos de pensamento ou dados.
- **Dynamic Resizing:** Componentes que se ajustam automaticamente ao conteúdo gerado pelo LLM.

## Instruções de Prompting
- "Desenha o layout como um mapa mental interativo."
- "Organiza os módulos de forma que o fluxo de informação seja da esquerda para a direita."
- "Permite que cada bloco de conteúdo seja minimizado ou expandido."

## Aplicação no Apollo AI
- Implementar um modo de "Whiteboard" onde o Apollo pode "colar" notas do Obsidian e criar diagramas de arquitetura vivos.
