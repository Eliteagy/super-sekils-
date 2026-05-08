---
tags: [agency-ops, automation, make, integromat, workflows, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🧛 Skill - Make.com: Enterprise-Grade Automation

**Make.com** (anteriormente Integromat) é a plataforma de orquestração de APIs visual para a **Elite Agency** em 2026. Ela permite ligar milhares de Apps e criar fluxos de trabalho que poupam centenas de horas de trabalho humano.

## 🚀 Por que Make?
Ao contrário do n8n (que podes rodar no teu Lab localmente), o Make é uma solução SaaS poderosa com conectores nativos para quase todas as ferramentas de marketing e vendas do mundo.

---

## 🛠️ Três Pilaries da Automação de Agência

### 1. HTTP Request (API Mastery)
Podes ligar-te a qualquer serviço que tenha uma API, enviando e recebendo dados em JSON. Isto permite-te integrar o **[[10 - Projects/Apollo AI\|Apollo AI]]** em qualquer fluxo de trabalho do Make.

### 2. Multi-Branch Routing
Usa filtros e iteradores para tratar cada lead ou cada e-mail de forma única.
- **Exemplo**: Se o e-mail vem de uma empresa de Luxo -> Envia para o **Claude 3.5**. Se é uma empresa de Retail -> Envia para o **DeepSeek V3**.

### 3. Data Store & Google Sheets Integration
Guardar o estado de cada automação para garantir que nada se perde. Fundamental para gerir o stock da **Mestre Capas** em tempo real entre o Shopify e o armazém.

---

## 🏗️ Uso na Elite Agency
- **Lead Capture Automated**: Lead chega via Ads -> Make limpa o e-mail -> Make envia para o Apollo AI para análise -> Make envia mensagem personalizada no WhatsApp.
- **Social Media Cross-Posting**: Publicar um vídeo no TikTok -> Make distribui automaticamente para Shorts, Reels e LinkedIn com legendas traduzidas via **[[Skill - ElevenLabs\|ElevenLabs]]**.
- **Customer Support 24/7**: Ligar o chat do Shopify ao **GPT-4o** via Make para resolver dúvidas de envio instantaneamente.

---

## 💻 Exemplo de Workflow de Elite
1.  **Trigger**: Webhook do Customizer da Mestre Capas.
2.  **Action**: Enviar imagem para o **[[Skill - Flux.1 Advanced\|Flux.1 LFM]]** para renderizar mockup profissional.
3.  **Action**: Notificar a equipa de produção no Slack com o link do mockup.
4.  **Action**: Enviar e-mail de "Obrigado" ao cliente com a imagem gerada por IA.

> [!TIP]
> **Dica de Custo**: Usa o Make para a orquestração de alto nível (Lógica) e o teu servidor **n8n** local para processamento pesado de dados e IA, poupando "Tasks" no plano do Make.

---

## 🔗 Relacionado
- [[n8n Security Automations]]
- [[Skill - Apollo.io & Instantly]]
- [[10 - Projects/The Elite Agency]]
