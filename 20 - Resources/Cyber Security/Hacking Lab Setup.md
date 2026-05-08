---
tags: [security, hacking, lab-setup, virtualization]
type: resource-guide
created: 2026-04-05
---

# 🏗️ Hacking Lab Setup: O Teu Ginásio de Segurança

Para aprenderes hacking a sério, precisas de um ambiente seguro e isolado. Aqui está o guia para montares o teu próprio laboratório de testes (Home Lab).

## 🖥️ 1. Virtualização (O Coração do Lab)

Não queres correr ferramentas de hacking diretamente no teu sistema principal. Usa uma "Virtual Machine" (VM).

| Software | Prós | Contras |
|----------|------|---------|
| **VMware Workstation Player** | Estável, excelente performance. | Grátis para uso pessoal, mas limitado. |
| **Oracle VirtualBox** | 100% Open Source, muitas funções. | Às vezes menos estável que o VMware. |

**Dica**: Recomendo o **VMware Player** pela estabilidade.

---

## 🧛 2. Máquina de Ataque (O Teu Arsenal)

Aqui é onde vais correr o teu sistema operativo de ataque.
*   **Kali Linux**: A escolha padrão. Vem com milhares de ferramentas pré-instaladas.
*   **Parrot Security OS**: Uma alternativa mais leve e focada em privacidade.

**Setup**: Descarrega o "Pre-built VM Image" do site oficial [kali.org](https://www.kali.org/get-kali/#kali-platforms). É só abrir no VMware e está pronto a usar.

---

## 🎯 3. Máquinas Alvo (As Vítimas)

Vais precisar de sistemas vulneráveis para atacar legalmente.
*   **Metasploitable 2**: Um Linux "intencionalmente" vulnerável. Excelente para treinar Nmap e Metasploit.
*   **Windows 10/11 VM**: Podes baixar imagens de avaliação oficiais da Microsoft para testar ataques em Windows.
*   **VulnHub**: Um site com centenas de VMs (CTFs) prontas a importar.

---

## 🌐 4. Networking: Isolamento é Tudo

Para garantires que nada do teu Lab "foge" para a tua rede de casa:
*   **Host-Only Adapter**: As VMs comunicam entre si e com o teu PC, mas não têm internet.
*   **NAT Network**: As VMs têm internet (para updates), mas estão "atrás" de um router virtual.

> [!CAUTION]
> **Nunca** coloques máquinas como o Metasploitable em modo **Bridged** (ligadas diretamente ao teu router de casa). Isso torna-as visíveis e atacáveis por qualquer pessoa na internet!

---

## 🧰 5. Primeiros Passos no Lab

Depois de tudo montado, tenta este workflow:
1.  Faz `ifconfig` no Kali e no Metasploitable para veres os IPs.
2.  No Kali, corre `nmap -sV [IP-do-Metasploitable]`.
3.  Analisa as portas abertas e procura vulnerabilidades no Google (ex: "vsftpd 2.3.4 exploit").

---

## 📚 Recursos para Praticar
*   **TryHackMe**: Salas guiadas passo-a-passo.
*   **HackTheBox**: Desafios mais avançados.
*   **VulnHub**: Para download de labs offline.

> [!TIP]
> Mantém um diário de cada ataque bem-sucedido aqui no Obsidian. Usa o template `New Note` para cada máquina que derrotares!
