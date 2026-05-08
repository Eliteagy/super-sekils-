---
tags: [skill, r3f, react-three-fiber, threejs, 3d, webgpu, dx]
source: https://github.com/pmndrs/react-three-fiber
type: skill-documentation
created: 2026-05-05
---

# Skill: React Three Fiber (R3F)

> **Mestre em computação gráfica declarativa, cenas 3D de alta performance e ecossistema pmndrs.**

R3F não é apenas um wrapper do Three.js; é um renderizador React que permite construir cenas 3D complexas com a mesma facilidade que constróis UIs. Em 2026, o foco está na transição para **WebGPU**, uso massivo de **KTX2** e eliminação do "React Tax" em loops de alta frequência.

## 🚀 Padrões de Performance (2026)

### WebGPU & Modern Rendering
Com a v9+, o R3F suporta WebGPU nativamente. Ativa-o para ganhos massivos em simulações complexas:

```tsx
<Canvas gl={(canvas) => new THREE.WebGPURenderer({ canvas, antialias: true })}>
  <App />
</Canvas>
```

### O "React Tax" (useFrame)
Nunca uses `setState` dentro do loop `useFrame`. A reconciliação do React é demasiado lenta para 60/120 FPS.

- **Bad**: `useFrame(() => setPosition(p => p + 0.1))`
- **Good**: Usa **Refs** e **Zustand/Valtio** para updates transitórios.

```tsx
const meshRef = useRef()
useFrame((state, delta) => {
  meshRef.current.rotation.x += delta
})
```

## 🛠️ Pipeline de Assets

1. **KTX2 (Basis Universal)**: Formato obrigatório para texturas. Mantém-se comprimido na VRAM, poupando até 80% de memória GPU.
2. **Meshopt**: Preferível ao Draco para compressão de geometria devido à velocidade de descompressão.
3. **Instanced Rendering**: Usa `<Instances />` do `@react-three/drei` para desenhar milhares de objetos repetidos numa única draw call.

## 📦 Ecossistema Essencial

- **Drei**: A "standard library" do R3F. Usa `<OrbitControls />`, `<PerformanceMonitor />` e `<Environment />`.
- **Leva**: Painel de debug GUI para controlar variáveis da cena em tempo real.
- **Rapier**: Engine de física 3D performante em Rust (WASM).
- **Postprocessing**: Usa `EffectComposer` com efeitos otimizados como **N8AO** (Ambient Occlusion ultra-rápido).

## 📐 Melhores Práticas

- **Zero Allocations**: Nunca cries novos objetos (`new THREE.Vector3()`) dentro do `useFrame`. Pré-aloca fora do loop.
- **On-Demand Rendering**: Se a cena for estática (ex: visualizador de produto), usa `frameloop="demand"` para poupar bateria.
- **DPR Scaling**: Usa `<PerformanceMonitor />` para reduzir a resolução (`dpr`) dinamicamente em dispositivos mais lentos.

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/pmndrs/react-three-fiber)
- [Documentation](https://docs.pmnd.rs/react-three-fiber)

---
*Gerado via Gemini CLI para a The Elite Agency.*
