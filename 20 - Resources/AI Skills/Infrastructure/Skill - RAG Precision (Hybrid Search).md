---
tags: [ai-infrastructure, rag, hybrid-search, reranking, embeddings, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🏗️ Skill - RAG Precision: Hybrid Search & Reranking

**RAG** (Retrieval-Augmented Generation) evoluiu em 2026 para além da simples "pesquisa vetorial". Para obteres respostas 100% precisas no **Apollo AI**, precisas de dominar a **Busca Híbrida** e o **Reranking**.

## 🚀 O que é o RAG Precision?
É a combinação de múltiplos métodos de busca para garantir que a IA encontra a informação certa, mesmo que as palavras do utilizador sejam vagas ou técnicas.

---

## 🛠️ Três Pilares do RAG de Elite

### 1. Hybrid Search (O Melhor de Dois Mundos)
Combina a **Busca Semântica** (Vector DB) com a **Busca de Palavras-Chave** (BM25/SQL).
- **Semântica**: Encontra "luxo" quando procuras por "caro".
- **Palavras-Chave**: Garante que o código "Eyes-ID-v2" é encontrado exatamente como foi escrito.

### 2. Reranking (O Filtro de Qualidade)
Depois de obteres os melhores 20 resultados, usas um modelo de **Reranker** (ex: BGE-Reranker ou Cohere) para reordená-los com base na relevância real para a pergunta final. Isto elimina o "ruído".

### 3. Query Expansion / Rewrite
O agente "reescreve" a pergunta do utilizador de 3 formas diferentes para garantir que cobre todos os ângulos de pesquisa na tua base de dados (Hypothetical Document Embeddings - HyDE).

---

## 💻 Como Implementar (Python Flow)

```python
import qdrant_client
from cohere import Client as Cohere

# 1. Busca Híbrida (Vector + Keyword)
results = qdrant.search(
    collection_name="apollo-docs",
    query_vector=my_vector,
    limit=20
)

# 2. Reranking para encontrar a "pérola" de informação
co = Cohere(api_key="COHERE_API_KEY")
reranked = co.rerank(
    model='rerank-english-v3.0',
    query="Como funciona o Red Armoury?",
    documents=[r.metadata['text'] for r in results],
    top_n=3
)
```

## 🏗️ Uso no Apollo AI
- **Apollo Deep Brain**: Usar Reranking para garantir que o Apollo não alucina sobre informações do teu Obsidian.
- **Support Engine**: Dar suporte técnico à Mestre Capas com 100% de precisão nos manuais de produtos.

> [!TIP]
> **Context Window**: Em 2026, com janelas de contexto de 1M tokens, o RAG é usado para **Filtrar** e não apenas para "resumir". Mandar os documentos certos é mais importante do que mandar muitos.

---

## 🔗 Relacionado
- [[Skill - Vector DBs (Pinecone & Qdrant)]]
- [[Skill - OpenAI Embeddings API]]
- [[Skill - Liquid AI (LFMs)]]
