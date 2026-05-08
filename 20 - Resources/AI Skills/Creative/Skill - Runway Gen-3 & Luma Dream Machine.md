---
tags: [creative-ai, runway, video-gen, luma, cinematic, sora, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🎨 Skill - Runway Gen-3 & Luma Dream Machine

**Runway Gen-3 Alpha** e **Luma Dream Machine** são as ferramentas de elite para a **Geração de Vídeo de IA** em 2026. Elas permitem transformar texto ou imagens em sequências cinematográficas de alta fidelidade para a **Elite Agency**.

## 🚀 Por que Geração de Vídeo de IA?
O custo de uma produção de vídeo tradicional é proibitivo. Com estas IAs, consegues criar anúncios, apresentações e conteúdo de marca com qualidade de Hollywood num computador.

---

## 🛠️ Três Funcionalidades de Elite

### 1. Image-to-Video (I2V)
A funcionalidade mais potente: pega numa imagem gerada pelo **[[Skill - Flux.1 (Image Gen)\|Flux.1]]** e anima-a com total consistência. Isto garante que o teu branding visual se mantém perfeito no vídeo.

### 2. Motion Control (Director Mode)
Em 2026, podes controlar a câmara com precisão milimétrica: "Pan Left", "Zoom In Slow", "Dutch Angle". Tens o controlo total de um realizador de cinema no teu teclado.

### 3. Consistent Characters (V3.2+)
O Runway agora consegue manter o **mesmo rosto e roupa** em múltiplos clips diferentes, permitindo contar histórias completas com "atores digitais" consistentes.

---

## 🏗️ Uso na Elite Agency
- **Cinematic Ads**: Criar anúncios para a Mestre Capas com planos de produto impossíveis de filmar na realidade.
- **Brand Storytelling**: Criar o "Rise of the Phoenix" para a Splash Screen do **[[10 - Projects/Apollo AI\|Apollo AI]]** com realismo 8K.
- **Fashion Mockups**: Ver as capas da Mestre Capas a serem usadas por modelos em ambientes urbanos, tudo gerado digitalmente.

---

## 💻 Como Consumir (API Automation)
Muitas destas geradoras permitem orquestração técnica:
```python
import runway

# Gera o vídeo industrial "Phoenix Rising"
video = runway.generate(
    prompt="A neon red phoenix rises from clinical white smoke in a dark cyberpunk factory, cinematic slow motion, 8k",
    model="gen-3-alpha-turbo",
    duration=10
)
print(f"[*] Vídeo gerado: {video.url}")
```

> [!TIP]
> **Dica Pro**: Usa o **Luma Dream Machine** para movimentos físicos mais realistas (pesos, gravidade) e o **Runway** para estética cinematográfica e controlo de câmara superior.

---

## 🔗 Relacionado
- [[Skill - Flux.1 (Image Gen)]]
- [[Skill - Suno & Udio]]
- [[Skill - ElevenLabs]]
