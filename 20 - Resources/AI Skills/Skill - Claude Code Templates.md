---
tags: [skill, claude-code, automation, templates]
source: https://github.com/davila7/claude-code-templates
type: skill-documentation
created: 2026-04-04
---

# Skill: Claude Code Advanced Templates

> **Uma biblioteca massiva de templates para maximizar o uso do Claude Code CLI.**

## Categorias de Templates
- **Project Bootstrapping:** Configuração imediata de ambientes Next.js, Vite, Python FastAPI.
- **Refactoring:** Scripts para converter código legado para padrões modernos (ex: JS para TS).
- **Security Auditing:** Blueprints de testes de segurança automatizados.
- **API Design:** Templates para gerar Specs de OpenAPI a partir de prompts.

## Padrão de Estrutura (.claude)
A biblioteca usa ficheiros `.md` dentro de `.claude/` para definir instruções persistentes por projeto.
- `CLAUDE.md`: O ficheiro mestre que define regras de build, test e style.

## Estratégia Apollo AI
- Integrar estes templates no "Coding View" do Apollo.
- Quando o utilizador inicia um "New Project", o Apollo oferece uma lista de templates desta biblioteca para acelerar o setup.
