---
tags: [gemini, google, code-review, ai, github, usage, commands]
source: https://developers.google.com/gemini-code-assist/docs/review-github-code
type: tool-documentation
created: 2026-04-04
---

# Gemini Code Assist - Como Usar no GitHub

## Fluxo Automático

1. **Abres um Pull Request** no GitHub
2. Em ~5 minutos, `gemini-code-assist[bot]` é adicionado como reviewer
3. O bot publica:
   - **Comentário geral** na tab Conversation com feedback
   - **Comentários inline** em partes específicas do código
   - **Sugestões de código** prontas para commit

## Comandos Manuais

Podes invocar o Gemini a qualquer momento criando um **issue comment** (comentário na página do PR):

### Via menção directa
```
@gemini-code-assist Podes explicar o que esta função faz?
```

### Via comandos /gemini
```
/gemini review     → Solicita uma code review completa
/gemini summary    → Gera um sumário do PR
/gemini help       → Lista todos os comandos disponíveis
```

## Sugestões Ready-to-Commit

Quando o Gemini sugere alterações de código:
1. A sugestão aparece como um **code block** inline no PR
2. Podes revisar a sugestão directamente
3. Clicas **"Commit suggestion"** para aplicar sem sair do GitHub

## Feedback

- **👍** nos comentários do bot → Feedback positivo
- **👎** nos comentários do bot → Feedback negativo (ajuda a melhorar)

## Limitações

- ❌ Não atua em ficheiros dentro de `.github/workflows/` (por segurança)
- ❌ Não é um repositório — é um serviço/app do GitHub Marketplace
- ⚠️ Review inicial pode demorar até 5 minutos

## Ecosystem Gemini

O Gemini Code Assist faz parte do ecossistema mais amplo:

| Produto | Descrição |
|---------|-----------|
| **Gemini Code Assist** | Code review em PRs (GitHub App) |
| **Gemini CLI** | CLI para interagir com Gemini ([repo](https://github.com/google-gemini/gemini-cli)) |
| **Gemini in IDEs** | Extensão para VS Code, Android Studio, etc. |
| **Gemini Agent Mode** | Modo agente para pair programming |

## Setup Rápido

1. Vai a [GitHub Marketplace - Gemini Code Assist](https://github.com/marketplace/gemini-code-assist)
2. Clica **"Add"**
3. Seleciona a conta/organização
4. Seleciona os repositórios
5. Confirma instalação
6. (Opcional) Adiciona `.gemini/config.yaml` para personalizar → Ver [[Gemini Code Assist - Configuração]]

## Links Relacionados

- [[Gemini Code Assist - Overview]]
- [[Gemini Code Assist - Configuração]]
- [Documentação Completa](https://developers.google.com/gemini-code-assist/docs/overview)
- [Agent Mode](https://developers.google.com/gemini-code-assist/docs/agent-mode)
- [Supported Languages](https://developers.google.com/gemini-code-assist/docs/supported-languages)
