---
tags: [openai, api, responses-api, tools, search]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - OpenAI Responses API

A **Responses API** é a evolução unificada das chamadas de chat e do antigo Assistants API. Ela oferece uma interface simplificada para lidar com ferramentas (Tool Choice) e pesquisa de ficheiros (File Search) nativamente.

## 🚀 O que é a Responses API?
Em vez de gerires múltiplos "objetos" de assistente, a Responses API permite que especifiques ferramentas e ficheiros diretamente num pedido de chat, com suporte nativo para persistência de estado (Sessions).

---

## 🛠️ Três Funcionalidades de Elite

### 1. Tool Call Automation
O modelo decide automaticamente quando usar uma ferramenta (ex: `get_weather` ou `execute_python_code`) e agora consegue lidar com chamadas paralelas muito mais complexas.

### 2. File Search Integration
Podes enviar PDFs, CSVs ou Excel diretamente no pedido. O OpenAI faz o RAG (Retrieval-Augmented Generation) interno por ti, poupando-te a criação de uma base de dados vetorial externa.

### 3. Native Connectivity
Liga-se diretamente ao **Connector Registry**, permitindo que o teu agente aceda a dados do Google Drive, Notion ou Salesforce sem que tenhas de escrever o código da API de cada um.

---

## 💻 Exemplo de Consumo

```python
from openai import OpenAI

client = OpenAI()

# Um único pedido com ferramentas e ficheiros integrados
response = client.responses.create(
    model="gpt-4o",
    messages=[{"role": "user", "content": "Analisa este ficheiro de vendas."}],
    tools=[{"type": "file_search"}],
    files=["vendas_mestre_capas.csv"]
)

print(response.content)
```

> [!TIP]
> **Migração**: Se ainda usas o antigo "Threads" do Assistants API, move para a Responses API. É mais barata, mais rápida e suporta as novas funcionalidades de 2026 nativamente.

---

## 🏗️ Uso na Elite Agency
- **Análise de Shopify**: Enviar o export do Mestre Capas e pedir insights de ROI num único passo.
- **Data Mining**: Usar o File Search para carregar toda a "Hook Library" da agência e pedir novos ganchos baseados no que já funcionou.
