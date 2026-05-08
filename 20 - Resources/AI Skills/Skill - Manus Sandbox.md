---
tags: [skill, manus, sandbox, docker, security]
source: https://github.com/Simpleyyt/ai-manus
type: skill-documentation
created: 2026-04-04
---

# Skill: Manus Sandbox Workflows

> **Utilização de ambientes isolados para execução segura de código gerado por IA.**

## O Conceito de Sandbox
Para que um agente seja verdadeiramente autónomo, ele precisa de um sítio para "partir as coisas" sem afetar o teu PC host. O Manus usa Docker/Sandboxes para isso.

## Vantagens
- **Segurança:** Código malicioso ou erróneo fica contido no container.
- **Reproduzibilidade:** O ambiente é sempre o mesmo (Clean Slate).
- **Multi-linguagem:** Podes executar Python, Node.js ou Bash sem instalar nada localmente.

## Configuração (Draft)
```yaml
# Exemplo de configuração de Sandbox
sandbox:
  image: python:3.10-slim
  storage: 500MB
  timeout: 300s
  network: isolated
```

## Como Usar no Apollo AI
- Integrar com o **Coding View** do Apollo para que, ao clicar em "Run", o código seja executado numa sandbox estilo Manus, mostrando apenas o output final.
