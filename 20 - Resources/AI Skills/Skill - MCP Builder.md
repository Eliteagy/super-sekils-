---
tags: [skill, mcp, development, integration]
source: https://github.com/ComposioHQ/awesome-claude-skills
type: skill-documentation
created: 2026-04-04
---

# Skill: MCP Server Development

> **Guia para criar servidores MCP (Model Context Protocol) de alta qualidade.**

## O que é?
Permite que o Apollo AI (ou qualquer LLM) interaja com serviços externos através de ferramentas (tools) bem desenhadas em Python ou TypeScript.

## Fases de Desenvolvimento

### 1. Pesquisa e Planeamento
- **Build for Workflows:** Não apenas "wrap" endpoints de API. Cria ferramentas que resolvam tarefas completas (ex: `schedule_event` em vez de apenas `create_entry`).
- **Context Efficient:** Retorna apenas o que é essencial. O contexto é um recurso escasso.
- **LLM-Friendly Errors:** Erros devem sugerir a próxima ação ("Tenta usar filter='active_only'").

### 2. Implementação (SDKs)
- **Python (FastMCP):** `pip install fastmcp`. Usa `@mcp.tool`. 
- **TypeScript:** `@modelcontextprotocol/sdk`. Usa `server.registerTool`.

### 3. Melhores Práticas
- **Schema Validation:** Usa Pydantic (Python) ou Zod (TS) para validar inputs.
- **Async/Await:** Sempre para operações de I/O.
- **Truncation:** Implementa limites de caracteres (ex: 25k tokens) para evitar overflow no contexto.

## Documentação de Referência
- Protocolo: `https://modelcontextprotocol.io/llms-full.txt`
- SDK Python: `https://github.com/modelcontextprotocol/python-sdk`
- SDK TS: `https://github.com/modelcontextprotocol/typescript-sdk`
