# BlackMatter — Perfil de Negociação (CTI)

> 2 chats, 121 mensagens. Período: 2021.

---

## Resumo Executivo

BlackMatter usa **humor sarcástico para mascarar operação sofisticada**. Conhece detalhes íntimos da infraestrutura da vítima em tempo real (Rubrik destruído, tentativa de restore no domingo). Suspeita de pesquisadores sem prova de vínculo.

## Tom e Comunicação

- **Estilo:** Sarcástico/casual com camada profissional
- **Abertura:** *"Hello and welcome to BlackMatter. How may I help you?"* → $15M imediato
- **Marcadores:** *"virustotal.com"*, *"good pentest"*, *"time is on our side"*, *"Oh [redacted] you so clever)"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Piso 7 dígitos; 10% desconto rápido; rejeita ofertas condicionais |
| Prova | Screenshots (ibb.co) de hashes; amostras via privatlab; lista de DBs |
| Pressão | Conhecimento íntimo da infra; compara com competidor atacado |
| Verificação | Obrigatória: domain name, admin, backup software |

## Insights

1. Suspeita de pesquisadores/curiosos sem prova de vínculo
2. Conhece detalhes operacionais em tempo real
3. Compara com outras vítimas do setor
4. Tom informal mascarando sofisticação
5. Recusa negociação estruturada por tipo de dado

```
Flexibilidade: Média | Pressão: Média | Sofisticação: Alta
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`blackmatter/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackmatter) |
| **Arquivos típicos** | `blackmatter.txt` |
| **Extensão / artefato** | `.blackmatter / .pay2key` |
| **Frases-chave da nota** | *"BLACK ... Matter"*, *"How may I help you?"*, *"universal decryptor"* |
| **Continuidade com o chat** | Arte ASCII da nota; chat mantém sarcasmo e conhecimento de infra em tempo real. |

**Se a nota contém...** → confirma **BlackMatter** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `PrivatLab` |
| **Matrizes** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Impacket/Mimikatz típicos; chat usa sarcasmo e conhecimento de infra ao vivo. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **BlackMatter** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
