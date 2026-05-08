---
tags: [skill, meta, image-gen, llama3]
source: https://github.com/Strvm/meta-ai-api
type: skill-documentation
created: 2026-04-04
---

# Skill: Meta AI Image Generation

> **Geração de imagens gratuitas usando a infraestrutura da Meta.**

## Requisitos
- Autenticação via conta de Facebook (FB Email/Password) para remover rate-limits e permitir geração de alta qualidade.

## Como Gerar Imagens
```python
from meta_ai_api import MetaAI

# Autenticação necessária para imagens
ai = MetaAI(fb_email="teu_email", fb_password="tua_password")
resp = ai.prompt(message="Gera uma imagem de um escritório futurista para uma agência de IA")

# O retorno inclui uma lista de URLs de media
for media in resp['media']:
    print(f"URL da Imagem: {media['url']}")
    print(f"Prompt usado: {media['prompt']}")
```

## Melhores Práticas
- **Diferenciação:** Útil para gerar assets rápidos de UI ou redes sociais diretamente pelo backend do Apollo.
- **Rate Limits:** Utilizadores autenticados têm limites significativamente maiores.
- **Formatos:** As imagens são geralmente enviadas como links públicos temporários (CDN da Meta).
