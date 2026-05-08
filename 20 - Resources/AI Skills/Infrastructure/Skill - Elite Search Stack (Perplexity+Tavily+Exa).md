---
tags: [perplexity, tavily, exa, search, rag, web-access, knowledge-retrieval]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - Elite Search Stack (Perplexity/Tavily/Exa)

Para que um agente AI seja "Elite" em 2026, ele não pode depender apenas de conhecimento estático. Esta tríade de APIs de busca define como os agentes acedem ao mundo real.

## 🚀 O que faz cada Peça?
- **Perplexity API (Sonar)**: Transforma a web num LLM. Ideal para obter respostas curadas e citadas diretamente.
- **Tavily AI**: Motor de busca construído especificamente para agentes LLM. Filtra ruído, anúncios e SEO-spam, entregando apenas conteúdo puro.
- **Exa (antiga Metaphor)**: Pesquisa semântica baseada em redes neurais. Em vez de palavras-chave, pesquisa por "significado" (ex: "sites que explicam mecânica quântica por analogia").

## 🛠️ Como Implementar (Tavily Python)

```python
from tavily import TavilyClient

tavily = TavilyClient(api_key="TAVILY_API_KEY")

# Pesquisa otimizada para agentes
response = tavily.search(
    query="Qual a última versão do NVIDIA NIM?",
    search_depth="advanced",
    max_results=5
)

for result in response['results']:
    print(f"Title: {result['title']}, Content: {result['content']}")
```

## 📈 Vantagens para o Apollo AI
- **Fact Checking**: O Apollo pode validar afirmações em tempo real pesquisando fontes confiáveis.
- **Deep Research**: Use o Tavily para coletar dados técnicos e o Exa para encontrar artigos científicos obscuros.
- **Up-to-date Knowledge**: O Apollo saberá de notícias que aconteceram há 5 minutos atrás.

> [!TIP]
> Use o **Exa** quando precisar de encontrar "anéis de conhecimento" ou sites que tenham uma estrutura específica, ignorando o ranking tradicional do Google.
