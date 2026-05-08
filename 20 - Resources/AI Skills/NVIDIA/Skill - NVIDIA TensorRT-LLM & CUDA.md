---
tags: [nvidia, tensorrt, cuda, optimization, quantization]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - NVIDIA TensorRT-LLM & CUDA

TensorRT-LLM é a "fórmula secreta" por trás da performance insana das GPUs NVIDIA na corrida da IA. Ele otimiza modelos de linguagem especificamente para a arquitetura de hardware (H100, A100, RTX 4090, etc.).

## 🚀 Por que usar?
Modelos como o Llama ou GPT são "pesados" para correr nativamente. O TensorRT-LLM faz:
- **Graph Optimization**: Reorganiza o fluxo de dados para evitar "gargalos".
- **Quantization (FP8/INT8)**: Reduz a precisão (e o tamanho) do modelo sem perda percetível de qualidade, permitindo rodar modelos maiores em menos VRAM.
- **In-flight Batching**: Processa múltiplos pedidos ao mesmo tempo com eficiência máxima.

## 🛠️ Três Pilares da Otimização

### 1. CUDA Cores & Tensor Cores
- **CUDA Cores**: Unidades genéricas de processamento paralelo.
- **Tensor Cores**: Aceleradores específicos para operações matemáticas de IA (multiplicação de matrizes).

### 2. Quantização FP8 (O Padrão 2026)
A NVIDIA introduziu o FP8 para maximizar a velocidade sem degradar a inteligência. Permite que uma RTX 4090 rode modelos que antes precisariam de uma A100.

### 3. Integração com Apollo AI
Podes usar o `trt-llm` para:
1.  **Compilar** os teus modelos customizados (ex: um Llama 3.1 com "finetuning" da Elite Agency).
2.  **Servir** via NIM para garantir 0% de latência.

---

## 📈 Benchmarks Estimados (Tokens/s)
| Hardware | PyTorch (Nativo) | TensorRT-LLM |
|----------|------------------|--------------|
| **RTX 3060** | 15 tok/s | 35 tok/s |
| **RTX 4090** | 80 tok/s | 160 tok/s |
| **H100** | 250 tok/s | 800+ tok/s |

> [!CAUTION]
> **Atenção**: Compilar um modelo com TensorRT consome muito tempo e CPU/GPU. Faz isto apenas quando o modelo estiver "finalizado" e pronto para produção na agência.
