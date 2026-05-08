---
tags: [skill, premiere-pro, video-editing, mcp, automation, dx]
source: https://github.com/hetpatel-11/Adobe_Premiere_Pro_MCP
type: skill-documentation
created: 2026-05-05
---

# Skill: Adobe Premiere Pro MCP

> **Automação de edição de vídeo de elite: Controla o Premiere Pro via IA para montagem, efeitos e gestão de projetos.**

Esta skill permite que o Gemini CLI (ou outros agentes MCP) interaja diretamente com o Adobe Premiere Pro, transformando descrições em linguagem natural em ações de edição reais na timeline.

## 🚀 Capacidades de Automação

O servidor expõe quase 100 ferramentas para manipular o Premiere:

- **AI-Driven Assembly**: Criação de rough cuts, spots de produto e demos de marca a partir de templates.
- **Timeline Control**: Operações de "razor" (corte), movimentação de clips e ajuste de faixas.
- **Efeitos e Transições**: Aplicação programática de efeitos (Blur, B&W) e transições (Cross Dissolve).
- **Gestão de Media**: Importação para bins específicos, gestão de markers e organização de proxies.
- **Interchange**: Exportação de sequências e geração de XMLs.

## 🛠️ Requisitos e Configuração

Para utilizar esta skill, o ambiente deve estar configurado:

1. **Software**: Premiere Pro 2020+ (Recomendado 2025/2026) e Node.js 18+.
2. **CEP Debug Mode**: Ativado no macOS (necessário para extensões não assinadas).
3. **UXP Developer Mode**: Ativado nas preferências do Premiere (`UXP Plugins > Enable developer mode`).
4. **MCP Bridge Panel**: O painel customizado deve estar aberto no Premiere (`Window > Extensions > MCP Bridge`).

## 📐 Fluxo de Trabalho AI-Edit

| Tarefa | Ação da IA |
| :--- | :--- |
| **Discovery** | Listar sequências e inspecionar o projeto atual. |
| **Ingest** | Organizar novos assets em bins estruturados por data/tipo. |
| **Rough Cut** | Montar clips na timeline baseando-se num guião ou "Clip Plan". |
| **Polish** | Aplicar color grading básico e transições entre cortes. |
| **Export** | Preparar o projeto para renderização final. |

## ⚠️ Limitações Conhecidas
- Foco principal em **macOS**.
- Dependência de polling via diretório partilhado (`/tmp/premiere-mcp-bridge`).
- Algumas operações de UI profunda não são expostas pela API de scripting da Adobe.

## 📚 Referências Oficiais
- [GitHub Repository](https://github.com/hetpatel-11/Adobe_Premiere_Pro_MCP)
- [Adobe Premiere Scripting Guide](https://premiere-scripting-guide.readthedocs.io/)

---
*Gerado via Gemini CLI para a The Elite Agency.*
