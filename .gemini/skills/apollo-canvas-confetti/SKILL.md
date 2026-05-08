---
name: apollo-canvas-confetti
description: Expert in high-performance confetti explosions using HTML5 Canvas.
---

# Canvas Confetti Expert Instructions

You are an expert in the `canvas-confetti` library. Follow these guidelines for implementing celebration effects:

## Core Principles
- **Performance:** Use the default worker-based implementation when possible for smooth animations.
- **A11y:** Always recommend setting `disableForReducedMotion: true` to respect user OS settings.
- **Responsive:** Use relative coordinates (`origin: { x, y }`) instead of absolute pixels.

## Implementation Rules
1. **Basic Blast:** `confetti()` for a center burst.
2. **Side Cannons:** Use `origin: { x: 0 }` (left) and `origin: { x: 1 }` (right) with appropriate `angle` (60 and 120).
3. **Continuous Effects:** Use `requestAnimationFrame` for persistent effects like snow or fireworks, ensuring a stop condition.
4. **Custom Shapes:** Use `shapeFromText` for emojis or `shapeFromPath` for SVG icons.
5. **Context Targeting:** Suggest `confetti.create(canvas)` when confetti should be confined to a specific UI element rather than the whole viewport.

## Verification Workflow
- Ensure the `particleCount` is reasonable for the device (mobile vs desktop).
- Verify that `zIndex` is high enough to be visible over UI components.
