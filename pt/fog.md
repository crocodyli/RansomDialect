# fog — Perfil de Negociação (CTI)

> 6 chats, 333 mensagens. Período: 2024–2025.

---

## Resumo Executivo

fog tem um dos **scripts de abertura mais curtos** do dataset (*"hi"* → lista RAR → preço). Delega decisões aos *"bosses"* e demonstra conhecimento técnico do próprio ransomware (`.fog.savepoint`). Tom cooperativo em deals que fecham.

## Tom e Comunicação

- **Estilo:** Casual/minimalista; pragmático
- **Abertura:** *"hi"* → lista RAR → prova + test decrypt + *"bosses are demanding $X"*
- **Marcadores:** *"bosses"*, *"Do we work?"*, *"Standing by"*, *"We work with bitcoins"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Flexível com aprovação dos bosses ($800K → $715K; ~$150K fechado) |
| Prova | 3 arquivos criptografados descriptografados; conhecimento de .fog.savepoint |
| Pressão | Implícita; sem escalada agressiva nos chats analisados |
| Pós-pagamento | Decryptor .exe para Win/ESXi; recusa pagamento fracionado |

## Insights

1. Abertura mais curta do dataset
2. Negociação via "bosses" como autoridade externa
3. Conhecimento técnico do próprio ransomware
4. Tom cooperativo quando vítima engaja
5. Link CSO Online para compra BTC

```
Flexibilidade: Média-Alta | Pressão: Baixa-Média | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`fog/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/fog) |
| **Arquivos típicos** | `readme.txt`, `readme2.txt` |
| **Extensão / artefato** | `.fog` |
| **Frases-chave da nota** | *"We call ourselves Fog"*, *"victim of a cyber attack"*, *"The sooner you contact us"* |
| **Continuidade com o chat** | Nota minimalista com identidade Fog; chat mantém abertura *hi* e delegação aos *bosses*. |

**Se a nota contém...** → confirma **fog** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `DonPAPI`, `Veeam-Get-Creds`, `Advanced Port Scanner`, `SharpShares`, `SoftPerfect NetScan`, `PsExec`, `Powercat`, `Proxychains`, `Certipy`, `Impacket` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Operação enxuta; chat minimalista com delegação aos *bosses*. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **fog** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
