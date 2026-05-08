---
tags: [nvidia, nemo, agent-toolkit, multimodal]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - NVIDIA NeMo & Agent Toolkit

NeMo é o framework da NVIDIA para construir, personalizar e implantar modelos Generative AI. O **Agent Toolkit** é a peça-chave para orquestrar fluxos complexos de agentes.

## 🤖 O que é o NeMo Agent Toolkit?
É uma biblioteca "framework-agnostic" que permite perfilar, avaliar e otimizar agentes que usam LangChain, LangGraph ou CrewAI em infraestrutura NVIDIA.

## 🛠️ Três Pilares do NeMo

### 1. Guardrails (Segurança)
Impõe limites para evitar que os teus agentes respondam a tópicos proibidos ou fujam do "TOM" da **Elite Agency**.
```yaml
# config.yaml (Colang)
define user express greeting
  "olá"
  "boa tarde"

define bot greet back
  "Olá! Bem-vindo ao centro de comando da Elite Agency."
```

### 2. Retriever (RAG de Elite)
Otimizado para usar GPUs para pesquisa vetorial massiva com o `cuVS`. Ideal para bases de conhecimento gigantes (como este Obsidian!).

### 3. Agentic Routing
Encaminha pedidos para diferentes modelos dependendo da complexidade:
- **Groq/Llama-8B**: Para respostas rápidas e simples.
- **NIM/Nemotron-70B**: Para raciocínio logico profundo.

---

## 🚀 Integração no Apollo AI
Podes usar o NeMo para:
- **Digital Branding**: Garantir que o agente "Apollo" nunca saia da persona industrial/luxo.
- **Busca Eficiente**: Usar o NeMo Retriever para que o Apollo consiga ler este vault em milissegundos.

> [!IMPORTANT]
> **Performance**: NeMo permite treinar "LoRAs" (Low-Rank Adaptation) em frações do tempo normal, permitindo que cada agente da agência tenha uma especialidade única (ex: Redator vs Programador).
