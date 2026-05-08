---
tags: [anthropic, claude, mcp, interoperability, tools, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🧥 Skill - Model Context Protocol (MCP)

O **Model Context Protocol (MCP)** é o novo padrão universal da Anthropic para a interoperabilidade entre IAs e fontes de dados. Ele permite que o Claude aceda a ferramentas, ficheiros e bases de dados de forma segura e padronizada.

## 🚀 O que é o MCP?
É o "USB para IA". Em vez de escreveres uma integração diferente para o Claude, GPT e Gemini, escreves um **MCP Server**. O Claude liga-se a esse servidor e ganha "super-poderes" instantâneos.

---

## 🛠️ Três Componentes do Ecossistema

### 1. Resources (Dados)
Coleções de dados de leitura que o Claude pode consultar (ex: logs de servidor, base de dados de leads da Elite Agency).

### 2. Tools (Ações)
Funções que o Claude pode executar no teu computador ou na nuvem (ex: criar um repositório no GitHub, enviar um e-mail pelo n8n).

### 3. Prompts (Templates)
Modelos de prompt partilhados que garantem que o Claude sabe exatamente como lidar com os dados que recebe.

---

## 💻 Como Configurar (Protocolo 2026)

Para dares acesso ao Claude ao teu sistema de ficheiros local:
```json
// config.json (Claude Desktop)
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "./apollo-ai-code"]
    },
    "google-drive": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-google-drive"]
    }
  }
}
```

## 🏗️ Uso Estratégico
- **Memória Infinita**: Criar um MCP Server que lê todo este vault de Obsidian e o entrega ao Claude como contexto rico.
- **Automação de Agência**: Um MCP que liga o Claude ao CRM da Elite Agency para qualificar leads em tempo real.
- **Deep Research**: Usar o MCP de pesquisa (Brave/Google) para que o Claude encontre as IAs mais potentes de 2026 antes de mais ninguém.

> [!TIP]
> **Interoperabilidade**: O MCP não é só para o Claude. Muitos outros agentes (incluindo o Apollo AI) estão a adotar este padrão para usar as mesmas ferramentas.
