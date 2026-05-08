---
tags: [cursor, analysis, forensic, debugging, root-cause]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - Analyze Project (Forensic Root Cause)

Esta skill transforma o Cursor num analisador forense, capaz de identificar por que uma sessão de código falhou ou onde estão os gargalos do projeto.

## 🚀 O que faz?
Ao ser ativada, a IA realiza uma varredura profunda no histórico recente e no código para classificar:
- **Scope Deltas**: O que mudou e o que fugiu do planeamento inicial.
- **Rework Patterns**: Identificação de código que foi refeito várias vezes (sinal de confusão).
- **Hotspots**: Áreas do código com alta frequência de erros ou mudanças.
- **Root Cause Analysis**: Diagnóstico preciso de falhas em lógica ou arquitetura.

## 🛠️ Como Implementar no Cursor

```markdown
# Forensic Root Cause Analyzer

1. Analyze current session against initial goal.
2. Identify rework patterns and scope deltas.
3. List hotspots with high churn.
4. Output a summary of findings with actionable fixes.
```

## 📈 Vantagens
- **Debug Acelerado**: Encontre erros que humanos levariam horas para rastrear.
- **Limpeza de Dívida Técnica**: Identifique onde o código está a degradar-se prematuramente.
- **Contexto Histórico**: Ajuda novos desenvolvedores a entender o "porquê" de certas decisões de código.

> [!TIP]
> Use esta skill sempre que o Cursor começar a "alucinar" ou a dar voltas num problema de código. Ela força o modelo a parar e analisar a realidade dos fatos.
