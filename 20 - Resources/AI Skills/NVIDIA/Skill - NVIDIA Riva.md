---
tags: [nvidia, riva, speech-ai, asr, tts, nlp]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - NVIDIA Riva

NVIDIA Riva é um SDK de IA conversacional multimodais e totalmente acelerado por GPU, projetado para construir aplicações de fala (Speech AI) de baixa latência em tempo real.

## 🚀 O que é o Riva?
É um conjunto de serviços de microserviços (NIMs) que oferecem:
- **ASR (Automatic Speech Recognition)**: Transcrição de fala para texto em múltiplos idiomas.
- **TTS (Text-to-Speech)**: Geração de voz natural a partir de texto.
- **NMT (Neural Machine Translation)**: Tradução em tempo real.

## 🛠️ Como Implementar

1.  **Implantação via NIM**:
    ```bash
    # Exemplo de pull do container Riva ASR
    docker run --gpus all -it --rm -p 50051:50051 \
      nvcr.io/nvidia/riva/riva-speech:2.15.0
    ```

2.  **Exemplo de uso em Python**:
    ```python
    import riva.client

    auth = riva.client.Auth(uri='localhost:50051')
    riva_asr = riva.client.ASRService(auth)

    # Configuração do reconhecimento
    config = riva.client.RecognitionConfig(
        encoding=riva.client.AudioEncoding.LINEAR_PCM,
        sample_rate_hertz=16000,
        language_code="pt-BR",
        max_alternatives=1,
        enable_automatic_punctuation=True,
    )
    ```

## 📈 Vantagens para o Apollo AI
- **Latência de "Ouvido Humano"**: Respostas em menos de 150ms, ideal para interação natural.
- **Multilingue**: Suporte nativo para Português, permitindo que o Apollo seja global.
- **Personalização**: Possibilidade de ajustar modelos (Fine-tuning) com o **NVIDIA NeMo** para vocabulário específico do projeto.

> [!TIP]
> Use o Riva em conjunto com o **NVIDIA NIM** (LLM) para criar um loop completo de voz: "Escutar -> Pensar -> Falar" sem sair da GPU.
