# Hive — Perfil de Negociação (CTI)

> 8 chats, 372 mensagens. Período: 2021–2022.

---

## Resumo Executivo

Hive possui comportamento **único no dataset para supply-chain attacks**: recusa categoricamente negociar com SMBs afetados indiretamente via MSP. Redireciona vítimas downstream ao fornecedor comprometido. Preço fixo de $1M sem flexibilidade.

## Tom e Comunicação

- **Estilo:** Formal; inflexível em supply-chain
- **Abertura:** *"Hello and welcome to Hive. How may I help you?"* → identificação da empresa
- **Marcadores:** *"introduce your company first"*, *"our target is [vendor]"*, *"not you, our goal is"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | $1M fixo para empresa-alvo; zero flexibilidade para downstream |
| Prova | Verificação por email corporativo → protonmail |
| Pressão | Redirecionamento ao vendor; pouca pressão de leak direta |
| Supply-chain | Múltiplas vítimas no mesmo chat (efeito cascata) |

## Insights

1. Recusa negociar com SMBs afetados indiretamente
2. Múltiplas vítimas no mesmo chat visível
3. Preço único sem flexibilidade para pequenos negócios
4. Narrativa de "accountability" do vendor
5. Pouca pressão de leak — foco em responsabilização terceira

```
Flexibilidade: Nenhuma (downstream) | Pressão: Baixa | Sofisticação: Baixa
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`hive/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hive) |
| **Arquivos típicos** | `HOW_TO_DECRYPT.txt`, `hive.txt` |
| **Extensão / artefato** | `.hive` |
| **Frases-chave da nota** | *"network has been breached"*, *"hiveleak... onion"*, *"purchase our decryption software"* |
| **Continuidade com o chat** | Nota padrão de leak site; chat formal *How may I help you?* com recusa a SMBs downstream. |

**Se a nota contém...** → confirma **Hive** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `GMER`, `PCHunter`, `Advanced IP Scanner`, `Bloodhound`, `SoftPerfect NetScan`, `MEGA`, `PrivatLab`, `RClone`, `Sendspace`, `UFile` |
| **Matrizes** | [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Supply-chain via MSP; chat recusa negociar com SMBs downstream. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Hive** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
