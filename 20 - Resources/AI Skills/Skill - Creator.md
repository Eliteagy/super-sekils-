---
tags: [skill, meta, automation, documentation]
source: https://github.com/ComposioHQ/awesome-claude-skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Creator (Meta-Skill)

> **Ensina o Apollo AI a criar e empacotar as suas próprias Skills.**

## Anatomia de uma Skill
Uma skill deve ser uma pasta auto-contida:
```
skill-name/
├── SKILL.md (Instruções + Metadados YAML)
├── scripts/ (Código executável Python/Bash)
├── references/ (Documentação extra)
└── assets/ (Templates, imagens, ícones)
```

## Regras de Escrita (SKILL.md)
- **Imperative Style:** Escreve instruções no imperativo ("Faz X", "Lê Y") em vez de "Tu deves fazer".
- **Progressive Disclosure:** 
  1. Metadados (Name/Description) - detetam quando disparar.
  2. SKILL.md - guia o processo principal.
  3. Resources - carregados sob demanda para poupar tokens.

## Fluxo de Criação
1. **Entender Exemplos:** Pede ao utilizador exemplos concretos de uso.
2. **Planear Recursos:** Identifica que scripts ou referências serão necessários.
3. **Inicializar:** Cria a estrutura de pastas e o `SKILL.md`.
4. **Validar:** Garante que os metadados estão corretos para o trigger automático do LLM.
