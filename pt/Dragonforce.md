# Dragonforce — Perfil de Negociação (CTI)

> 14 chats, 375 mensagens. Período: 2023–2024.

---

## Resumo Executivo

Dragonforce foca em **credibilidade da marca** (*"We're not newbies"*, *"DragonForce, we don't make mistakes"*). Preço em BTC (não USD), timer de 2 semanas, e flexibilidade após pushback da vítima.

## Tom e Comunicação

- **Estilo:** Direto/confiante; levemente dismissivo
- **Abertura:** *"exploring your financial possibilities"* → lista → preço BTC
- **Marcadores:** *"the bosses"*, temp.sh links, *"losing your reputation would be worse"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Flexível após pushback; ancora em BTC |
| Prova | Test decrypt no portal; 2–3 arquivos da lista |
| Pressão | Timer 2 semanas; reputação como alavanca principal |
| Recusa | Decrypt de arquivos grandes |

## Insights

1. Referencia facções concorrentes para desqualificar medo
2. Timer explícito como gatilho de publicação
3. Respostas curtas em chats sem negociação ativa
4. Foco em credibilidade vs. volume de dados
5. Estrutura party inconsistente (DragonForce / Attacker)

```
Flexibilidade: Média | Pressão: Média | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`dragonforce/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/dragonforce) |
| **Arquivos típicos** | `[rand].README.txt`, `readme.xt` |
| **Extensão / artefato** | `.dragonforce` |
| **Frases-chave da nota** | *"files have been stolen... and encrypted"*, *"We work for money"*, *"communication process:"* |
| **Continuidade com o chat** | Nota estruturada em passos; chat ancora em BTC com timer de 2 semanas. |

**Se a nota contém...** → confirma **Dragonforce** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | [`DragonForce`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/DragonForce.md) |
| **Tools-chave** | `AdFind`, `ADVobfuscator`, `LaZagne`, `Cobalt Strike`, `PsExec`, `MEGA`, `Advanced IP Scanner`, `Darkside/TrueSight driver (BYOVD)`, `Mimikatz`, `RClone` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Kill chain estruturada; chat ancora BTC com timer de 2 semanas. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Dragonforce** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`DragonForce/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/DragonForce) |
| **TTPs (MITRE)** | [`DragonForce-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/DragonForce/DragonForce-TTP.md) |
| **CVEs** | — |
| **TTPs-chave** | *T1190 — Vetores de acesso expostos*; *T1048 — Exfiltração antes do lock*; *T1486 — Operação RaaS com timer de leak* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.
