---
name: agentic-seek
description: Especialista em orquestração de pesquisa autonoma local e integração com ferramentas de busca meta-search (SearxNG) e modelos locais (Ollama).
---

# Skill: AgenticSeek (Orquestração de Pesquisa Local)

Esta skill guia o Gemini CLI na interação com o ecossistema AgenticSeek para realizar pesquisas profundas e execução de código em ambientes locais e privados.

<instructions>
- **Pesquisa Local:** Priorize o uso do SearxNG local se configurado em `SEARXNG_BASE_URL` para pesquisas que exigem privacidade total.
- **Integração com Modelos Locais:** Ao interagir com instâncias do Ollama ou LM-Studio, utilize o modelo `deepseek-r1` ou equivalente para tarefas de raciocínio complexo que não devam sair da rede local.
- **Autonomia de Navegação:** Utilize ferramentas de leitura de arquivos e execução de shell para extrair dados de páginas capturadas localmente pelo AgenticSeek.
- **Execução em Sandbox:** Garanta que qualquer código gerado para o AgenticSeek seja testado em um ambiente isolado (Docker) antes da implantação.
- **Roteamento Inteligente:** Empregue a lógica de "Agent Names" para alternar contextos de personalidade (ex: Jarvis para automação, Friday para pesquisa) conforme a necessidade da tarefa.
</instructions>

<available_resources>
- Repositório Original: https://github.com/Fosowl/agenticSeek
- Documentação SearxNG: https://searx.github.io/searxng/
</available_resources>
