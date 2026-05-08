---
tags: [skill, manus, claude, desktop, integration]
source: https://github.com/emsi/MyManus
type: skill-documentation
created: 2026-04-04
---

# Skill: MyManus (Claude Desktop Sync)

> **Integração do Manus AI como uma "Skill" dentro do Claude Desktop.**

## O que é?
O MyManus permite que o Claude Desktop utilize o motor do Manus para realizar tarefas que o Claude sozinho não conseguiria (como navegação web complexa e execução de tarefas de longa duração).

## Funcionamento (Loop Agêntico)
1. **Plan:** O agente cria um plano de ação.
2. **Execute:** Executa as subtarefas sistematicamente.
3. **Observe:** Analisa o resultado de cada passo.
4. **Iterate:** Adapta a estratégia se encontrar obstáculos.

## Configuração no Windows
- **Ficheiro:** `windows_claude_desktop_config.json`
- **Ferramentas:** Utiliza o Playwright MCP para automação de browser.

## Como Aplicar no Apollo AI
- **Modo "Companion":** Podemos configurar o Chat do Apollo para atuar como um "MyManus", delegando tarefas de pesquisa web via Playwright sempre que o utilizador pedir dados em tempo real de 2024/2025.
