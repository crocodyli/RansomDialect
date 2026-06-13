# Akira — Negotiation Profile (CTI)

> Largest volume in the dataset: 60 chats, 2,408 messages. Period: 2023–2025.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 60 |
| Total messages | 2,408 |
| Actor / victim msgs | 1,193 / 1,215 |
| Avg. actor message length | 154.9 characters |
| Price flexibility | **High** |
| Pressure intensity | **Medium-High** |
| Proof sophistication | **High** |

---

## Executive Summary

Akira operates as a **"technical support company"** with highly standardized scripts. Its surface tone is professional and patient, but pressure escalates through 24h deadlines and onion blog publication. It is one of the most sophisticated groups in financial due diligence and offers the most complete post-payment package in the dataset.

---

## Tone and Communication Style

- **Tone:** Corporate, calm, nearly consultative — similar to an IT helpdesk
- **Persona:** "Akira support" / "surprise security audit"
- **Cadence:** Proactive follow-ups (*"Standing by"*, *"so?"*, *"Waiting for the update"*)
- **Escalation:** Accuses victims of *"playing dirty"* or *"waste our time"* before publishing

**Typical opening:**
> *"Hello. You've reached an Akira support chat. Currently, we are preparing the list of data we took from your network. For now you have to know that dealing with us is the best possible way to settle this quick and cheap."*

Sarcastic variant:
> *"Congratulations, you have passed a surprise information security audit and become a victim of ransomware."*

---

## Negotiation Flow

```
1. "Support chat" opening + request to confirm negotiator authority
2. Delivery of exfiltrated file list (.rar / privnote)
3. Five numbered post-payment services (decryptor, deletion, report, etc.)
4. Financial due diligence (statements, cyber insurance, audits)
5. Test decrypt: 2–3 encrypted files (<=10 MB)
6. Possession proof: 2–3 files from the list on demand
7. Price negotiation with "upper management"
8. BTC payment with test transaction
9. Delivery: CLI decryptor (--secret key), deletion logs, technical report
```

---

## Pricing Strategy

- **Anchoring:** Values from $80K to $2.4M observed in the dataset
- **Flexibility:** High — accepts significant counteroffers (e.g., $2.4M -> $1M, ~58% discount)
- **Modular:** Price can be negotiated in parts (*"whole deal or in parts"*)
- **Levers:** Cyber insurance, victim liquidity, payment speed
- **Tactic:** *"upper management"* as the authority approving discounts

---

## Decryption and Exfiltration Proof

1. Exfiltrated file list via privnote or direct attachment
2. 2–3 uploaded encrypted files returned decrypted
3. 2–3 files from the list as possession proof
4. Delivery of `unlocker.7z` / `unlockers.7z` with CLI instructions

---

## Pressure Tactics

- Publication on onion blog after prolonged silence
- 24h response deadline
- Bad-faith accusation: *"Your attempts to waste our time could force our exit"*
- Publishes **before** agreement if victim delays
- Threat of uploading additional data

---

## Negotiation-Phase TTPs

- Active financial due diligence (requests statements, insurance policy)
- BTC test transaction before full payment
- Detailed post-payment report (kerberoasting, Forti VPN, etc.)
- Deletion logs delivered in .rar
- Decryptor with explicit `--secret` parameter

---

## Behavioral IOCs (Linguistic Indicators)

| Indicator | Example |
|-----------|---------|
| `>` prefix in messages | `> Standing by.` |
| "support chat" | Standard opening |
| "dealing with us is the best possible way" | Opening script |
| "whole deal or in parts" | Modular negotiation |
| "please wait" / "wait a bit" | 23+ occurrences in dataset |
| "are you going to work with us?" | Engagement pressure |
| Cyber insurance references | Due diligence |
| privnote.com links | List delivery |

---

## Critical Insights

1. **Script reused across years** — identical phrases in 2023 and 2025 chats
2. **"Upper management"** is likely a rhetorical lever, not necessarily real hierarchy
3. **Pre-deal publication** is used as delay punishment — does not wait for full negotiation failure
4. **Highest proactive follow-up rate** in the dataset — operator does not wait for victim response
5. **Discounts up to 58%** when victims document limited liquidity

---

## Classification

```
Style:         Corporate-Professional
Flexibility:   High
Pressure:      Medium-High
Sophistication: High
Maturity:      Very High (2023–2025)
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`akira/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/akira) |
| **Typical files** | `akira_readme.txt`, `akira_readme_2.txt`, `akira_readme_3.txt` |
| **Extension / artifact** | `.akira` |
| **Key note phrases** | *"surprise information security audit"*, *"internal infrastructure... fully or partially dead"*, *"backups... completely removed"* |
| **Chat continuity** | Same technical-support persona; the note announces exfiltration and backup destruction before the chat portal. |

**If the note contains...** → confirms **Akira** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | [`Akira`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Akira.md) |
| **Key tools** | `Advanced IP Scanner`, `AnyDesk`, `PowerTool`, `DonPAPI`, `Impacket`, `Cloudflared`, `FileZilla`, `Masscan`, `MobaXterm`, `Zemana Anti-Rootkit` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | RClone/temp.sh during intrusion explain privnote and exfil lists in chat. |

**If these artifacts appear in the environment** → strengthens **Akira** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`Akira/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/Akira) |
| **TTPs (MITRE)** | [`Akira-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Akira/Akira-TTP.md) |
| **CVEs** | [`CVEs`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Akira/CVEs-Akira.md) |
| **Key TTPs** | *T1190 — Exploração de VPN/edge (Cisco, SonicWall)*; *T1133 — Acesso remoto com credenciais roubadas*; *T1486 — Criptografia + exfiltração pré-ransom* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 60 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
