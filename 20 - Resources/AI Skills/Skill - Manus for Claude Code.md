---
tags: [skill, manus, claude-code, cli, autonomous-coding]
source: https://github.com/emsi/MyManus
type: skill-documentation
created: 2026-04-04
---

# Skill: Manus for Claude Code (CLI)

> **Plugin de autonomia para o Claude Code (CLI da Anthropic).**

## Diferenciais da Versão CLI
- **Native Tools:** Utiliza as ferramentas nativas do Claude Code (Bash, Read, Write, Edit, Grep).
- **Zero Configuration:** Auto-configuração do servidor Playwright MCP via `.mcp.json`.
- **Foco em Dev:** Ideal para automação de tarefas de desenvolvimento (escrever testes, refatorar código, pesquisar documentação técnica).

## Comandos Úteis (Claude Code)
```bash
# Adicionar o marketplace do MyManus
/plugin marketplace add https://github.com/emsi/MyManus.git

# Instalar o plugin
/plugin install mymanus@mymanus
```

## Casos de Uso Recomendados
- **Investigação Profunda:** Pesquisar múltiplas fontes e gerar reportes com citações.
- **Web Scraping Autónomo:** Recolher dados de produtos ou notícias sem supervisão.
- **Workflows Multi-etapa:** Planeamento e execução de projetos de software completos.

## Aplicação no Apollo AI
- **Apollo CLI Skill:** Se implementarmos uma CLI para o Apollo, podemos usar esta lógica de "Marketplace de Plugins" para permitir que o utilizador instale novas skills dinamicamente.
