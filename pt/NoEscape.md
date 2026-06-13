# NoEscape — Perfil de Negociação (CTI)

> 2 chats, 10 mensagens. Período: 2023. **Dataset muito limitado.**

---

## Resumo Executivo

NoEscape apresenta **tom polido contrastando com pressão legal** (*"Hello sir"*, *"your silence will only worsen"*). Dataset sem negociação de preço capturada — foco em test decrypt via portal e publicação automática após timer.

## Tom e Comunicação

- **Estilo:** Formal/cortês
- **Abertura:** Identificação + preço (~$80K) + instrução test decrypt (≤5MB)
- **Marcadores:** *"Hello sir"*, *"Can i help you?"*, link onion do blog

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Não negociado nos chats disponíveis |
| Prova | Test decryptor na landing page apenas |
| Pressão | Press release no blog; *"last warning"* 24h; processos |
| Comportamento | Monólogo de pressão sem resposta da vítima |

## Insights

1. Sem negociação de preço capturada
2. Tom polido vs. pressão legal
3. Foco em portal, não chat
4. Publica sem diálogo se silêncio
5. Possível sucessor de estilo Avaddon/Hive

```
Flexibilidade: N/D | Pressão: Média-Alta | Sofisticação: Baixa
⚠️ Apenas 2 chats sem negociação — perfil incompleto
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`noescape/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/noescape) |
| **Arquivos típicos** | `HOW_TO_RECOVER_FILES.txt`, `HOW_TO_RECOVER_FILES_no_personal_id.txt` |
| **Extensão / artefato** | `.noescape` |
| **Frases-chave da nota** | *"HOW TO RECOVER FILES"*, *"personal id"*, *"DO NOT MODIFY FILES"* |
| **Continuidade com o chat** | Nota formal com ID pessoal; chat polido com test decrypt via portal. |

**Se a nota contém...** → confirma **NoEscape** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — hunt/IR durante crise. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem entrada dedicada no RTM (jun/2026) |
| **Checklist geral** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Sem entrada RTM; chat formal com test decrypt via portal. |

Índice: [`operational_mapping.json`](../operational_mapping.json)
---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
