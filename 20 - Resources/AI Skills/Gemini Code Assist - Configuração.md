---
tags: [gemini, google, code-review, ai, github, configuration]
source: https://developers.google.com/gemini-code-assist/docs/customize-gemini-behavior-github
type: tool-documentation
created: 2026-04-04
---

# Gemini Code Assist - Configuração & Customização

## Estrutura de Ficheiros

```
.gemini/
├── config.yaml      # Configurações gerais
└── styleguide.md    # Guia de estilo personalizado
```

## config.yaml — Schema Completo

```yaml
# Ativa funcionalidades divertidas (poema no sumário do PR)
have_fun: false

# Configuração de memória persistente
memory_config:
  disabled: false  # true para desactivar para este repo

# Configuração de code review
code_review:
  disable: false  # true para desactivar reviews automáticos
  
  # Severidade mínima dos comentários: LOW, MEDIUM, HIGH, CRITICAL
  comment_severity_threshold: MEDIUM
  
  # Máximo de comentários de review (-1 = ilimitado)
  max_review_comments: -1
  
  # Configuração para quando o PR é aberto
  pull_request_opened:
    help: false       # Posta mensagem de ajuda
    summary: false    # Posta sumário do PR
    code_review: true # Posta code review
    include_drafts: true # Atua em draft PRs

# Padrões glob de ficheiros para ignorar
ignore_patterns: []
```

## Campos Importantes

### `comment_severity_threshold`

Define a severidade mínima dos comentários:
- **LOW** — Todas as sugestões (incluindo minor refactorings)
- **MEDIUM** — Padrão. Filtra sugestões menores
- **HIGH** — Só problemas significativos
- **CRITICAL** — Só problemas críticos

> Violações do style guide personalizado tipicamente **igualam ou excedem** o threshold definido.

### `ignore_patterns`

Usa [glob patterns](https://code.visualstudio.com/docs/editor/glob-patterns):

```yaml
ignore_patterns:
  - "*.min.js"
  - "vendor/**"
  - "dist/**"
  - "*.generated.*"
```

### `memory_config`

Se activaste "improved response quality" para múltiplos repos, podes desactivar para um repo específico:

```yaml
memory_config:
  disabled: true
```

## Configuração Multi-Repositório

### Consumer (Grátis)
1. Ir para [settings do Gemini Code Assist](https://codeassist.google/code-review)
2. Login com GitHub
3. Selecionar conta e aceitar ToS
4. Configurar na página "Free agent"
5. Save

### Enterprise
1. Google Cloud Console → Gemini Code Assist → Agents & Tools
2. Secção "Code Assist Source Code Management" → Advanced
3. Selecionar conexão na tabela
4. Tab "Settings" → alterar configurações
5. Save

> **Prioridade**: `config.yaml` do repositório **sobrepõe** configurações do grupo.

## Style Guide

Adiciona um ficheiro `styleguide.md` na pasta `.gemini/` com regras específicas:

```markdown
# Style Guide

## Naming Conventions
- Use camelCase for variables
- Use PascalCase for components
- Use UPPER_SNAKE_CASE for constants

## Code Quality
- Maximum function length: 50 lines
- Always handle errors explicitly
- Prefer TypeScript strict mode
```

## Links

- [Schema completo](https://developers.google.com/gemini-code-assist/docs/customize-gemini-behavior-github#schema)
- [Style guide docs](https://developers.google.com/gemini-code-assist/docs/code-review-style-guide)
- [Setup para GitHub](https://developers.google.com/gemini-code-assist/docs/set-up-code-assist-github)
- [Usar no GitHub](https://developers.google.com/gemini-code-assist/docs/use-code-assist-github)
