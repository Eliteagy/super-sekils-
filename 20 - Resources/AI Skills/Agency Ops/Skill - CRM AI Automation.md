---
tags: [agency-ops, sales, crm, automation, hubspot, salesforce, 2026-standard]
type: resource-guide
created: 2026-04-06
---

# 🧛 Skill - CRM AI Automation: Smart Sales Pipeline

Em 2026, um **CRM** (Customer Relationship Management) não é apenas uma lista de contactos—é o centro de inteligência da **Elite Agency**. A automação de CRM com IA garante que nenhuma lead "morre no funil".

## 🚀 Por que CRM AI-Native?
A maioria das agências falha no seguimento (Follow-up). Uma automação de CRM bem montada gere as tuas leads, atualiza o status dos negócios e agenda reuniões por ti.

---

## 🛠️ Três Pilaries do CRM de Elite

### 1. Auto-Data Enrichment
Quando uma lead entra (ex: via Facebook Ads ou Landing Page), a IA do **[[Skill - Apollo.io & Instantly\|Apollo.io]]** ou do **[[Skill - OpenAI Agents SDK\|OpenAI SDK]]** preenche automaticamente:
- Tamanho da Empresa.
- Receita Anual Estimada.
- Links de Redes Sociais.
- Ponto de Dor (Pain Point) mais provável.

### 2. Smart Follow-up Routing
Se uma lead não responde a 3 e-mails, o CRM aciona o **[[Skill - n8n Security Automations\|n8n]]** para enviar uma mensagem no WhatsApp ou fazer um "retargeting" de anúncios personalizado apenas para essa pessoa.

### 3. Revenue Forecasting (V4.2+)
Usando os dados históricos da Elite Agency, o CRM prevê quanto vais facturar nos próximos 90 dias com base na velocidade atual do teu pipeline de vendas.

---

## 🏗️ Como Orquestrar (Full CRM Flow)
1.  **Trigger**: Novo Lead no Hubspot ou Salesforce.
2.  **Action**: Enviar para o **[[Skill - Claude 3.5 Sonnet & Computer Use\|Claude 3.5]]** para ler o Twitter/Linkedin da lead.
3.  **Action**: Gerar uma proposta em PDF enviada por e-mail com **[[Skill - Make.com\|Make.com]]**.
4.  **Action**: Notificar-te no Slack apenas se o "Deal Value" for superior a 5.000€.

---

## 💻 Exemplo de Webhook Integrado
```python
# Script simples para ligar o teu CRM ao Apollo AI
import requests

def send_to_apollo(lead_id, lead_data):
    url = "https://apollo-ai-platform.com/api/enrich"
    headers = {"Authorization": "Bearer AGENT_KEY"}
    response = requests.post(url, json={"id": lead_id, "data": lead_data})
    
    if response.status_code == 200:
        print("[+] Lead enriquecida com sucesso pelo Apollo AI.")
```

> [!TIP]
> **Dica Pro**: Usa ferramentas como o **Pipedrive** ou **Hubspot** como base e liga-as ao **Make.com** para toda a lógica pesada de IA, poupando os custos proibitivos das IA's nativas dos CRMs industriais.

---

## 🔗 Relacionado
- [[Skill - Make.com]]
- [[Skill - OpenAI Agents SDK]]
- [[10 - Projects/The Elite Agency]]
