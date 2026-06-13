# Darkside — Perfil de Negociação (CTI)

> 5 chats, 425 mensagens. Período: 2020–2021.

---

## Resumo Executivo

Darkside foi **pioneiro em pressão de mercado de capitais** — ameaça contatar traders para short de ações. Personaliza abertura com nome da empresa, dados de seguro cyber (Beazley), linha de crédito e NASDAQ. Tom frio e calculado.

## Tom e Comunicação

- **Estilo:** Profissional/frio; ameaçador com intel financeiro detalhado
- **Abertura:** Saudação personalizada + intel financeiro + volume exfiltrado
- **Marcadores:** *"Are you ready for a dialog?"*, *"we always do what was promised"*, *"your liquidity allows"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Rígido; $10M inicial; desconto temporal 24h apenas |
| Prova | Free decrypt test via portal; arquivo devolvido com instrução de rename |
| Pressão | Forbes, NYT, Bloomberg; short sellers; publicação faseada |
| OSINT | Beazley, Response Limit, apólice de seguro específica |

## Insights

1. Pioneiro em pressão de mercado de capitais (short sellers)
2. Exige proposta para estender timer
3. Conhece apólice de seguro específica da vítima
4. Monologuista quando vítima ignora
5. Desconto vinculado a velocidade, não capacidade real

```
Flexibilidade: Baixa | Pressão: Muito Alta | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`darkside/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/darkside) |
| **Arquivos típicos** | `darkside.txt` |
| **Extensão / artefato** | `.darkside` |
| **Frases-chave da nota** | *"Welcome to DarkSide"*, *"universal decryptor"*, *"backups are deleted"* |
| **Continuidade com o chat** | Nota fria e direta; chat escala com OSINT financeiro e ameaças à imprensa. |

**Se a nota contém...** → confirma **Darkside** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Mimikatz`, `SessionGopher`, `Darkside/TrueSight driver (BYOVD)`, `ADRecon`, `AdFind`, `Advanced IP Scanner`, `SoftPerfect NetScan`, `Bashupload`, `MEGA`, `pCloud` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Bashupload/exfil tools; chat escala OSINT financeiro e ameaças à imprensa. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Darkside** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
