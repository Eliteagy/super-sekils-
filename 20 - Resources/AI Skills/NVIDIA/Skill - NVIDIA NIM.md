---
tags: [nvidia, nim, model-serving, optimization]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - NVIDIA NIM (Inference Microservices)

NIM é o novo padrão para servir modelos de IA da NVIDIA em produção. Ele encapsula o TensorRT-LLM, servidores de inferência e quantização em microserviços prontos a usar.

## 🚀 O que é o NIM?
É um contentor (Docker/K8s) que expõe uma API compatível com OpenAI, permitindo que qualquer aplicação (como o fizesse no GPT-4o) converse com modelos como o **Llama 3.1**, **Gemma** ou **Nemotron**.

## 🛠️ Como Implementar

1.  **Acesso ao Catálogo**:
    *   `build.nvidia.com` — Catálogo de APIs e contentores.
2.  **Lançamento via Docker**:
    ```bash
    docker run -it --rm --name nim \
      -e NGC_API_KEY=$NGC_API_KEY \
      -v $HOME/.cache:/opt/nim/.cache \
      -p 8000:8000 \
      nvcr.io/nim/meta/llama3-70b-instruct
    ```
3.  **Consumo via Python**:
    ```python
    import openai

    client = openai.OpenAI(base_url="http://localhost:8000/v1", api_key="not-needed")
    response = client.chat.completions.create(
        model="llama3-70b-instruct",
        messages=[{"role": "user", "content": "Olá, Apollo!"}]
    )
    ```

## 📈 Vantagens para o Apollo AI
- **Performance**: Latência reduzida em 5x em comparação com servidores não otimizados.
- **Eficiência**: Suporta FP8 e INT8 nativamente para poupar VRAM.
- **Modularidade**: Facilmente orquestrável para multi-agentes.

> [!TIP]
> No Apollo AI, usa o NIM para o motor de "Heavy Reasoning" (70B+) enquanto manténs o Ollama para modelos leves (8B).
