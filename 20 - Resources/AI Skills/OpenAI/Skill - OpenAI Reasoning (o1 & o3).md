---
tags: [openai, reasoning, o1, o3, chain-of-thought, complex-logic]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - OpenAI Reasoning (o1 & o3)

A série `o` da OpenAI (o1, o1-mini, o3) representa o salto para o raciocínio profundo (RL-based Chain of Thought), onde o modelo "pensa" antes de responder em 2026.

## 🚀 O que faz?
Ao contrário dos modelos chat padrão, estes modelos são desenhados para:
- **Chain of Thought Escondido**: Resolve problemas através de passos lógicos internos antes de mostrar o output final.
- **Complex Coding**: Capaz de planear arquiteturas de microserviços inteiras sem erros de lógica comuns.
- **STEM Mastery**: Excelente em matemática avançada, física e biologia (nível de doutoramento).
- **Tool Orchestration**: Capaz de decidir sequências complexas de chamadas de ferramentas sem se perder.

## 🛠️ Como Implementar no Cursor

```markdown
# Reasoning Rules

1. When task involves deep architectural changes, switch to 'o1' or 'o3'.
2. Ask the model to "think through the edge cases" explicitly.
3. Use the hidden reasoning tokens to solve persistent logical bugs.
4. If the codebase is giant, use o1-preview for initial architectural scan.
```

## 📈 Vantagens para o Apollo AI
- **Cérebro Central**: Use o o3 como o "Super-Agente" que toma as grandes decisões de design do Apollo.
- **Verificação de Regras**: Peça ao o1 para auditar as regras do projeto contra bugs de segurança.
- **Raciocínio Geométrico**: Ideal para calcular os vetores e a lógica da "Kinetic Vision".

> [!IMPORTANT]
> Estes modelos têm maior latência e custo por token. Use-os para **pensar**, e modelos mais leves (como GPT-4o-mini ou NIMs locais) para **executar**.
