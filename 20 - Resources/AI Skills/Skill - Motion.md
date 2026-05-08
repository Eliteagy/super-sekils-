---
tags: [skill, motion, framer-motion, frontend, animation, react, dx]
source: https://github.com/motiondivision/motion
type: skill-documentation
created: 2026-05-05
---

# Skill: Motion (Framer Motion)

> **Mestre em animações declarativas, transições de layout e orquestração visual de alto nível para React e a Web.**

A library **Motion** (anteriormente Framer Motion) é o padrão ouro para animações no ecossistema React. Em 2026, o foco mudou para performance extrema (RSC-first), integração com a View Transitions API e bundles ultra-leves.

## 🚀 Padrões Modernos (2026)

### RSC & Client Boundaries
O Motion exige interatividade no cliente. Usa sempre o padrão de separar componentes de animação com a diretiva `'use client'`.

```tsx
'use client'
import { motion } from 'motion/react'

export const FadeIn = ({ children }) => (
  <motion.div initial={{ opacity: 0 }} animate={{ opacity: 1 }}>
    {children}
  </motion.div>
)
```

### Lazy Loading & Performance
Para manter um INP (Interaction to Next Paint) baixo, usa sempre o `LazyMotion` no root da aplicação.

- **domAnimation**: Reduz o bundle em ~15kb (suporta transformações e opacidade).
- **domMax**: Suporta tudo, incluindo drag, layout e gestos.

## 🛠️ Melhores Práticas de Performance

1. **Hardware Acceleration**: Anima apenas propriedades que usam GPU: `x`, `y`, `scale`, `rotate`, `opacity`.
2. **Evita Layout Thrashing**: Nunca animes `width`, `height`, `top` ou `left`. Usa o prop `layout` para transições de tamanho fluidas.
3. **layoutId**: Usa para criar "Shared Element Transitions" (ex: um card a expandir para um modal).

## ♿ Acessibilidade (A11y)

Não ignores as preferências do utilizador. Usa o hook `useReducedMotion` para desativar movimentos bruscos:

```tsx
const shouldReduceMotion = useReducedMotion()
const x = shouldReduceMotion ? 0 : 100
```

## 🎭 Variants & Orquestração

Usa **Variants** em vez de props inline para orquestrar animações complexas em árvores de componentes:

- `staggerChildren`: Atrasa a animação dos filhos automaticamente.
- `when`: Controla se a animação ocorre `beforeChildren` ou `afterChildren`.

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/motiondivision/motion)
- [Documentation](https://motion.dev)

---
*Gerado via Gemini CLI para a The Elite Agency.*
