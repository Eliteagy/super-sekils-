---
tags: [skill, manus, api, task-management, profiles, automation]
source: https://github.com/openclaw/skills/blob/main/skills/mvanhorn/manus/SKILL.md
type: skill-documentation
created: 2026-04-04
---

# Skill: Manus API Advanced (Profiles & Outputs)

> **Guia avançado para criação e gestão de tarefas autónomas via API do Manus.**

## Perfis de Agente (Modelos)
Dependendo da complexidade, o Apollo deve escolher o perfil correto:
- **`manus-1.6` (Standard):** Equilíbrio entre velocidade e inteligência (Default).
- **`manus-1.6-lite`:** Mais rápido, ideal para tarefas simples de rotina.
- **`manus-1.6-max`:** Investigação profunda e processos analíticos pesados.

## Modos de Execução
- **`agent`:** Modo totalmente autónomo (recomendado para criação de ficheiros como PPTs ou Relatórios).
- **`adaptive`:** A IA decide a melhor abordagem conforme o prompt.

## Extração Inteligente de Resultados
Em vez de depender de links de partilha (`share links`), a skill recomenda:
1. **Poll for completion:** Verificar o status (`pending` -> `running` -> `completed`).
2. **Download Direto:** Procurar por entradas do tipo `output_file` no array `output`.
3. **Persistência Local:** Descarregar o ficheiro via `fileUrl` e entregar diretamente ao utilizador.

## Exemplo de Comando (Polling Strategy)
```bash
# Verificar status e ficheiros
curl "https://api.manus.ai/v1/tasks/{task_id}" \
  -H "API_KEY: $MANUS_API_KEY"
```

## Como Aplicar no Apollo AI
- **Smart Agent Selection:** Ao receber um prompt, o Apollo analisa se deve usar o `lite` (para poupar créditos) ou o `max` (para qualidade extrema).
- **File Management:** Implementar o download automático de outputs do Manus para a pasta `downloads` do Apollo local.
