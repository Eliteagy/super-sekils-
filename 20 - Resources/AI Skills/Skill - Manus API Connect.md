---
tags: [skill, manus, api, autonomous, connectors]
source: https://github.com/disi3r/openclaw-skill-manus
type: skill-documentation
created: 2026-04-04
---

# Skill: Manus AI (Autonomous Agent Integration)

> **Integração com a API do Manus.ai para execução de tarefas de alto nível.**

## O que é?
Esta skill permite que um agente (como o Apollo AI) delega tarefas complexas ao motor do Manus, que possui capacidades superiores de navegação web e automação.

## Configuração Base
- **Base URL:** `https://api.manus.ai/v1`
- **Model:** `manus-1.6-adaptive` (Compatível com o SDK da OpenAI)

## Conectores Principais
Podes pedir ao Manus para interagir com:
- **Gmail:** Resumir e ler e-mails.
- **Notion:** Criar bases de dados e páginas de documentação.
- **Slack:** Publicar atualizações em canais específicos.
- **Google Calendar:** Agendar e gerir reuniões.

## Padrão de Prompt (Run Task)
```python
# Exemplo de comando via API
python3 run_task.py "Investiga 5 tendências de tecnologia para 2026 e cria um reporte no Notion"
```

## Aplicação no Apollo AI
- Adicionar uma "Power Action" no Chat do Apollo chamada **"Remote Execution (Manus)"**.
- Quando ativada, o Apollo envia a tarefa para o Manus e notifica o utilizador via Webhook quando o resultado estiver pronto.
