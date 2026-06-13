# Avos (AvosLocker) — Perfil de Negociação (CTI)

> 1 chat, 86 mensagens. Período: 2021. **Dataset limitado.**

---

## Resumo Executivo

Avos demonstra o modelo **RaaS com separação Staff/affiliate**. O Staff central oferece "customer support" mas delega decisões ao affiliate responsável pelo ataque. Tom profissional e moderado, distinto de grupos agressivos.

## Tom e Comunicação

- **Estilo:** Profissional, modelo "enterprise client" + customer support
- **Abertura:** *"As you are an enterprise client of ours, we will provide you with customer support"*
- **Marcadores:** *"Staff"*, *"affiliate"*, *"our terms and we never go against them"*, *"Thank you for your business"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Flexível: $150K → $100K → $85K aceito |
| Prova | Decrypt manual via riseup.net/anonfiles (.avos2 não suportado no portal) |
| Pressão | Recusa lista até acordo; ameaça de blog; deadline extensível (Labor Day) |
| Arquitetura | Staff central + affiliate com dados — limita provas de exfiltração |

## Insights

1. Separação operador/affiliate cria latência nas respostas
2. Extensão de deadline por feriados bancários
3. Negocia em BTC quando landing pede XMR
4. Relatório pós-pagamento excepcionalmente detalhado (Mimikatz, Forti VPN, Exchange)
5. Paciente com links quebrados da vítima

```
Flexibilidade: Alta | Pressão: Média | Sofisticação: Média
⚠️ Apenas 1 chat — validar com outras fontes
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`avoslocker/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avoslocker) |
| **Arquivos típicos** | `avoslocker.txt` |
| **Extensão / artefato** | `.avos / .avos2` |
| **Frases-chave da nota** | *"Your files have been encrypted"*, *"do not shutting down your computer"*, *"decryption key & application"* |
| **Continuidade com o chat** | Nota formal de AvosLocker; chat separa Staff central e affiliate RaaS. |

**Se a nota contém...** → confirma **Avos** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `LaZagne`, `Mimikatz`, `XenArmor`, `Avast Anti-Rootkit driver`, `NirSoft WinLister`, `Nmap`, `SoftPerfect NetScan`, `FileZilla`, `Gofile[.]io`, `PSCP` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Modelo RaaS Staff/affiliate reflete separação operador central vs. afiliado no chat. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Avos** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
