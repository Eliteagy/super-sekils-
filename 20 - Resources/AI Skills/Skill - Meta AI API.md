---
tags: [skill, meta, llama3, api, scraping]
source: https://github.com/Strvm/meta-ai-api
type: skill-documentation
created: 2026-04-04
---

# Skill: Meta AI API (Llama 3 & Web Search)

> **Interação com o Meta AI sem necessidade de API Key oficial.**

## Destaques
- **Llama 3:** Acesso direto ao modelo da Meta.
- **Web Search:** Conectado à internet via Bing em tempo real.
- **Zero Cost:** Não requer créditos ou chaves de API.

## Implementação Básica (Python)
```python
from meta_ai_api import MetaAI

ai = MetaAI()
response = ai.prompt(message="Quais as últimas notícias sobre agentes de IA hoje?")
print(response['message'])
print(response['sources']) # Links das fontes reais
```

## Funcionalidades Avançadas
- **Streaming:** `ai.prompt(message="...", stream=True)` para respostas em tempo real.
- **Conversas Contínuas:** Mantém o contexto das perguntas anteriores automaticamente.
- **Novas Conversas:** `new_conversation=True` para resetar o contexto.

## Quando Usar no Apollo AI
- Quando precisares de **verificação de factos em tempo real** sem gastar tokens de busca do Gemini/Claude.
- Como "fallback" gratuito para tarefas de chat geral.
