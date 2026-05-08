---
tags: [ai-infrastructure, docker, kubernetes, deployment, virtualization, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🏗️ Skill - Docker & Kubernetes for AI

O **Docker** e o **Kubernetes (K8s)** são as bases para escalar a Inteligência Artificial em 2026. Eles permitem que "isoles" o teu modelo (ex: um NIM da NVIDIA ou um servidor Ollama) e o repliques conforme a carga aumenta.

## 🚀 Por que Contentores para IA?
A IA tem dependências complexas (CUDA, Drivers, bibliotecas Python específicas). O Docker garante que o que corre no teu **Hacking Lab** vai correr exatamente da mesma forma no servidor da **Elite Agency** na nuvem.

---

## 🛠️ Três Pilaries do Deployment de IA

### 1. Docker Images (NVIDIA Container Toolkit)
Para usares a GPU dentro de um contentor Docker, precisas do toolkit oficial da NVIDIA.
```bash
# Docker Compose para servir um modelo Llama 3 via Ollama com GPU
services:
  ollama:
    image: ollama/ollama
    ports:
      - "11434:11434"
    volumes:
      - ./ollama_data:/root/.ollama
    deploy:
      resources:
        reservations:
          devices:
            - driver: nvidia
              count: 1
              capabilities: [gpu]
```

### 2. Kubernetes (K8s) Orchestration
Quando precisas de rodar 10 agentes ao mesmo tempo, o K8s trata da "auto-cura" (reinicia se cair) e do "escalamento" (adiciona mais GPUs se houver muito tráfego).

### 3. vLLM & TGI (Inference Servers)
Em 2026, em vez de correres Flask/FastAPI puro, corre servidores otimizados como **vLLM** ou **TGI** dentro do Docker para obteres 3x mais tokens por segundo.

---

## 🏗️ Uso Estratégico no Apollo AI
- **Apollo Hub**: Criar um `docker-compose` que levanta o Apollo, a base de dados vetorial Qdrant e o motor de inferência Groq com um único comando.
- **Microserviços de IA**: Transformar cada "Skill" de hacking (recon, scanning) num microserviço Docker que o Apollo pode invocar à escala.

> [!IMPORTANT]
> **Docker Hub AI Images**: Usa sempre imagens oficiais (NVIDIA, PyTorch, Ollama) para garantir que tens os últimos patches de segurança e otimizações de driver.

---

## 🔗 Relacionado
- [[Skill - NVIDIA NIM]]
- [[Skill - Vector DBs (Pinecone & Qdrant)]]
- [[00 - Dashboard]]
