---
tags: [cursor, stripe, supabase, postgres, payments, backend, best-practices]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - Stripe & Supabase Best Practices

Esta skill consolida os padrões oficiais e da comunidade para implementar pagamentos robustos (Stripe) e bases de dados performantes (Supabase/PostgreSQL).

## 🚀 O que faz?
Garante que a implementação de backend e pagamentos segue os padrões de segurança e performance:
- **Webhook Reliability**: Padrões para processar eventos do Stripe sem perda de dados.
- **RLS (Row Level Security)**: Configuração correta de políticas de segurança no Supabase.
- **Postgres Optimization**: Sugestões de índices, queries e migrações eficientes.
- **Subscription Lifecycle**: Gestão de estados de subscrição (trial, active, past_due).

## 🛠️ Como Implementar no Cursor

```markdown
# Stripe & Supabase Patterns

1. Implement Stripe Webhooks with signature verification.
2. Use Supabase RLS for all table interactions.
3. Apply standard PostgreSQL indexing for performance.
4. Follow subscription lifecycle handling as per official SDK.
```

## 📈 Vantagens
- **Segurança de Pagamentos**: Reduz o risco de falhas em transações financeiras.
- **Escalabilidade de Dados**: Otimiza a base de dados desde o dia 1.
- **Conformidade**: Segue as normas de privacidade e segurança do Supabase.

> [!TIP]
> Use esta skill junto com a **Architect Review** para validar se a sua infraestrutura de pagamentos é resiliente a erros de rede.
