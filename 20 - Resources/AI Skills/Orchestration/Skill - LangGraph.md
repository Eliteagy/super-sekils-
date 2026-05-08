---
tags: [ai-agents, orchestration, langgraph, stateful-agents, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - LangGraph: Stateful Graph Orchestration

**LangGraph** é o novo padrão para construir sistemas de agentes persistentes e multi-estágio em 2026. Ao contrário das correntes lineares, o LangGraph permite ciclos (loops) e fluxos determinísticos baseados em grafos.

## 🚀 Por que LangGraph?
Sistemas de agentes puros (como o ReAct) às vezes entram em loops infinitos ou perdem o rumo. O LangGraph dá ao desenvolvedor o controlo total sobre o **Estado** e as **Transições** do agente.

---

## 🛠️ Três Pilares do LangGraph

### 1. State (O Cérebro)
Define um objeto de estado partilhado (TypedDict ou Pydantic) que todos os nós do grafo conseguem ler e escrever. Isto garante consistência.

### 2. Nodes & Edges (O Fluxo)
- **Nodes**: Funções Python individuais que realizam tarefas (ex: pesquisar web, gerar código).
- **Edges**: Regras que definem para onde o fluxo vai a seguir (condicionais ou diretas).

### 3. Persistence (Checkpoints)
O LangGraph guarda o estado do grafo em cada passo. Se o servidor falhar, o agente pode retomar exatamente do ponto onde parou.

---

## 💻 Exemplo de Orquestração (Apollo AI Context)

```python
from langgraph.graph import StateGraph, END

# Define o estado do Apollo
class ApolloState(TypedDict):
    query: str
    context: list
    answer: str

# Define o Grafo
workflow = StateGraph(ApolloState)

# Adiciona Nós
workflow.add_node("search_mcp", search_mcp_node)
workflow.add_node("generate_answer", llm_node)

# Define as Arestas (Edges)
workflow.set_entry_point("search_mcp")
workflow.add_edge("search_mcp", "generate_answer")
workflow.add_edge("generate_answer", END)

# Compila
app = workflow.compile()
```

## 🏗️ Uso na Elite Agency
- **Sales Funnel**: Um grafo que gere o lead desde o primeiro contacto (Nó 1) até ao envio do contrato (Nó Final), com aprovação humana obrigatória pelo meio.
- **Content Engine**: Nó de Ideação -> Nó de Escrita -> Nó de Revisão (Com loop se a revisão falhar).

> [!IMPORTANT]
> **Human-in-the-loop**: No LangGraph, podes "pausar" a execução de um nó e esperar por uma entrada manual do utilizador antes de o agente avançar para o passo seguinte. Ideal para segurança e controlo de qualidade.

---

## 🔗 Relacionado
- [[Skill - OpenAI Agents SDK]]
- [[Skill - Model Context Protocol (MCP)]]
- [[10 - Projects/Apollo AI]]
