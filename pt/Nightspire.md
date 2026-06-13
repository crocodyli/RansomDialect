# Nightspire — Perfil de Negociação (CTI)

> 7 chats, 367 mensagens. Período: 2025–2026.

---

## Resumo Executivo

Nightspire representa a **nova geração de negociadores** — usa filings públicos (receita $14,8M, lucro $2,1M) para ancorar preço. Escalada agressiva quando vítima menciona FBI (*"FBI won't stop your board"*). Foco em custo de downtime + multas contratuais ($500K+).

## Tom e Comunicação

- **Estilo:** Agressivo/profissional; orientado a OSINT financeiro público
- **Abertura:** Preço direto ($100K–$150K BTC) + detalhamento de dados sensíveis
- **Marcadores:** *"We already researched your company"*, *"Public filings show"*, *"FBI won't stop your board"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Flexível incremental ($100K → $90K → $135K → $110K); % receita/lucro |
| Prova | Lista via gofile.io; amostras de contratos/PII como pressão |
| Pressão | Penalidades contratuais; SEC; spam via competidores; dark web markets |
| Escalada | Menção a FBI/autoridades aumenta agressividade |

## Insights

1. OSINT de filings públicos (estilo 10-K) para pricing
2. Escalada agressiva com menção a law enforcement
3. Descontos pequenos (~10%) como "goodwill"
4. Foco em downtime + multas contratuais
5. Tom mais sofisticado que grupos 2020–21

```
Flexibilidade: Média | Pressão: Muito Alta | Sofisticação: Média-Alta
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`nightspire/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/nightspire) |
| **Arquivos típicos** | `nightspire_readme.txt`, `[NSPIRE_MSG].txt`, `readme.txt` |
| **Extensão / artefato** | `.nspire / .nightspire` |
| **Frases-chave da nota** | *"sensetive data are stolen and encrypted"*, *"pay within 3 days"*, *"DO NOT USE THIRD PARTY SOFTWARE"* |
| **Continuidade com o chat** | Nota com prazo 3 dias; chat escala com OSINT de filings 10-K e menção a FBI. |

**Se a nota contém...** → confirma **Nightspire** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Everything.exe`, `MEGA`, `WinSCP` |
| **Matrizes** | [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Exfiltração pré-lock; chat escala com OSINT de filings 10-K. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Nightspire** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
