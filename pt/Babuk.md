# Babuk — Perfil de Negociação (CTI)

> 2 chats, 150 mensagens. Período: 2021–2022.

---

## Resumo Executivo

Babuk combina **formalidade técnica com ameaças legais agressivas** (GDPR, prisão do CEO). Pergunta explicitamente sobre seguro ransomware e usa Zoominfo para pricing. Remove post público como concessão pré-pagamento.

## Tom e Comunicação

- **Estilo:** Formal/técnico → ameaçador quando frustrado
- **Abertura:** *"Technical support is ready"* → pergunta sobre recovery company e insurance
- **Marcadores:** *"reasonable discount"*, *"insurance will pay everything"*, *"any dialogues only in this chat"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Baseado em turnover (Zoominfo): $400K → $100K → $85K |
| Prova | 4–5 arquivos + ecdh_pub_k.bin via file.io/dropmefiles |
| Pressão | GDPR/prisão CEO; fotos pessoais de funcionários; prazo 2 dias |
| Screening | Pergunta sobre insurance e recovery firm antes de negociar |

## Insights

1. Pergunta explicitamente sobre seguro ransomware
2. Remove post no fórum como concessão pré-pagamento
3. Usa Zoominfo para pricing (com erros em SMBs)
4. Suporte técnico pre-deal (ecdh_pub_k.bin)
5. Exige falar com donos, não intermediários

```
Flexibilidade: Média-Alta | Pressão: Alta | Sofisticação: Alta
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte externa: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente no ThreatLabz (verificado jun/2026) |
| **Artefato conhecido** | .babuk (conhecido em CTI; sem nota no ThreatLabz) |
| **Atribuição alternativa** | Sem entrada no ThreatLabz — use *Technical support is ready* e perguntas sobre seguro no chat. |

Consulte [`notes_mapping.json`](../notes_mapping.json) para o índice completo.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `File[.]io` |
| **Matrizes** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Ferramentas de credential theft precedem perguntas sobre seguro cyber no chat. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Babuk** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
