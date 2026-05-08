---
tags: [ai-agents, orchestration, autogen, conversation, multi-agent, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - AutoGen: Conversational Multi-Agent Framework

**AutoGen** é o framework da Microsoft para construir agentes que conversam uns com os outros para resolver problemas complexos. É a ferramenta de eleição para fluxos que exigem iteração constante e depuração autónoma.

## 🚀 Por que AutoGen?
Ao contrário de frameworks lineares, o AutoGen foca-se na **Conversa**. Imagina um programador IA a escrever código e um revisor IA a testá-lo e a dar feedback até estar perfeito—isso é AutoGen.

---

## 🛠️ Três Pilares do AutoGen

### 1. Customizable Agents
Podes criar agentes com diferentes LLMs (ex: um corre Llama 3 no Groq e outro corre GPT-4o) para otimizar custos e performance.

### 2. Conversation Patterns
Define como os agentes falam:
- **Two-agent Chat**: Diálogo direto.
- **Group Chat**: Múltiplos agentes a colaborar (ex: Gestor, Programador, Tester).
- **Hierarchical Chat**: Um agente "Chefe" delega a sub-agentes.

### 3. Tool Interaction
Os agentes do AutoGen são mestres em usar ferramentas de sistema (terminal, browsers) e podem até escrever as suas próprias ferramentas se necessário.

---

## 💻 Exemplo de Orquestração (Apollo AI Context)

```python
from autogen import AssistantAgent, UserProxyAgent

# Agente de Código
coder = AssistantAgent(name="Coder", llm_config=llm_config)

# Agente que executa o código e reporta erros
executor = UserProxyAgent(name="Executor", code_execution_config={"work_dir": "coding"})

# Inicia a conversa de depuração automática
executor.initiate_chat(coder, message="Cria um componente React para a Mestre Capas.")
```

## 🏗️ Uso na Elite Agency
- **DevOps Autónomo**: O Coder escreve o código, o Executor testa-o, e o Coder corrige até passar em todos os testes sem intervenção humana.
- **Data Scientist Agent**: Um agente extrai dados do CRM e outro gera gráficos e relatórios PDF usando Python.

> [!TIP]
> **Cost Optimization**: Usa o AutoGen com modelos locais via **Ollama** ou **LM Studio** para tarefas internas pesadas de depuração antes de mandares o código final para produção.

---

## 🔗 Relacionado
- [[Skill - OpenAI Agents SDK]]
- [[Skill - LangGraph]]
- [[Skill - DeepSeek V3]]
