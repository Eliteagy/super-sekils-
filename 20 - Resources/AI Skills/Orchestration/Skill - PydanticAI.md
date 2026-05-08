---
tags: [pydantic-ai, orchestration, agents, type-safety, python]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - PydanticAI (Next-Gen Agents)

PydanticAI é o novo standard para construir aplicações de agents em Python em 2026. Criado pela equipa do Pydantic, traz robustez, type-safety e uma experiência de desenvolvimento superior ao LangChain.

## 🚀 O que faz?
É um framework focado em **Production-Grade Agents**:
- **Strict Type Safety**: Usa Pydantic v2 para garantir que tanto o input quanto o output dos agentes são válidos.
- **Model-Agnostic**: Suporta OpenAI, Anthropic, Gemini e modelos locais (Ollama/NIM) via uma interface unificada.
- **Dependency Injection**: Sistema elegante para passar ferramentas e bases de dados para os agentes.
- **Built-in Instrumentation**: Loggin e monitorização nativa (Logfire).

## 🛠️ Como Implementar

```python
from pydantic_ai import Agent
from pydantic import BaseModel

class MyOutput(BaseModel):
    result: str
    confidence: float

# Definir o agente
agent = Agent('openai:gpt-4o', result_type=MyOutput)

@agent.tool
def get_user_data(ctx, user_id: str):
    return {"name": "Apollo", "status": "active"}

# Executar
result = agent.run_sync("Analisa o status do user 123")
print(result.data.result)
```

## 📈 Vantagens para o Apollo AI
- **Debugging Rápido**: Erros de tipo são apanhados imediatamente, não em runtime durante uma chamada de API cara.
- **Escalabilidade**: Ideal para orquestrar múltiplos Mini-Agentes que comunicam entre si com contratos de dados claros.
- **Modernização**: Substitui frameworks pesados e imprevisíveis por algo puramente Pythonic.

> [!TIP]
> Use o PydanticAI para construir a "Lógica de Decisão" central do Apollo, garantindo que ele nunca tenta executar uma ação com parâmetros inválidos.
