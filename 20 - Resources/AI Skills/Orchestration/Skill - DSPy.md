---
tags: [ai-agents, orchestration, dspy, optimization, prompt-engineering, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - DSPy: Programmatic Prompt Optimization

**DSPy** (Declarative Self-Improving Python) é o framework que está a substituir o "Prompt Engineering" manual em 2026. Em vez de escreveres prompts à mão, o DSPy **otimiza** os teus pedidos e os pesos do modelo programaticamente.

## 🚀 Por que DSPy?
Prompts manuais são frágeis. Se mudares do GPT-4o para o Llama 3, o teu prompt antigo pode falhar. O DSPy permite que definas a **assinatura** da tarefa e ele "compila" o melhor prompt para o modelo que estiveres a usar.

---

## 🛠️ Três Pilares do DSPy

### 1. Signatures (O "O que fazer")
Define o input e o output de forma declarativa.
- **Exemplo**: `question -> answer`.

### 2. Modules (As Peças)
Componentes como `Predict`, `ChainOfThought` ou `ProgramOfThought` que estruturam como o modelo deve raciocinar.

### 3. Teleprompters (O Otimizador)
O "coração" do DSPy. Ele corre a tua tarefa em centenas de exemplos de teste e **aprende** qual é o melhor prompt para maximizar a precisão.

---

## 💻 Exemplo de Otimização (Elite Agency Context)

```python
import dspy

# Define a assinatura: Recebe um lead e escreve um e-mail.
class LeadEmail(dspy.Signature):
    """Escrever e-mail de vendas frio de alta conversão."""
    lead_info = dspy.InputField()
    email_draft = dspy.OutputField()

# Módulo de Raciocínio (Chain of Thought)
assistant = dspy.ChainOfThought(LeadEmail)

# Otimização Automática (Teleprompter)
# O DSPy vai testar vários prompts até encontrar o que melhor converte!
optimizer = dspy.telepropmter.BootstrapFewShot(metric=my_conversion_metric)
optimized_assistant = optimizer.compile(assistant, trainset=my_leads_dataset)
```

## 🏗️ Uso Estratégico
- **Multi-Model Portability**: Escrever a lógica uma vez e o DSPy adapta o prompt para Groq/Llama, NVIDIA/Nemotron ou OpenAI/GPT.
- **Auto-Melhoria**: Deixar o sistema otimizar os e-mails de vendas da Elite Agency com base nos resultados reais de clique e resposta.

> [!IMPORTANT]
> **O Fim do Prompt Engineering**: Em 2026, os engenheiros de topo não escrevem prompts; eles escrevem **Sistemas DSPy** que geram prompts melhores que qualquer humano conseguiria.

---

## 🔗 Relacionado
- [[Skill - OpenAI Agents SDK]]
- [[Skill - DeepSeek V3]]
- [[20 - Resources/AI Skills/Orchestration/Skill - LangGraph]]
