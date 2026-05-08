---
tags: [skill, anthropic, artifacts, web, ui]
source: https://github.com/anthropics/skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Anthropic Web Artifacts Builder

> **Guia para criar sistemas que geram e renderizam UI dinamicamente.**

## O que é?
Este padrão permite que o Claude (ou o Apollo AI) crie componentes de interface (React/HTML), os execute num ambiente seguro e os apresente ao utilizador num "Canvas" separado do chat.

## Componentes Técnicos
- **Frontend Environment:** Geralmente usa React + Tailwind + Lucide Icons.
- **Sandboxing:** O código gerado deve ser isolado para segurança.
- **Iterative Updates:** O LLM deve ser capaz de editar partes específicas do código sem reescrever tudo (padrão `diff`).

## Instrução de Sistema (Prompts)
- "Age como um experiente engenheiro de frontend."
- "Gera código React auto-contido que execute numa única página."
- "Usa componentes visuais de alto impacto (glassmorphism, gradients)."

## Como Usar no Apollo AI
- Implementar uma aba de "Preview" ao lado do Coding View.
- Quando o Apollo detetar que está a criar UI, ele renderiza o Artifact automaticamente.
