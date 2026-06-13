# Ranzy — Perfil de Negociação (CTI)

> 2 chats, 56 mensagens. Período: 2020–2021.

---

## Resumo Executivo

Ranzy é um dos grupos **mais simples do dataset** — modelo "smash and grab" sem double extortion visível. Respostas de 1–3 palavras, preço fixo ($7.000), sem prova de decrypt ou negociação.

## Tom e Comunicação

- **Estilo:** Minimalista/casual
- **Abertura:** *"hi"* → *"price for your case is $7,000"*
- **Marcadores:** howtobuybitcoins.info, *"yes correct address"*, *"ok, without discount"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Fixo; sem desconto; sem negociação |
| Prova | Nenhuma |
| Pressão | Nenhuma explícita |
| Pagamento | Wallet BTC direto; recusa trocar endereço |

## Insights

1. Sem double extortion visível
2. Sem prova de decrypt ou lista de dados
3. Não negocia desconto nem valor
4. Respostas de 1–3 palavras
5. Representa era primitiva (2020–21) do ecossistema

```
Flexibilidade: Nenhuma | Pressão: Baixa | Sofisticação: Nenhuma
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`ranzy/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ranzy) |
| **Arquivos típicos** | `ranzy.txt` |
| **Extensão / artefato** | `.ranzy` |
| **Frases-chave da nota** | *"Your servers is LOCKED"*, *"eviluser@tutanota.com"*, *"personal id:"* |
| **Continuidade com o chat** | Nota minimalista por e-mail; chat confirma preço fixo $7K sem double extortion. |

**Se a nota contém...** → confirma **Ranzy** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `UFile` |
| **Matrizes** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Operação smash-and-grab; chat fixa $7K sem double extortion. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Ranzy** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
