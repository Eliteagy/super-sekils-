---
tags: [gemini, google, code-review, ai, github-app]
source: https://github.com/marketplace/gemini-code-assist
type: tool-documentation
created: 2026-04-04
---

# Gemini Code Assist

> **Bring the power of Gemini to the pull request process**

Gemini Code Assist é uma **GitHub App** da Google que actua como um code reviewer AI-powered nos teus Pull Requests. Não é um repositório de código — é um serviço/bot que se instala no GitHub.

## O que faz

- **Pull Request Summary** — Quando um novo PR é aberto, o Gemini Code Assist fornece uma review inicial em ~5 minutos
- **Code Review Automático** — Adiciona-se automaticamente como reviewer e publica comentários inline no código
- **Sugestões Ready-to-Commit** — Fornece alterações de código prontas para commit directamente no PR
- **Interação via Comandos** — Podes invocar o Gemini a qualquer momento com comandos

## Comandos Disponíveis

| Comando | Descrição |
|---------|-----------|
| `/gemini review` | Solicita uma code review |
| `/gemini summary` | Gera um sumário do PR |
| `/gemini help` | Mostra ajuda |
| `@gemini-code-assist` | Menção directa para perguntas |

## Customização

Podes personalizar o comportamento criando ficheiros na pasta `.gemini/` na raiz do repositório:

- **`.gemini/config.yaml`** — Configurações gerais
- **`.gemini/styleguide.md`** — Guia de estilo para reviews

## Tags do Marketplace

- `ai-assisted`
- `code-review`

## Links Importantes

- [GitHub Marketplace](https://github.com/marketplace/gemini-code-assist)
- [Documentação Oficial](https://developers.google.com/gemini-code-assist/docs/review-github-code)
- [Customização](https://developers.google.com/gemini-code-assist/docs/customize-gemini-behavior-github)
- [Privacy Policy](https://policies.google.com/privacy)
- [Terms of Service](https://policies.google.com/terms)

## Versões

| Aspecto | Consumer (Grátis) | Enterprise |
|---------|-------------------|------------|
| Setup | Directo no GitHub | Via Google Cloud |
| Config | Per-repository | Multi-repository via GCP |
| Style Guide | Per-repository | Multi-repository via GCP |
| GitHub Types | GitHub.com | GitHub Enterprise Server + Cloud |

## Considerações

- Não gera sumários/sugestões para ficheiros em `.github/workflows/` (segurança)
- Versão Enterprise usa Developer Connect connection (região `us-east1`)
- Feedback: 👍 e 👎 nos comentários do bot
