---
tags: [openai, realtime-api, voice-ai, low-latency, multimodal]
type: resource-guide
created: 2026-04-06
---

# 🤖 Skill - GPT-4o Realtime API

O **Realtime API** é a fronteira da interação humana com IA. Ele permite conversas de áudio nativas com latência de ~100ms, eliminando o atraso dos sistemas tradicionais (STT -> LLM -> TTS).

## 🚀 O que é o Realtime API?
É uma ligação persistente (Websocket ou WebRTC) onde o áudio entra e o áudio sai diretamente do modelo, permitindo que a IA reconheça interrupções, entone a voz de forma emocional e reaja em tempo real.

---

## 🛠️ Três Pilares da Experiência

### 1. Native Audio Reasoning
Diferente de modelos antigos, o GPT-4o "ouve" a entoação, o ritmo e o ruído de fundo, permitindo-lhe reagir a nuances emocionais do utilizador.

### 2. Baixíssima Latência (WebRTC)
Utiliza as mesmas tecnologias que as apps de videoconferência (Zoom/Meet), garantindo que a conversa pareça fluida e natural, sem pausas constrangedoras.

### 3. Tool Calling em Áudio
O agente pode estar a falar e, no meio da frase, decidir chamar uma ferramenta (ex: agendar uma reunião) sem parar o fluxo da conversa.

---

## 💻 Como Conectar (Protocolo 2026)

```javascript
// Exemplo WebRTC (Browser)
const rtcPeerConnection = new RTCPeerConnection();
const stream = await navigator.mediaDevices.getUserMedia({ audio: true });
stream.getTracks().forEach(track => rtcPeerConnection.addTrack(track, stream));

// URL Efêmera da OpenAI
const data = await fetch('https://api.openai.com/v1/realtime/sessions', {
  method: 'POST',
  headers: { 'Authorization': `Bearer ${OPENAI_API_KEY}` }
});

// A magia do áudio-para-áudio nativo acontece aqui
const session = await data.json();
```

---

## 🏗️ Uso na Elite Agency
- **Sales Agents**: Vendedores 24/7 que atendem chamadas via VoIP com voz humana perfeita.
- **Support Vocal**: Assistentes que ajudam clientes da Mestre Capas a personalizar produtos via voz em tempo real.
- **Red Armoury Assistant**: Um assistente de voz industrial para o teu próprio comando de operações.

> [!CAUTION]
> **Atenção aos Custos**: O Realtime API é faturado por minuto de áudio (Input/Output). Usa-o para interações críticas de alta conversão, reservando o chat para tarefas administrativas.
