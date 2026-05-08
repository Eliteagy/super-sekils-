---
tags: [ai-infrastructure, database, vector-db, rag, pinecone, qdrant, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🏗️ Skill - Vector DBs: Pinecone & Qdrant

**Bases de Dados Vetoriais** são o "Cérebro de Longo Prazo" da Inteligência Artificial. Elas permitem que o teu agente (Apollo AI) se lembre de milhares de documentos, conversas e factos através de **Busca Semântica**.

## 🚀 O que é um Vector DB?
Ao contrário de bases de dados SQL (que procuram por palavras exatas), os Vector DBs guardam **Embeddings** (representações matemáticas de significado). Se procurares por "luxo industrial", o sistema encontrará "Red Armoury" mesmo que as palavras não coincidam.

---

## 🛠️ As Duas Escolhas de Elite

### 1. Pinecone (Serverless Power)
- **Foco**: Escalabilidade infinita na nuvem, sem gestão de servidores.
- **Vantagem**: Ideal para a **Elite Agency** crescer sem se preocupar com infraestrutura.
- **Uso**: Guardar os perfis de centenas de leads e histórico de interações.

### 2. Qdrant (Open Source & Performance)
- **Foco**: Máxima performance, suporte a filtros complexos e "Self-Hosting".
- **Vantagem**: Podes rodar o Qdrant no teu **Hacking Lab** localmente via Docker.
- **Uso**: Memória local do Apollo AI para máxima privacidade e velocidade.

---

## 💻 Como Implementar (Python Flow)

```python
import pinecone
from openai import OpenAI

# 1. Gera Embedding da tua nota de Obsidian
client = OpenAI()
res = client.embeddings.create(input="Apollo AI é o futuro.", model="text-embedding-3-small")
vector = res.data[0].embedding

# 2. Guarda no Pinecone
index = pinecone.Index("apollo-memory")
index.upsert(vectors=[("id1", vector, {"metadata": "info_projeto"})])

# 3. Pesquisa por significado
query_res = index.query(vector=query_vector, top_k=5, include_metadata=True)
```

## 🏗️ Uso no Apollo AI
- **Memória Infinita**: Carregar todos os teus ficheiros de Obsidian para o Qdrant. Assim, o Apollo sabe sempre tudo o que escreveste sem precisares de carregar os ficheiros manualmente.
- **RAG de Alta Precisão**: Usar filtros de metadados para pesquisar apenas em "10 - Projects" ou "20 - Resources".

> [!TIP]
> **Hybrid Search**: Em 2026, o padrão é usar **Busca Híbrida** (Vector + BM25 Keywords) para garantir que nomes próprios e termos técnicos específicos são sempre encontrados.

---

## 🔗 Relacionado
- [[Skill - OpenAI Embeddings API]]
- [[Skill - NVIDIA NeMo & Agent Toolkit]]
- [[00 - Dashboard]]
