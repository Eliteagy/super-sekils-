---
tags: [creative-ai, suno, udio, music-gen, audio-production, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🎨 Skill - Suno & Udio: AI Music Production

**Suno** e **Udio** são os líderes da revolução musical de IA em 2026. Eles permitem que qualquer pessoa na **Elite Agency** crie músicas completas (letra, melodia, voz e produção) em segundos, com qualidade de rádio.

## 🚀 O que faz destas IAs o "Futuro do Som"?
Diferente de geradores de "loops" antigos, o Suno e o Udio criam composições completas de até 4 minutos, com estruturas complexas (intro, verso, refrão, solo, ponte, final).

---

## 🛠️ Três Funcionalidades de Elite

### 1. Style Prompting (Versão V4/V5)
Podes descrever estilos ultra-específicos: "Industrial Neon Red, Cyberpunk, Cinematic Heavy Drums, 130 BPM, Male Dark Vocal". Ideal para o áudio do **Apollo AI**.

### 2. Lyrics Generation (Custom Mode)
Podes escrever as tuas próprias letras ou pedir ao **Claude 3.5** para as escrever, e a IA canta com a prosódia perfeita, captando rimas e ritmo de forma humana.

### 3. Audio Inpainting & Stem Separation
Em 2026, podes "pintar" partes da música que não gostas (ex: mudar o solo de guitarra) ou separar as vozes dos instrumentos (Stems) para mixagens profissionais.

---

## 🏗️ Uso na Elite Agency
- **Brand Anthem**: Criar o hino "Red Armoury" da agência para vídeos de apresentação.
- **Background Music**: Música livre de direitos de autor (Royalty-Free) para todos os anúncios da Mestre Capas no YouTube/Instagram.
- **Custom Jingle**: Criar sons de notificação musicais únicos para as apps e dashboards do Apollo AI.

---

## 💻 Como Consumir (V3.5+ API)
Ambas as plataformas oferecem APIs para geração em lote (batching).
```python
import suno_api

# Gera um hino para a Mestre Capas
song = suno_api.create(
    prompt="A corporate but emotional pop song about high-quality phone cases and self-expression, upbeat.",
    lyrics="Feeling unique with every click, my Mestre case is looking slick..."
)
print(f"[*] Música a ser gerada: {song.url}")
```

> [!TIP]
> **Dica Pro**: Usa o **Udio** se precisares de maior fidelidade acústica (Jazz, Orquestral) e o **Suno** para estilos modernos (Pop, EDM, Trap).

---

## 🔗 Relacionado
- [[Skill - ElevenLabs]]
- [[Skill - Runway Gen-3 & Luma Dream Machine]]
- [[10 - Projects/The Elite Agency]]
