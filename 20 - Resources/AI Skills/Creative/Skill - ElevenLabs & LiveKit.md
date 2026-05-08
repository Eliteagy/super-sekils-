---
tags: [elevenlabs, livekit, voice-ai, tts, stt, conversational-ai, audio]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - ElevenLabs & LiveKit (Voice Elite)

A combinação do **ElevenLabs** (Vozes de Alta Fidelidade) com o **LiveKit** (Orquestração de Áudio em Tempo Real) permite criar agentes que falam e ouvem com latência ultra-baixa em 2026.

## 🚀 O que faz?
Entrega a experiência de "Conversação Humana":
- **ElevenLabs API**: Clonagem de voz, text-to-speech emocional e dublagem instantânea.
- **ElevenLabs Conversational AI**: WebSockets para voz-para-voz direta.
- **LiveKit Agents**: SDK para ligar LLMs a canais de áudio/vídeo WebRTC.
- **Voice Design**: Criação de vozes únicas do zero (Procedural Voice).

## 🛠️ Como Implementar

```python
# ElevenLabs Conversational AI Example
import websockets
import json

async def chat_with_apollo():
    async with websockets.connect(
        "wss://api.elevenlabs.io/v1/convai/conversation?agent_id=AGENT_ID"
    ) as ws:
        # Enviar áudio capturado do microfone
        # Receber e tocar áudio gerado pelo agente
        pass
```

## 📈 Vantagens para o Apollo AI
- **Natural Interaction**: O Apollo deixa de ser um chat de texto para ser uma presença de voz real.
- **Global Reach**: Tradução e legendagem de voz dinâmica em múltiplos idiomas.
- **Emotional Nuance**: As vozes do ElevenLabs expressam entusiasmo, calma ou urgência conforme o contexto.

> [!TIP]
> Use o **LiveKit** para orquestrar sessões multi-utilizador onde o Apollo atua como moderador ou assistente de voz numa sala de reuniões virtual.
