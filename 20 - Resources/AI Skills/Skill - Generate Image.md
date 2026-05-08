---
tags: [skill, image-gen, flux, gemini, ai-art, react, optimization]
source: https://github.com/google/gemini-cli
type: skill-documentation
created: 2026-05-05
---

# Skill: Generate Image (Scientific)

> **Geração e edição de imagens de alta qualidade usando FLUX.2 Pro e Gemini 3 Pro via OpenRouter.**

Esta skill permite a criação de assets visuais, fotografias realistas e ilustrações artísticas, além de edição de imagens existentes através de comandos em linguagem natural.

## 🚀 Modelos Suportados

- **Google Gemini 3 Pro**: Alta qualidade, ideal para geração e edição complexa.
- **FLUX.2 Pro**: Rápido e estético, excelente para fotorrealismo e arte.
- **FLUX.2 Flex**: Opção económica para geração rápida.

## 🛠️ Como Usar (Scripts)

Podes usar o script `generate_image.py` para tarefas rápidas:

```bash
# Gerar uma nova imagem
python scripts/generate_image.py "Um pôr do sol digital sobre uma cidade cyberpunk"

# Editar uma imagem existente
python scripts/generate_image.py "Muda a cor do céu para roxo" --input original.jpg
```

## 📐 Integração Frontend & Performance

Sempre que integrares fluxos de geração de imagem em interfaces React, utiliza padrões de performance para evitar re-renderizações desnecessárias.

### Stable Callback Refs (useLatest)
Usa o hook `useLatest` para lidar com callbacks de geração (ex: `onGenerate`) dentro de efeitos sem disparar ciclos de renderização extras.

```typescript
function useLatest<T>(value: T) {
  const ref = useRef(value)
  useEffect(() => { ref.current = value }, [value])
  return ref
}
```

## 🎨 Casos de Uso

- **Apresentações**: Backgrounds abstratos e diagramas conceituais.
- **Marketing**: Assets visuais para redes sociais e websites.
- **Documentação**: Ilustrações de processos ou conceitos abstratos (usa `scientific-schematics` para diagramas técnicos).

## 📚 Referências Oficiais
- [OpenRouter Models](https://openrouter.ai/models)
- [Gemini Image Generation Guide](https://ai.google.dev/gemini-api/docs/image-generation)

---
*Gerado via Gemini CLI para a The Elite Agency.*
