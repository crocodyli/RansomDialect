# MountLocker — Perfil de Negociação (CTI)

> 1 chat, 60 mensagens. Período: 2020. **Dataset limitado.**

---

## Resumo Executivo

MountLocker usa **framework legal como principal vetor de pressão** — class-action lawsuits (link ZDNet), comparação com perdas legais. Tom educado (*"Sincerely, yours"*) mas firme. Rejeita argumentos COVID/wildfires.

## Tom e Comunicação

- **Estilo:** Profissional/corporativo; argumentação legal-financeira
- **Abertura:** *"Greetings! We are ready to help you!"* → bom/mau cenário → $9M → 1TB exfiltrado
- **Marcadores:** *"businessmans"*, *"Sincerely, yours"*, chat protegido por senha

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Rígido ($9M); espera proposta entre 5–50% do pedido |
| Prova | Arquivo ≤5MB test decrypt; amostra via privatlab |
| Pressão | Class-action lawsuits; PII detalhado; onion blog; timer |
| OSINT | Cita receita estimada (~$1B) para justificar preço |

## Insights

1. Framework legal como vetor principal de pressão
2. Rejeita COVID/wildfires como irrelevantes
3. Espera 5–50% do pedido, não 90% abaixo
4. Tom mais educado que média de 2020
5. Oferta de chat protegido por senha

```
Flexibilidade: Baixa-Média | Pressão: Alta | Sofisticação: Alta
⚠️ Apenas 1 chat — validar com outras fontes
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte externa: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente no ThreatLabz (verificado jun/2026) |
| **Artefato conhecido** | .mount-locker (conhecido em CTI; sem nota no ThreatLabz) |
| **Atribuição alternativa** | Sem entrada no ThreatLabz — use framework legal e *Greetings! We are ready to help you!* no chat. |

Consulte [`notes_mapping.json`](../notes_mapping.json) para o índice completo.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `MEGA` |
| **Matrizes** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Poucas tools catalogadas; chat usa framework legal como pressão. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **mount-locker** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
