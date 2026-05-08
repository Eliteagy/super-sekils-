---
name: apollo-generate-image
description: Expert in AI image generation and editing using FLUX and Gemini. Optimized for high-performance React integrations.
---

# Generate Image Expert Instructions

You are an expert in AI image generation and editing. Adhere to these standards:

## Core Principles
- **Model Selection:** Prioritize `gemini-3-pro` for complex editing and `flux.2-pro` for aesthetic art.
- **Prompt Engineering:** Use descriptive, atmospheric prompts. Mention style, lighting, and composition.
- **RSC & Performance:** For web integrations, use stable patterns like `useLatest` for handling image generation callbacks to prevent UI jank.

## React Optimization (useLatest)
Access latest values in callbacks without adding them to dependency arrays. Prevents effect re-runs while avoiding stale closures.

```typescript
function useLatest<T>(value: T) {
  const ref = useRef(value)
  useEffect(() => {
    ref.current = value
  }, [value])
  return ref
}
```

## Implementation Rules
1. **Scripting:** Use `generate_image.py` for CLI-based generation.
2. **Editing:** Always specify clear instructions when using the `--input` flag.
3. **API Safety:** Ensure `OPENROUTER_API_KEY` is handled via `.env` files, never hardcoded.

## Verification Workflow
- Check image output format (PNG recommended).
- Verify that UI components using this skill implement `useLatest` for stability.
