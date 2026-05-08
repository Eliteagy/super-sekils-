# CRM de Outreach — Template Spreadsheet

**Categoria:** #crm #organização #outreach
**Nível:** Prático
**Fonte:** Mentoria 2026-03-29

---

## 📊 ESTRUTURA DA SPREADSHEET

### Aba 1: Pipeline Principal

| Coluna | Descrição | Exemplo |
|--------|-----------|---------|
| A | Nome da Lead | João Silva |
| B | Empresa | Stand Silva |
| C | Cargo | Gerente |
| D | Email | joao@standsilva.pt |
| E | Telefone | +351 912 345 678 |
| F | LinkedIn | linkedin.com/in/joao |
| G | Nicho | Stand Automóvel |
| H | LTV Estimado | €20.000 |
| I | Prioridade (1-10) | 8 |
| J | Status | Em progresso |
| K | Data Entrada | 01/04/2026 |
| L | Último Contato | 05/04/2026 |
| M | Próxima Ação | Warm Call |
| N | Data Próxima Ação | 07/04/2026 |
| O | Notas | Já abriu 2 e-mails |

---

### Aba 2: Tracking de Toques (21 Dias)

| Lead | Dia 1 | Dia 2 | Dia 3 | Dia 4 | Dia 5 | Dia 7 | Dia 10 | Dia 14 | Dia 18 | Dia 21 | Status |
|------|-------|-------|-------|-------|-------|-------|--------|--------|--------|--------|--------|
| João Silva | ✅ Email | ✅ LI | ✅ Email | ✅ IG | ✅ Email | ⏳ | | | | | Em progresso |
| Maria Santos | ✅ Email | ✅ LI | ✅ Email | ✅ IG | ✅ Email | ✅ LI | ✅ Email | ⏳ | | | Em progresso |
| Pedro Costa | ✅ Email | ✅ LI | ✅ Email | ✅ IG | ✅ Email | ✅ LI | ✅ Email | ✅ IG | ✅ Email | ✅ Call | Reunião agendada |

**Legenda:**
- ✅ = Feito (com data)
- ⏳ = Pendente
- ❌ = Não feito / Skip
- 📞 = Warm call feita

---

### Aba 3: Reuniões Agendadas

| Lead | Data/Hora | Link | Confirmado? | Lembrete 2d | WhatsApp 1d | 2h Antes | 15min Antes | Show? | Resultado |
|------|-----------|------|-------------|-------------|-------------|----------|-------------|-------|-----------|
| João Silva | 10/04 14h | Zoom | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Fechado |
| Maria Santos | 11/04 10h | Meet | ✅ | ✅ | ⏳ | | | | |

---

### Aba 4: Clientes Fechados

| Cliente | Data Fecho | Valor/mês | LTV | Serviço | Start Date | Status | Notas |
|---------|------------|-----------|-----|---------|------------|--------|-------|
| Stand Silva | 10/04/2026 | €600 | €20.000 | Conteúdo + Gestão | 15/04/2026 | Ativo | Pagamento dia 15 |

---

### Aba 5: Métricas

| Métrica | Esta Semana | Mês Atual | Meta |
|---------|-------------|-----------|------|
| Novas Leads | 15 | 45 | 50 |
| Toques Feitos | 85 | 280 | 400 |
| Respostas | 8 | 22 | 30 |
| Reuniões Agendadas | 3 | 12 | 15 |
| No-Shows | 0 | 2 | < 2 |
| Fechamentos | 1 | 4 | 5 |
| Revenue | €600 | €2.400 | €3.000 |

---

## 📝 FORMULAS ÚTEIS

### Contar Toques por Lead:
```
=COUNTIF(B2:K2, "✅")
```

### Dias Desde Último Contato:
```
=TODAY() - L2
```

### Alerta para Leads Paradas (> 7 dias sem contato):
```
=IF(TODAY() - L2 > 7, "⚠️ Follow-up", "OK")
```

### Taxa de Conversão (Reuniões / Leads):
```
=COUNTA(Aba3!A:A) / COUNTA(Aba1!A:A)
```

### Taxa de Show-up:
```
=COUNTIF(Aba3!I:I, "✅") / COUNTA(Aba3!I:I)
```

---

## 🎯 WORKFLOW DIÁRIO

### Manhã (30 min):

1. **Verificar reuniões do dia** (Aba 3)
   - [ ] Enviar WhatsApp de confirmação (1 dia antes)
   - [ ] Enviar mensagem 2h antes
   - [ ] Enviar mensagem 15min antes

2. **Verificar próximas ações** (Aba 1, coluna M-N)
   - [ ] Fazer warm calls agendadas para hoje
   - [ ] Enviar e-mails pendentes

3. **Atualizar tracking** (Aba 2)
   - [ ] Marcar toques feitos com ✅
   - [ ] Agendar próximos toques com ⏳

---

### Tarde (30 min):

1. **Follow-up de reuniões**
   - [ ] Enviar e-mail de agradecimento (15min pós-call)
   - [ ] Adicionar notas na lead
   - [ ] Atualizar status

2. **Novas leads**
   - [ ] Pesquisar 5-10 novas empresas
   - [ ] Preencher Aba 1 com dados
   - [ ] Classificar prioridade (1-10)

3. **Métricas**
   - [ ] Atualizar Aba 5 com números do dia

