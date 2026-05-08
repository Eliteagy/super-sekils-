---
tags: [security, hacking, python, automation]
type: resource-guide
created: 2026-04-06
---

# 🐍 3 Automações de Python para Hacking

Python é o "canivete suíço" do hacker moderno. Aqui estão 3 scripts essenciais para automatizares tarefas repetitivas de reconhecimento e exploração.

---

## 1. Port Scanner Minimalista (Recon Ativo)
Este script verifica que portas estão abertas num alvo sem precisares de ferramentas externas.

```python
import socket

def port_scanner(target_ip, ports):
    print(f"[*] A escanear {target_ip}...")
    for port in ports:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        s.settimeout(1) # Rápido
        result = s.connect_ex((target_ip, port))
        if result == 0:
            print(f"[+] Porta {port}: ABERTA")
        s.close()

# Exemplo de uso:
# target = "192.168.1.1"
# common_ports = [21, 22, 80, 443, 8080]
# port_scanner(target, common_ports)
```

---

## 2. Subdomain Enumerator (Recon Web)
Automatiza a descoberta de subdomínios (ex: `admin.alvo.com`) usando uma wordlist básica.

```python
import requests

def sub_enum(domain, wordlist_path):
    with open(wordlist_path, 'r') as file:
        for line in file:
            sub = line.strip()
            url = f"http://{sub}.{domain}"
            try:
                requests.get(url, timeout=2)
                print(f"[+] Subdomínio encontrado: {url}")
            except requests.ConnectionError:
                pass

# Exemplo: sub_enum("google.com", "subdomains.txt")
```

---

## 3. Metadata Extractor / Link Crawler
Este script entra numa página e extrai todos os links, útil para mapear a superfície de ataque de um site.

```python
from bs4 import BeautifulSoup
import requests

def get_links(url):
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'html.parser')
    links = [a['href'] for a in soup.find_all('a', href=True)]
    
    print(f"[*] Encontrados {len(links)} links em {url}:")
    for link in links:
        print(f" -> {link}")

# Exemplo: get_links("https://exemplo.com")
```

---

## 🚀 Como Executar
1. Instala as dependências: `pip install requests beautifulsoup4`
2. Guarda cada script como `.py`.
3. Integra-os no teu **Hacking Lab** para testar contra o Metasploitable!

> [!TIP]
> Podes combinar estes 3 num único "Agent" de Reconhecimento que corre tudo de uma vez.
