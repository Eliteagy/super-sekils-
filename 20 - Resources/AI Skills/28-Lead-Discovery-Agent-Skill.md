# 🤖 Skill 28: Agente de Descoberta de Leads (Lead Discovery)

**Categoria:** #AgencyOps #LeadGen #Automacao #Python #NextJS
**Status:** 🟢 Ativo (Integrado na Elite Agency App)

---

## 📍 1. Propósito do Agente

O **Lead Discovery Agent** é uma unidade de inteligência focada em minerar a web (Google Maps, Search, LinkedIn) para encontrar decisores em nichos de alto ticket. Ele substitui a prospecção manual, entregando leads já qualificados e com "Hooks" de abordagem prontos.

---

## ⚙️ 2. Arquitetura Técnica

A habilidade está dividida em dois ambientes sincronizados:

1.  **Motor Móvel (Python):** Script CLI para extração rápida de massa via terminal.
2.  **Motor Integrado (Next.js/TS):** Rota de API (`/api/prospecting`) que processa buscas reais via IA (OpenRouter + Serper).

### Fluxo de Inteligência:
1.  **Input:** Nicho + Localização.
2.  **Search:** O Agente varre o Google Search/Maps em tempo real.
3.  **Filtragem:** IA (Claude/GPT) analisa os resultados, extrai Site/Telefone e valida o "fit" do lead.
4.  **Output:** Tabela MD no Obsidian ou Card no Kanban do CRM.

---

## 🛠️ 3. Como Executar

### Via CLI (Local):
```bash
python Lead-Discovery-Agent.py
```

### Via Dashboard:
Basta aceder ao **Clients Hub** na Elite Agency App e clicar no botão **"Prospecção IA"**.

---

## 💎 4. Insights de Elite (Mining Strategy)

> [!TIP]
> **O Gancho de 1%:** O segredo não é apenas o número, mas o **Hook Estratégico**. O agente está configurado para analisar o site do lead e sugerir uma melhoria imediate (ex: vídeo 3D Spline, automação de reels), aumentando a taxa de agendamento em 40%.

---

## 🔗 Links de Operação
- **Vault Operacional:** [[Elite Agency OB]]
- **App Dashboard:** [Elite CRM (Localhost)](http://localhost:3000/crm)
- **CRM de Luxo:** [[02-Prospeccao-Cascais-Luxo]] (No Vault Elite Agency)

---
[[00 - Dashboard]] | [[00 - Master AI Index]]
