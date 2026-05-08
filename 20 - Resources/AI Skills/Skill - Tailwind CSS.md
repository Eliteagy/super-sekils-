---
tags: [skill, tailwind, frontend, css, v4, dx]
source: https://github.com/tailwindlabs/tailwindcss
type: skill-documentation
created: 2026-05-05
---

# Skill: Tailwind CSS (v4)

> **Expertise em Tailwind CSS v4, configuração CSS-first e padrões utilitários modernos.**

Esta skill fornece diretrizes avançadas para o uso do Tailwind CSS v4, focando na nova engine Oxide, configuração via CSS e melhores práticas de design system.

## 🚀 Novidades do v4 (Oxide Engine)

- **CSS-First Configuration**: Esquece o `tailwind.config.js`. Agora tudo é feito via diretivas `@theme` diretamente no teu ficheiro CSS.
- **Oxide Engine**: Um novo compilador escrito em Rust, 10x mais rápido.
- **Native Container Queries**: Suporte nativo para container queries sem plugins.
- **Zero-runtime CSS Variables**: Todas as tokens do tema são expostas como variáveis CSS reais.

## 🛠️ Configuração Base (Modern Workflow)

Para iniciar um projeto v4, usa a diretiva de importação simplificada:

```css
@import "tailwindcss";

@theme {
  --color-brand: oklch(0.6 0.2 250);
  --font-sans: "Inter", system-ui, sans-serif;
}
```

## 📐 Padrões de Layout e Design

### Container Queries
Usa `@container` no pai e prefixos como `@md:` ou `@lg:` nos filhos para layouts que respondem ao tamanho do componente, não da viewport.

### Cores OKLCH
Prefere o formato OKLCH para definições de cores, garantindo uma gama mais ampla e uniformidade percetual.

### Responsive Design (Mobile-First)
1. Estilos base (mobile) sem prefixo.
2. Overrides com prefixos (`sm:`, `md:`, `lg:`, etc.).
3. Exemplo: `w-full md:w-1/2 lg:w-1/3`.

## 🌑 Dark Mode (Modern Approach)

Usa a estratégia de `selector` ou `media` via CSS:

| Elemento | Light | Dark |
| :--- | :--- | :--- |
| Fundo | `bg-white` | `dark:bg-zinc-900` |
| Texto | `text-zinc-900` | `dark:text-zinc-100` |

## 🚫 Anti-Patterns a Evitar

- **Abuso de @apply**: Prefere extrair componentes em React/Vue em vez de criar classes CSS gigantes com `@apply`.
- **Valores Arbitrários Excessivos**: Usa `-[...]` apenas quando estritamente necessário; prefere estender o tema.
- **Misturar v3 com v4**: Migra totalmente para o workflow CSS-first.

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/tailwindlabs/tailwindcss)
- [Documentation v4](https://tailwindcss.com/docs/v4-beta)

---
*Gerado via Gemini CLI para a The Elite Agency.*
