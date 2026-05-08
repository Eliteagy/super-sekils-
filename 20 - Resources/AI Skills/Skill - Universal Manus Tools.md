---
tags: [skill, manus, cli, tools, pdf, universal]
source: https://github.com/yuanqi99/manus-skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Universal Manus Tools (PDF & CLI)

> **Coleção de ferramentas CLI independentes desenhadas para agentes de IA.**

## O Conceito de "Universal Skill"
Estas skills são desenhadas como pacotes Python independentes. Podem ser usadas no Manus, mas também em qualquer terminal ou IDE (Cursor, Windsurf, Claude Code).

## Ferramenta em Destaque: PDF Watermark Remover
- **Função:** Remove marcas de água (padrões repetidos ou texto semi-transparente) de ficheiros PDF.
- **Uso CLI:**
  ```bash
  pdf-watermark-remover input.pdf output.pdf
  ```

## Integração Multi-Ambiente
Para usar estas ferramentas como um agente:
1. Clonar o repositório no workspace.
2. Instalar a skill necessária (`pip install -e .`).
3. O agente pode agora invocar o comando diretamente via terminal.

## Como Aplicar no Apollo AI
- **Módulo de Utilidades:** No **Coding View** do Apollo, podemos adicionar uma aba de "Tools" que permite ao utilizador carregar um PDF e usar esta skill para "limpar" o documento antes de o processar com RAG.
- **Protocolo de Skills:** Adotar o ficheiro `SKILL.md` como padrão para todas as novas funcionalidades que adicionarmos ao Apollo.
