---
tags: [skill, testing, playwright, webapp]
source: https://github.com/ComposioHQ/awesome-claude-skills
type: skill-documentation
created: 2026-04-04
---

# Skill: Webapp Testing (Playwright)

> **Automação e testes de aplicações web locais.**

## Ferramentas
- **Playwright:** Para interação direta com o browser.
- **with_server.py:** Script helper para gerir o ciclo de vida do servidor (Vite, Webpack, etc).

## Pattern: Reconnaissance-Then-Action
1. **Navegação:** `page.goto('http://localhost:5173')`.
2. **Espera Ativa:** `page.wait_for_load_state('networkidle')`. CRÍTICO para apps JS/React.
3. **Inspeção:** Tirar screenshot (`page.screenshot`) para ver o estado real antes de agir.
4. **Seletores:** Identificar IDs ou classes no DOM renderizado.

## Exemplo de Script
```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch(headless=True)
    page = browser.new_page()
    page.goto('http://localhost:3000')
    page.wait_for_load_state('networkidle')
    # Validar se o botão de Login existe
    assert page.locator('button:has-text("Login")').is_visible()
    browser.close()
```
