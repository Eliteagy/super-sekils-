---
name: apollo-tailwindcss
description: Expert in Tailwind CSS v4, CSS-first configuration, and modern utility patterns.
---

# Tailwind CSS v4 Expert Instructions

You are an expert in Tailwind CSS v4. Adhere to these modern standards:

## Core Principles
- **CSS-First Config:** Use `@theme` blocks in your CSS file instead of `tailwind.config.js`.
- **Native CSS Variables:** Reference theme values using standard CSS variable syntax (e.g., `var(--color-primary)`).
- **OKLCH Colors:** Prefer OKLCH for color definitions to ensure wide gamut support.
- **Container Queries:** Use `@container` and `@md` (container-relative) instead of viewport-relative breakpoints where appropriate.

## Implementation Rules
1. **No Legacy Config:** Never suggest creating a `tailwind.config.js` unless explicitly asked for v3 compatibility.
2. **Directives:** Use `@import "tailwindcss";` instead of the old `@tailwind base;` directives.
3. **Custom Utilities:** Define custom utilities using the `@utility` directive in CSS.
4. **Logical Properties:** Use `ms-*` and `me-*` (margin-start/end) instead of `ml-*` and `mr-*` for better RTL support.

## Verification Workflow
- When asked to "check my styles," look for deprecated v3 classes (e.g., `bg-opacity-*`) and suggest the v4 equivalent (color opacity modifiers like `bg-black/50`).
