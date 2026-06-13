# trinity — Perfil de Negociação (CTI)

> 14 chats, 713 mensagens.

---

## Resumo Executivo

trinity possui modelo **per-device raro no dataset** — 0,25 BTC/PC, 0,5 BTC/servidor. Sem double extortion nos chats. Usa pagamentos anteriores de *"coworkers"* como prova social. Chats muito curtos com negociação quase inexistente.

## Tom e Comunicação

- **Estilo:** Minimalista; seco; transacional
- **Abertura:** *"Hi"* → preço BTC por endpoint
- **Marcadores:** *"Price for decrypt X btc"*, *"we don't work with middlemen"*, inventário de hosts

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Fixo por máquina; sem desconto; cita outros pagantes |
| Prova | 1 arquivo <1MB grátis; não decrypta backups |
| Pressão | Mínima; expõe email de outro pagante como prova social |
| Recusa | Intermediários categoricamente |

## Insights

1. Modelo per-device raro (maioria é per-network)
2. Host inventory enviado proativamente
3. Prova social via pagamentos de "coworkers"
4. Sem double extortion nos chats
5. Negociação quase inexistente — transação direta

```
Flexibilidade: Nenhuma | Pressão: Baixa | Sofisticação: Baixa
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`trinity/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/trinity) |
| **Arquivos típicos** | `README.txt` |
| **Extensão / artefato** | `.trinitylocker` |
| **Frases-chave da nota** | *"TRINITY LOCKER"*, *"helpdesk101@onionmail.com"*, *"download TOR"* |
| **Continuidade com o chat** | Nota com portal Tor/e-mail; chat cobra 0,25 BTC por endpoint sem flexibilidade. |

**Se a nota contém...** → confirma **trinity** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — hunt/IR durante crise. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem entrada dedicada no RTM (jun/2026) |
| **Checklist geral** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Minimalismo operacional; chat cobra por endpoint sem flexibilidade. |

Índice: [`operational_mapping.json`](../operational_mapping.json)
---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
