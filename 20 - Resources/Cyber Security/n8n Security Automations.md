---
tags: [automation, n8n, security, workflow]
type: resource-guide
created: 2026-04-06
---

# 🤖 Automações n8n para Cyber Security

O n8n permite-te criar workflows de segurança complexos sem precisares de escrever código para cada integração. Aqui estão 3 workflows essenciais para o teu **Mega Obsidian**.

---

## 1. CVE Monitor (Alerta de Vulnerabilidades)
**Trigger**: RSS Read (ex: [CVE Feed](https://cvefeed.io/rss/all))
**Action**: Enviar para Discord/Slack/Telegram.
**Porquê?**: Estar sempre um passo à frente de novas vulnerabilidades em tecnologias que usas (ex: Shopify, React, Python).

---

## 2. GitHub Repo Stalker (Atualização de Ferramentas)
**Trigger**: Cron (ex: de 24 em 24 horas)
**Action**: Verificar se as tuas ferramentas de hacking favoritas (ex: `Nmap`, `dirsearch`, `Metasploit`) têm novos commits ou releases.
**Porquê?**: Garantir que o teu arsenal no **Hacking Lab** está sempre atualizado.

---

## 3. OSINT Scraper & Spreadsheet Sink
**Trigger**: Webhook (Enviado pelo teu telemóvel ou browser).
**Action**: 
1.  Receber um e-mail ou domínio.
2.  Consultar APIs de limpeza (ex: `HaveIBeenPwned` ou `Shodan`).
3.  Guardar o resultado numa **Google Sheet** ou **Airtable**.
**Porquê?**: Construir uma base de dados de inteligência de forma passiva.

---

## 🛠️ Como Instalar
1. Corre o n8n no teu **Hacking Lab** via Docker:
   `docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n`
2. Cria os nós conforme descrito acima.
3. Liga os teus webhooks a scripts Python para uma automação híbrida!

> [!TIP]
> Podes usar o n8n para fazer o "Log" automático das tuas vitórias no Lab diretamente para o Obsidian (via Git ou Plugin de File System).
