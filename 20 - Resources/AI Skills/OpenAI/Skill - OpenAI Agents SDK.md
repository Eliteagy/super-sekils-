---
tags: [openai, sdk, ai-agents, orchestration, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - OpenAI Agents SDK

O Agents SDK é o novo padrão oficial da OpenAI para construir agentes escaláveis, autónomos e com memória persistente. Ele simplifica drasticamente a lógica de "Loops de Agente" (Reasoning -> Planning -> Action).

## 🚀 O que é o Agents SDK?
É uma biblioteca de alto nível que substitui a construção manual de threads e histórico de chat. O SDK gere sessões, memória de longo prazo e coordenação entre múltiplos agentes nativamente.

## 🛠️ Três Conceitos Chave

### 1. Agents & Workflows
Um **Agente** tem um nome, uma personalidade e um conjunto de ferramentas. Um **Workflow** define a sequência lógica de múltiplos agentes a trabalhar juntos.

### 2. Sessions (A Nova Memória)
Em vez de guardares JSONs de chat em bases de dados à mão, o SDK usa **Sessions** (ex: `SQLiteSession`) que guardam automaticamente o estado, memória e contexto entre interações.

### 3. Runners
O **Runner** é o motor que executa o agente. Ele gere as chamadas de API, retentações e a execução paralela de ferramentas.

---

## 💻 Exemplo de Código (O Padrão 2026)

```python
from openai_agents import Agent, Runner, SQLiteSession

# Define o Agente Apollo
apollo = Agent(
    name="Apollo AI",
    instructions="És o orquestrador industrial da Elite Agency.",
    tools=["web_search", "code_executor"]
)

# Inicia um corredor com memória persistente
runner = Runner(session=SQLiteSession("apollo_memory.db"))

# Executa uma tarefa
response = runner.run(apollo, "Analisa o desempenho da Mestre Capas o trimestre passado.")
print(response.output)
```

> [!IMPORTANT]
> **Persistent State**: Com o SDK, podes parar um agente, desligar o servidor, e ao ligar novamente, ele sabe exatamente onde parou sem precisares de voltar a enviar todo o histórico.
