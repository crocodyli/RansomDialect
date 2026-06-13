# Hunters International — Perfil de Negociação (CTI)

> 1 chat, 29 mensagens. Período: 2024. **Dataset limitado.**

---

## Resumo Executivo

Um dos operadores **mais inflexíveis do dataset**. Modelo *"take it or leave it"* puro: *"I'm okay to get nothing"*, *"We are not in a hurry"*. Recusa explicitamente $1,5M e $4M contra pedido de $10M.

## Tom e Comunicação

- **Estilo:** Frio/minimalista; ultimato
- **Abertura:** *"Hi, how may I assist you?"* → confirma 2,79M arquivos, 2,3 TB
- **Marcadores:** *"I'm okay to get nothing"*, *"price is final"*, *"each case is unique"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Rígido ($10M); desconto só para "small companies" |
| Prova | Decrypt em ~20 min; confirmação de file tree |
| Pressão | Email em massa a competidores/parceiros/clientes |
| Recusa | $1,5M e $4M explicitamente rejeitados |

## Insights

1. Um dos mais inflexíveis do dataset
2. Recusa ofertas substanciais sem contra-proposta
3. Usa histórico da vítima mas rejeita comparação
4. Prova técnica rápida (~20 min)
5. Espera banco abrir vs. aceitar BTC existente

```
Flexibilidade: Muito Baixa | Pressão: Alta | Sofisticação: Média
⚠️ Apenas 1 chat — validar com outras fontes
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`hunters/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hunters) |
| **Arquivos típicos** | `READ ME NOW!.txt`, `Contact Us.txt`, `Contact Us2.txt` |
| **Extensão / artefato** | `.hunters (variantes)` |
| **Frases-chave da nota** | *"HUNTERS INTERNATIONAL group"*, *"military-grade AES"*, *"large amount of sensitive data was exfiltrated"* |
| **Continuidade com o chat** | Nota ultimato; chat confirma inflexibilidade (*I'm okay to get nothing*). |

**Se a nota contém...** → confirma **Hunters International** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Advanced IP Scanner`, `Advanced Port Scanner`, `RClone`, `WinSCP` |
| **Matrizes** | [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Operação ultimato desde a intrusão; chat confirma inflexibilidade total. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Hunters International** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`Hunters International/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/Hunters%20International) |
| **TTPs (MITRE)** | [`Hunters International-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Hunters%20International/Hunters%20International-TTP.md) |
| **CVEs** | — |
| **TTPs-chave** | *T1190 — Acesso inicial via serviços expostos*; *T1486 — AES + double extortion*; *T1490 — Inibição de recovery/backup* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.
