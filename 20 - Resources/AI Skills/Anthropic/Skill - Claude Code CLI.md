---
tags: [anthropic, claude-code, ai-agents, autonomous-coding, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🧥 Skill - Claude Code CLI

O **Claude Code** é o agente de engenharia de software da Anthropic que corre diretamente no teu terminal. Ele não apenas sugere código—ele **executa** comandos, corrige ficheiros e melhora codebases inteiras.

## 🚀 Funcionalidades de Elite (Versão 4.6)

### 1. Auto Mode (Modo Autónomo)
Permite ao Claude resolver problemas complexos (ex: "Migra este site de React para Next.js") sem pedir permissão para cada alteração, usando guardas de segurança inteligentes.

### 2. Computer Use (GUI Interaction)
Através de screenshots e controlo de rato/teclado virtual, o Claude consegue navegar em sites, testar interfaces e preencher formulários como um humano.

### 3. MCP (Model Context Protocol) Integration
O Claude Code liga-se a fontes de dados externas (Bases de dados, GitHub, Slack) via MCP para ter contexto total sobre o teu negócio.

---

## 🛠️ Como Instalar e Usar

```bash
# Instalação (npm)
npm install -g @anthropic-ai/claude-code

# Iniciar o agente na pasta do teu projeto
claude login
claude init

# Exemplos de Comandos
/ask "Explica como o Apollo AI gere a memória."
/write "Cria um script para exportar leads da Elite Agency para CSV."
/fix "Corrige o bug de carregamento na splash screen da Mestre Capas."
```

## 📈 Vantagens para o Apollo AI
- **Contexto de 1M Tokens**: O Claude pode ler todo o código do Apollo de uma só vez para encontrar bugs de arquitetura.
- **Teste Real**: O Claude pode abrir o teu site local e clicar em botões para ver se o checkout da Mestre Capas está a funcionar.

> [!IMPORTANT]
> **Skills Discovery**: O Claude Code aprende com as tuas ferramentas locais. Se tiveres o Docker instalado, ele saberá usá-lo automaticamente para testar contentores.
