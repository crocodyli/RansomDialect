# Qilin — Perfil de Negociação (CTI)

> 2 chats, 39 mensagens. Período: 2024–2025.

---

## Resumo Executivo

Qilin opera com **script quase intercambiável com Akira/RansomHub** — pacote de 7 entregáveis pós-pagamento, file tree, 3 arquivos prova + 3 test decrypt. Diferencial: ameaça de venda de dados a **autoridades fiscais**.

## Tom e Comunicação

- **Estilo:** Profissional/padrão; paciente
- **Abertura:** 7 entregáveis pós-pagamento → file tree → provas
- **Marcadores:** *"forget about us forever"*, *"activation key"*, *"On Monday we are waiting"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Não detalhado nos chats (foco em provas primeiro) |
| Prova | file.io listing parcial; 3 arquivos por nome; decrypt de criptografados |
| Pressão | Notificação a clientes/staff; venda a competidores/mídia/fisco |
| Paciência | Aceita log files; timelines de dias; paciente com fim de semana |

## Insights

1. Script intercambiável com Akira/RansomHub
2. Venda a autoridades fiscais como diferencial
3. Aceita log files para test decrypt
4. Operação paciente com timelines de dias
5. Dataset ainda em fase de provas

```
Flexibilidade: N/D | Pressão: Alta | Sofisticação: Média-Alta
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`qilin/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/qilin) |
| **Arquivos típicos** | `README-RECOVER-[rand].txt`, `DtMXQFOCos-RECOVER-README.txt` |
| **Extensão / artefato** | `.qilin / .7z extension variants` |
| **Frases-chave da nota** | *"-- Qilin"*, *"Compromising and sensitive data"*, *"Employees p"* |
| **Continuidade com o chat** | Nota estilo Akira-like; chat oferece 7 entregáveis e ameaça venda a fisco. |

**Se a nota contém...** → confirma **Qilin** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | [`Qilin`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Qilin.md) |
| **Tools-chave** | `Nmap`, `ScreenConnect`, `EDRSandBlast`, `Mimikatz`, `Cobalt Strike`, `Proxychains`, `fsutil`, `EasyUpload`, `Nping`, `PCHunter` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | EasyUpload.io e perfil RTM; chat estilo Akira-like com 7 entregáveis. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Qilin** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
