# Mallox — Perfil de Negociação (CTI)

> 3 chats, 108 mensagens. Período: 2023.

---

## Resumo Executivo

Mallox é um dos poucos grupos com **automação de desconto via BOT** no chat. Desconfia universalmente de alegações de backup intacto (*"All customers say so"*). Roles múltiplos: BOT, Support, Hervios.

## Tom e Comunicação

- **Estilo:** Direto; BOT + humano
- **Abertura:** Preço na landing; BOT aplica desconto % com data de expiração
- **Marcadores:** *"Discount X%. Discount expiration date"*, *"I'm not interested in your personal income"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | BOT aplica desconto automático; piso ~$30K de $33,7K |
| Prova | Test file via dropmefiles; delay se técnico offline |
| Pressão | Mínima; *"company needs the data, they can pay"*
| Recusa | Respostas monossilábicas (*"no"*) para ofertas baixas |

## Insights

1. Automação de desconto via BOT — raro no dataset
2. Desconfia universalmente de claims de backup
3. Negociação via intermediário/recovery frequente
4. Chat parcialmente chinês/inglês
5. Naming inconsistente (Hervios/hiervos)

```
Flexibilidade: Média | Pressão: Baixa | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`mallox/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/mallox) |
| **Arquivos típicos** | `FILE RECOVERY.txt`, `HOW TO BACK FILES.txt` |
| **Extensão / artefato** | `.mallox / .ma1x0` |
| **Frases-chave da nota** | *"files are encrypted and can not be used"*, *"decrypt one file for free"*, *"Do not try to change or restore files yourself"* |
| **Continuidade com o chat** | Nota oferece test decrypt no site; chat usa BOT com desconto % automático. |

**Se a nota contém...** → confirma **Mallox** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Dropmefiles`, `File[.]io`, `Sendspace` |
| **Matrizes** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Dropmefiles/File.io; chat usa BOT com desconto % automático. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Mallox** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
