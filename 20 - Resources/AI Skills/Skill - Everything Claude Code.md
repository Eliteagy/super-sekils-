---
tags: [skill, claude-code, ecc, optimization, orchestration, patterns, dx]
source: https://github.com/affaan-m/everything-claude-code
type: skill-documentation
created: 2026-05-05
---

# Skill: Everything Claude Code (ECC)

> **O framework definitivo de otimização e orquestração para Claude Code e agentes CLI.**

O **Everything Claude Code (ECC)**, criado por affaan-m, é um ecossistema massivo de agentes, skills e guardrails desenhado para levar a performance de ferramentas como Claude Code e Cursor ao limite absoluto.

## 🚀 Arquitetura e Orquestração

O ECC utiliza uma abordagem de **Multi-Agent Orchestration** para manter o contexto do agente principal limpo e eficiente:

- **28+ Sub-agentes especializados**: `typescript-reviewer`, `tdd-agent`, `security-auditor`, `build-resolver`, entre outros.
- **119+ Skills On-demand**: Bibliotecas de conhecimento específicas para ecossistemas (Bun, Next.js, PyTorch, Rust, Go, etc.).
- **Cross-Platform**: Configurações sincronizadas via `AGENTS.md` para Claude Code, Cursor (`.cursor/`), e Codex.

## 🧠 Aprendizagem Contínua (v1 & v2)

Um dos pilares do ECC é o sistema que permite ao agente acumular "experiência" entre sessões:

- **/learn**: Comando para extrair padrões de código bem-sucedidos e guardá-los em `~/.claude/skills/learned/`.
- **/learn-eval**: Avalia a utilidade dos padrões aprendidos.
- **/checkpoint**: Salva o estado atual da sessão para recuperação rápida.

## 🛡️ Segurança e Guardrails (AgentShield)

O ECC implementa camadas rigorosas de proteção:

- **Hook-based Enforcement**: Bloqueia comandos inseguros (ex: `git --no-verify`) e deteta segredos em prompts.
- **Config Protection**: Impede que agentes desativem linters ou modifiquem ficheiros críticos de segurança.
- **Red-Teaming Pipeline**: O flag `--opus` ativa um ciclo de três agentes (red-team/blue-team/auditor) para testar vulnerabilidades na configuração.

## 📊 Otimização de Contexto

- **Harness Audit**: Identifica "token bloat" (desperdício de tokens) na configuração e histórico.
- **SQLite State Store**: Gestão de persistência de sessão fora do contexto de texto.
- **Selective Install**: Sistema de instalação modular que permite carregar apenas o necessário para o projeto atual.

## 📚 Comandos Essenciais (ECC)

| Comando | Descrição |
| :--- | :--- |
| `/learn` | Extrai padrões e cria novas skills aprendidas. |
| `/checkpoint` | Cria um ponto de restauro do estado do agente. |
| `/audit` | Analisa a eficiência do contexto e uso de tokens. |
| `/agent <name>` | Invoca um sub-agente especializado para uma sub-tarefa. |

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/affaan-m/everything-claude-code)
- [The Shortform Guide](https://github.com/affaan-m/everything-claude-code/blob/main/the-shortform-guide.md)

---
*Gerado via Gemini CLI para a The Elite Agency.*
