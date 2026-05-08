---
tags: [skill, canvas-confetti, frontend, animation, canvas, dx]
source: https://github.com/catdad/canvas-confetti
type: skill-documentation
created: 2026-05-05
---

# Skill: Canvas Confetti

> **Mestre em explosões de confetes de alta performance e celebrações visuais leves via HTML5 Canvas.**

A library `canvas-confetti` é a escolha ideal para adicionar efeitos de celebração sem comprometer a performance, utilizando diretamente a API de Canvas do browser.

## 🚀 Uso Rápido

O uso mais básico dispara um canhão do centro do ecrã:

```javascript
import confetti from 'canvas-confetti';

confetti();
```

## 🛠️ Configurações Comuns

| Propriedade | Descrição | Exemplo |
| :--- | :--- | :--- |
| `particleCount` | Número de pedaços de confete. | `150` |
| `spread` | Ângulo de dispersão (em graus). | `70` |
| `origin` | Ponto de origem (x, y de 0 a 1). | `{ x: 0.5, y: 0.6 }` |
| `colors` | Array de cores HEX. | `['#ff0000', '#00ff00']` |
| `scalar` | Escala do confete (tamanho). | `1.2` |
| `shapes` | Formas (`square`, `circle`, `star`). | `['star']` |

## 🎭 Efeitos Avançados

### Side Cannons (School Pride)
Dispara dois canhões dos cantos inferiores:

```javascript
confetti({
  particleCount: 100,
  spread: 70,
  origin: { y: 0.6, x: 0 },
  angle: 60
});
confetti({
  particleCount: 100,
  spread: 70,
  origin: { y: 0.6, x: 1 },
  angle: 120
});
```

### Formas Customizadas (Emojis)
```javascript
const unicorn = confetti.shapeFromText({ text: '🦄' });
confetti({ shapes: [unicorn], scalar: 2 });
```

## 📐 Melhores Práticas

- **Reduced Motion**: Respeita sempre a preferência do utilizador usando `disableForReducedMotion: true`.
- **Z-Index**: Define `zIndex` se o confete precisar de aparecer por cima de modais.
- **Cleanup**: A função retorna uma `Promise` que resolve quando a animação termina, útil para encadear ações.
- **Custom Canvas**: Se precisares de confetes num elemento específico (não no fullscreen), usa `confetti.create(canvasElement)`.

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/catdad/canvas-confetti)
- [Demo Page](https://www.kirilv.com/canvas-confetti/)

---
*Gerado via Gemini CLI para a The Elite Agency.*
