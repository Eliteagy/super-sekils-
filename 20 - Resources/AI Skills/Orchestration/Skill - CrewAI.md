---
tags: [ai-agents, orchestration, crewai, role-playing, teams, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - CrewAI: Role-Based Multi-Agent Teams

**CrewAI** é o framework focado em equipas de agentes que colaboram de forma intuitiva, baseada em "Papéis" (Roles). É ideal para processos que imitam equipas humanas, como pesquisa, redação e análise de mercado.

## 🚀 Por que CrewAI?
Ao contrário do LangGraph (que é técnico e baseado em grafos), o CrewAI é narrativo e focado em **Tarefas** e **Delegação**. É a ferramenta perfeita para a **Elite Agency** prototipar fluxos de trabalho humanos em minutos.

---

## 🛠️ Três Pilares do CrewAI

### 1. Agents (As Personas)
Define agentes com nomes, histórias de fundo (backstory) e objetivos claros.
- **Exemplo**: O "Market Research Specialist" focado em encontrar as tendências de e-commerce para a Mestre Capas.

### 2. Tasks (As Missões)
Define o que deve ser feito e qual o output esperado. As tarefas podem ser sequenciais ou paralelas.

### 3. Crew (A Equipa)
O "Manager" que junta os agentes e as tarefas, gerindo a colaboração e a partilha de conhecimento entre eles.

---

## 💻 Exemplo de Orquestração (Elite Agency Context)

```python
from crewai import Agent, Task, Crew

# Agente Investigador
researcher = Agent(
  role='Pesquisador de Leads',
  goal='Encontrar novas leads qualificadas no setor de e-commerce.',
  backstory='És um mestre em OSINT e LinkedIn Sales Navigator.',
  tools=[search_tool]
)

# Agente Copywriter
writer = Agent(
  role='Email Copywriter',
  url='Escrever e-mails de vendas frios de alta conversão.',
  backstory='És um mestre da persuasão focado no Red Armoury branding.'
)

# Missão de Vendas
sales_task = Task(description='Pesquisa 10 leads e escreve e-mails personalizados.', agent=researcher)

# A Equipa de Vendas
sales_crew = Crew(agents=[researcher, writer], tasks=[sales_task])
sales_crew.kickoff()
```

## 🏗️ Uso na Elite Agency
- **Campanhas de Marketing**: Uma equipa de (Pesquisador + Estrategista + Copywriter) gera uma campanha completa em 5 minutos.
- **Social Media Engine**: Um agente analisa os posts virais da semana e outro adapta os ganchos para o estilo da agência.

> [!TIP]
> **Autoconsistência**: No CrewAI, podes pedir a um agente para "rever" o trabalho do outro antes de o entregar, garantindo que o nível de qualidade da Elite Agency é mantido.

---

## 🔗 Relacionado
- [[Skill - OpenAI Agents SDK]]
- [[Skill - LangGraph]]
- [[10 - Projects/The Elite Agency]]
