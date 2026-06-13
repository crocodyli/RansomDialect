# Avaddon — Perfil de Negociação (CTI)

> 7 chats, 380 mensagens. Período: 2021.

---

## Resumo Executivo

Avaddon combina **profissionalismo superficial com agressividade real**. Usa sarcasmo (*":D"*, *"Tick tock tick tock"*), escalada emocional rápida após recusa, e descontos temporais agressivos (15% → 50%). Política geográfica única: alvos CIS recebem decryptor gratuito.

## Tom e Comunicação

- **Estilo:** Casual-profissional → sarcástico/agressivo sob pressão
- **Abertura:** *"You have been infected by the Avaddon ransomware. Price for you is $X"*
- **Marcadores:** *"We are a serious organization"*, *"Guys?"*, *"take a loan"*, *"Tick tock"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Rígido com degraus de desconto temporal; pergunta *"How much can you offer?"* |
| Prova | Test Decryption na landing (≤2MB); General Decryptor para toda a rede |
| Pressão | Blog, spam a terceiros, DDoS no site, ações judiciais, contagem regressiva |
| Flexibilidade | Média — descontos temporais sim, negociação de valor limitada |

## Insights

1. Usa histórico do chat contra vítima que recua (*"you wrote it"*)
2. Escalada emocional em minutos após recusa
3. **Exceção política:** alvos CIS = decryptor grátis
4. Não negocia arquivos individuais — só General Decryptor
5. Overnight follow-ups (*"Guys?"* às 05:20)

```
Flexibilidade: Média | Pressão: Alta | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`avaddon/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avaddon) |
| **Arquivos típicos** | `avaddon.txt` |
| **Extensão / artefato** | `{{ext}} (variável por campanha)` |
| **Frases-chave da nota** | *"Your network has been infected!"*, *"DO NOT DELETE THIS FILE"*, *"General Decryptor"* |
| **Continuidade com o chat** | Tom agressivo da nota evolui para sarcasmo e *Tick tock* no chat. |

**Se a nota contém...** → confirma **Avaddon** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Mimikatz`, `SharpDump`, `GMER`, `PowerTool`, `TDSSKiller`, `SoftPerfect NetScan`, `Anonfiles`, `MEGA`, `ProtonMail`, `Sendspace` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | DDoS e spam a terceiros na operação alinham com escalada emocional na negociação. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Avaddon** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
