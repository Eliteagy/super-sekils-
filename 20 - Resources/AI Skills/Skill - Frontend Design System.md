---
tags: [skill, anthropic, frontend, react, dx]
source: https://github.com/anthropics/skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Frontend Design (AI Patterns)

> **Regras de ouro para a IA gerar código frontend de alta performance.**

## Component Guidelines
- **Modularity:** Um ficheiro, um componente (sempre que possível).
- **Type Safety:** Uso obrigatório de TypeScript Interfaces para todos os Props.
- **Atomic CSS:** Preferência por Tailwind ou CSS Modules para evitar conflitos de estilo global.
- **Stable Callbacks (Advanced):** Usar o hook `useLatest` para aceder a valores atualizados em callbacks dentro de `useEffect` sem disparar re-runs desnecessários.

```typescript
function useLatest<T>(value: T) {
  const ref = useRef(value)
  useEffect(() => { ref.current = value }, [value])
  return ref
}
```

## DX (Developer Experience)
- Inserir comentários explicativos em secções complexas logicamente.
- Usar nomes de funções e variáveis auto-explicativos (Semântica).
- Implementar Error Boundaries em componentes de UI gerados.

## Estratégia Apollo AI
- O Apollo AI deve seguir estes padrões sempre que o utilizador pedir para "Codar um componente". Isto garante que o código é limpo e fácil de manter.
