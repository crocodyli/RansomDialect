# RunSomeWares (RSW) — Perfil de Negociação (CTI)

> 1 chat, 27 mensagens. Período: 2025. **Dataset limitado.**

---

## Resumo Executivo

RunSomeWares demonstra **TTPs maduros de 2025** com tom cooperativo quando vítima engaja seriamente. Pesquisa reputação/família da vítima para pricing. Flexível em timeline se vítima dá data concreta.

## Tom e Comunicação

- **Estilo:** Direto/pragmático; cooperativo
- **Abertura:** Lista exaustiva → prova de arquivos → test decrypt
- **Marcadores:** *"We analized the company's revenue"*, *"most influential family"*, *"Let's get a deal"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Flexível com análise de receita; desconto por velocidade |
| Prova | 5 arquivos por nome; decrypt de binários; public share para grandes |
| Pressão | *"Your time is up. This is last chance"*; headline de jornal |
| Flexibilidade | Estende timer se vítima dá data concreta de pagamento |

## Insights

1. Pesquisa reputação/família para pricing
2. Flexível em timeline com data concreta
3. Decrypt de binários com instrução text editor
4. Tom cooperativo com engajamento sério
5. Chat recente com TTPs maduros

```
Flexibilidade: Média-Alta | Pressão: Média | Sofisticação: Alta
⚠️ Apenas 1 chat — validar com outras fontes
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte externa: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente no ThreatLabz (verificado jun/2026) |
| **Artefato conhecido** | .RSW (conhecido em CTI; sem nota no ThreatLabz) |
| **Atribuição alternativa** | Sem entrada no ThreatLabz — use *We analized the company's revenue* e tom cooperativo no chat. |

Consulte [`notes_mapping.json`](../notes_mapping.json) para o índice completo.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — hunt/IR durante crise. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem entrada dedicada no RTM (jun/2026) |
| **Checklist geral** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | OSINT de receita na intrusão; chat cooperativo se vítima engaja. |

Índice: [`operational_mapping.json`](../operational_mapping.json)
---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
