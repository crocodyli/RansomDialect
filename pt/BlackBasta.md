# BlackBasta — Perfil de Negociação (CTI)

> 5 chats, 257 mensagens. Período: 2023–2024.

---

## Resumo Executivo

BlackBasta opera com **framing de negócio sério** (*"act as a businessman"*). Impaciente com delays percebidos, oferece desconto atrelado a prazo (25% se pagar na semana), e fecha em $150K após oferta inicial de ~$39K.

## Tom e Comunicação

- **Estilo:** Profissional/business-like; impaciente com stalling
- **Abertura:** Chat privado → identificação → volume exfiltrado → preço → 5 garantias pós-pagamento
- **Marcadores:** *"we'll be in touch"*, *"act as a businessman"*, *"Are you seriously?"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Desconto 10–25%; piso rígido (~$150K); rejeita ofertas "meager" |
| Prova | Lista via temp.sh; 3–5 arquivos; decrypt de arquivos "unimportant" |
| Pressão | Publicação em fim de semana; PII específico (SSN, passaportes) |
| Pós-pagamento | Decryptor Windows+Linux; deletion log via qaz.im; relatório (phishing, PtH) |

## Insights

1. Desconto atrelado a prazo (25% na semana)
2. Acusa stalling mesmo com chat offline
3. Fecha em $150K após oferta de ~$39K (~74% desconto)
4. Relatório de segurança pós-pagamento detalhado
5. Tom "businessman" como framing deliberado

```
Flexibilidade: Média | Pressão: Média-Alta | Sofisticação: Alta
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`blackbasta/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackbasta) |
| **Arquivos típicos** | `blackbasta1.txt`, `blackbasta2.txt`, `instructions_read_me.txt` |
| **Extensão / artefato** | `.basta` |
| **Frases-chave da nota** | *"Your data are stolen and encrypted"*, *"company id for log in"*, *"decrypt one file for free"* |
| **Continuidade com o chat** | Nota direta sobre portal Tor; chat adota framing *businessman* e piso ~$150K. |

**Se a nota contém...** → confirma **BlackBasta** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | [`BlackBasta`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/BlackBasta.md) |
| **Tools-chave** | `AdFind`, `AnyDesk`, `Backstab`, `Mimikatz`, `Brute Ratel (BRc4)`, `BITSAdmin`, `Rclone`, `Bloodhound`, `Atera`, `Cobalt Strike` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Qlik/ConnectWise no acesso inicial; chat mantém framing business e piso ~$150K. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **BlackBasta** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`BlackBasta/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/BlackBasta) |
| **TTPs (MITRE)** | [`BlackBasta-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/BlackBasta/BlackBasta-TTP.md) |
| **CVEs** | — |
| **TTPs-chave** | *T1190 — Exploração de appliances expostos (Qlik, ConnectWise)*; *T1219 — RMM (ScreenConnect, RDP) para persistência*; *T1486 — Deploy via GPO / PsExec* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.