---

### Fim de Semana (1 hora):

1. **Revisão semanal**
   - [ ] Analisar métricas da semana
   - [ ] Identificar leads paradas (> 7 dias)
   - [ ] Planear ações da próxima semana

2. **Limpeza de pipeline**
   - [ ] Remover leads não qualificadas
   - [ ] Atualizar status de todas as leads
   - [ ] Arquivar fechados/perdidos

---

## 📋 TEMPLATE DE PREENCHIMENTO

### Nova Lead (Aba 1):

```
Nome: [Nome completo]
Empresa: [Nome da empresa]
Cargo: [Cargo do decisor]
Email: [Email profissional]
Telefone: [Telefone direto se possível]
LinkedIn: [URL do perfil]
Nicho: [Stand/Imobiliária/Clínica/etc.]
LTV Estimado: [€10.000-€50.000]
Prioridade: [1-10, baseado em LTV + fit]
Status: [Nova lead]
Data Entrada: [Data de hoje]
Último Contato: [Data de hoje]
Próxima Ação: [E-mail inicial]
Data Próxima Ação: [Data de hoje]
Notas: [Qualquer insight da pesquisa]
```

---

### Após E-mail Inicial (Aba 2):

```
Dia 1: ✅ 01/04/2026
Status: Em progresso
Próximo toque: Dia 2 - LinkedIn invite
Data: 02/04/2026
```

---

### Após Reunião (Aba 3 + Aba 1):

```
Aba 3 - Preencher:
Confirmado? ✅
Lembrete 2d? ✅
WhatsApp 1d? ✅
2h Antes? ✅
15min Antes? ✅
Show? ✅
Resultado: [Fechado / Pendente / Perdido]

Aba 1 - Atualizar:
Status: [Fechado / Em negociação / Perdido]
Último Contato: [Data de hoje]
Próxima Ação: [Enviar proposta / Follow-up / etc.]
Notas: [Resumo da reunião + próximos passos]
```

---

## 🔗 CONEXÕES COM OUTRAS FERRAMENTAS

### Google Calendar Integration:
- Criar evento automático quando lead agenda
- Adicionar link do Zoom/Meet
- Set reminder 1h antes

### CRM Avançado (Opcional):
- HubSpot (grátis até 1M contacts)
- Pipedrive (€12-24/mês)
- Airtable (grátis até 1.200 records)

### Automação de E-mail:
- Lemlist (€59/mês)
- Instantly (€37/mês)
- Mailshake (€29/mês)

### LinkedIn Automation:
- Waalaxy (€0-80/mês)
- Dripify (€39-69/mês)
- LinkedHelper (€15/mês)

---

## ⚠️ ERROS A EVITAR

| Erro | Consequência | Solução |
|------|--------------|---------|
| Não atualizar daily | Perdes tracking | 30 min manhã + 30 min tarde |
| Muitas leads sem ação | Pipeline inchado | Máximo 50 leads ativas |
| Não classificar prioridade | Perdes tempo com leads baixas | Score 1-10 obrigatório |
| Esquecer follow-up | Perdes oportunidades | Usar fórmula de alerta (> 7 dias) |
| Não medir métricas | Não sabes o que funciona | Atualizar Aba 5 semanalmente |

---

## 📊 EXEMPLO DE PREENCHIMENTO

### Lead: João Silva (Stand Silva)

**Aba 1:**
```
Nome: João Silva
Empresa: Stand Silva Lda
Cargo: Gerente de Vendas
Email: joao@standsilva.pt
Telefone: +351 912 345 678
LinkedIn: linkedin.com/in/joaosilva
Nicho: Stand Automóvel
LTV Estimado: €20.000
Prioridade: 8
Status: Em negociação
Data Entrada: 01/04/2026
Último Contato: 10/04/2026
Próxima Ação: Enviar proposta
Data Próxima Ação: 11/04/2026
Notas: Reunião correu bem. Quer pensar 2 dias.
```

**Aba 2:**
```
Dia 1: ✅ 01/04 - Email inicial
Dia 2: ✅ 02/04 - LinkedIn invite
Dia 3: ✅ 03/04 - Email FU1
Dia 4: ✅ 04/04 - IG DM
Dia 5: ✅ 05/04 - Email FU2
Dia 7: ✅ 07/04 - LinkedIn FU
Dia 10: ✅ 10/04 - Email FU3 → ACEITOU REUNIÃO
Dia 14: -
Dia 18: -
Dia 21: -
Status: Reunião agendada 10/04 14h
```

**Aba 3:**
```
Lead: João Silva
Data/Hora: 10/04/2026 14:00
Link: zoom.us/j/123456789
Confirmado? ✅
Lembrete 2d? ✅ (enviado 08/04)
WhatsApp 1d? ✅ (enviado 09/04 10h)
2h Antes? ✅ (enviado 10/04 12h)
15min Antes? ✅ (enviado 10/04 13:45)
Show? ✅
Resultado: Fechado €600/mês
```

---

## 🔗 Conexões

- **Relacionado a:** [[10-Warm-Call-Outreach]], [[12-Templates-Outreach-Completo]]
- **Aplica-se a:** [[Projeto-Fechamento-40]]

---

*Nota: Cria esta spreadsheet no Google Sheets ou Excel. Mantém atualizada daily.*
