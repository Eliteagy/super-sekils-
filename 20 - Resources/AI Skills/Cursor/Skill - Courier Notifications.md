---
tags: [cursor, courier, notifications, email, sms, messenger, automation]
type: resource-guide
created: 2026-04-06
---

# 🟢 Skill - Courier (Multi-channel Notifications)

Courier simplifica drasticamente a forma como o seu agente AI envia notificações em múltiplos canais (Email, SMS, Slack, etc).

## 🚀 O que faz?
Centraliza e abstrai a lógica de notificações, permitindo que o Cursor se foque no conteúdo:
- **Unified Interface**: Um único comando para vários canais.
- **Provider Aggregator**: Liga SendGrid, Twilio, Slack e mais.
- **Dynamic Templates**: Gere templates de mensagens com variáveis preenchidas pela IA.
- **Routing Logic**: Define condições para o envio (ex: se o user não leu o Slack em 5m, envia SMS).

## 🛠️ Como Implementar no Cursor

```markdown
# Courier Notification Logic

1. Use Courier Library for all notification triggers.
2. Select appropriate channel based on user preference.
3. Apply templates defined in the Courier workspace.
4. Monitor delivery status and log failures.
```

## 📈 Vantagens
- **Omnichannel Real**: Envie a mensagem certa no canal certo.
- **Agilidade de Desenvolvimento**: Crie workflows de notificação complexos num piscar de olhos.
- **Métricas de Engajamento**: Acompanhe o que os usuários abriram e onde clicaram.

> [!TIP]
> Use o Courier para notificar o usuário quando o **Autonomous Agent** completar uma tarefa longa com sucesso.
