# RansomHub — Perfil de Negociação (CTI)

> 1 chat, 1 mensagem. Período: 2024. **Perfil incompleto.**

---

## Resumo Executivo

Dataset **insuficiente para perfil completo**. Única mensagem é um template FAQ automatizado sem diálogo humano. Formato sugere onboarding automatizado similar a Qilin/Akira.

## Conteúdo Capturado

**Template FAQ:**
- *"What happened?"* — listagem de categorias de dados comprometidos
- *"What if I decline?"* — social media, leak site, lawsuits, permanent halt

## O que NÃO está no dataset

- Preço
- Prova de decrypt
- Negociação de qualquer tipo
- Resposta a perguntas da vítima

## Insights (baseados no template)

1. Formato FAQ sugere automação de onboarding
2. Ênfase em consequências legais/reputacionais vs. técnicas
3. Provável chat abandonado ou truncado na coleta
4. Script provavelmente similar a Qilin (7 entregáveis)
5. **Validar com outras fontes CTI antes de usar este perfil**

```
Flexibilidade: N/D | Pressão: Alta (template) | Sofisticação: N/D
⚠️ PERFIL INCOMPLETO — apenas 1 mensagem
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`ransomhub/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ransomhub) |
| **Arquivos típicos** | `readme_[id].txt`, `readme_[id]_2.txt` |
| **Extensão / artefato** | `.ransomhub` |
| **Frases-chave da nota** | *"Visit our Blog"*, *"Your data is stolen and encrypted"*, *"TOR darknet"* |
| **Continuidade com o chat** | Nota é FAQ template; único chat capturado também é template automatizado. |

**Se a nota contém...** → confirma **RansomHub** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Mimikatz`, `BadRentdrv2`, `ThreatFire System Monitor driver (BYOVD)`, `Angry IP Scanner`, `Nmap`, `SoftPerfect NetScan`, `WKTools`, `PSCP`, `RClone`, `WinSCP` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | RMM comum no precursor; chat é FAQ template automatizado. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **RansomHub** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`RansomHub/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/RansomHub) |
| **TTPs (MITRE)** | [`RansomHub-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/RansomHub/RansomHub-TTP.md) |
| **CVEs** | — |
| **TTPs-chave** | *T1190 — Initial access via afiliados*; *T1219 — RMM comum no kill chain*; *T1486 — Modelo RaaS com leak site* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.
