# LockBit 3.0 — Negotiation Profile (CTI)

> Third largest volume: 42 chats, 2,220 messages. Period: 2022–2025.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 42 |
| Total messages | 2,220 |
| Actor / victim msgs | 1,313 / 907 |
| Avg. actor message length | ~50 characters (smallest in dataset) |
| Price flexibility | **Variable** (by target size) |
| Pressure intensity | **Medium-High** |
| Proof sophistication | **High** |

---

## Executive Summary

LockBit 3.0 has the **shortest responses in the dataset** — often a single line. The tone is robotic, direct, and dismissive. It adapts price drastically to target size (Entrust: $8M vs SMB: $100K). It operates its own infrastructure (onion FSS, blog) and shows mature RaaS operational automation.

---

## Tone and Communication Style

- **Tone:** Terse, robotic, dismissive when challenged
- **Persona:** Efficient operator with no interest in rapport
- **Cadence:** One-line replies; rarely explains or elaborates
- **Irony:** Especially toward security companies (*"Do google lockbit"*)

**Typical opening:**
> *"hello! pay for key! after payment you will be able to restore your operations."*

Or automated test-decrypt instructions.

---

## Negotiation Flow

```
1. Monosyllabic opening with price or payment instruction
2. 10% listing with password (partial exfiltration download)
3. Onion FSS for files >10MB
4. Test decrypt in chat (encrypted file upload)
5. Minimal negotiation - limited discount (~15%)
6. "last price" as ultimatum
7. Payment -> decryptor + deletion confirmation
```

---

## Pricing Strategy

- **Enterprise:** $8M (Entrust) -> 15% discount = $6.8M
- **Mid-market:** $120K -> $100K
- **SMB:** Lower values with little negotiation
- **Typical phrase:** *"you can afford"* — based on financial OSINT
- **Discount:** Limited (~15%) for enterprise; *"last price"* as hard ceiling
- **Special case:** In some Leaked2025 chats, negotiates deletion only (no decryptor)

---

## Decryption and Exfiltration Proof

1. 10% listing with password-protected download
2. Proprietary onion File Sharing Service (FSS) for large files
3. Direct test decrypt in chat
4. Massive data proof — full download availability in Leaked2025 chats

---

## Pressure Tactics

- Irony toward cyber/security firms
- Threat of publication on leak blog
- *"our principles have become worth more than money"* — refusal to negotiate "on principle"
- *"last price"* as no-margin ultimatum
- Criminal reputation leverage (*"Do google lockbit"*)

---

## Negotiation-Phase TTPs

- Proprietary infrastructure: onion FSS, blog, payment portal
- Temporary blog takedown as concession
- Test decrypt automation
- Price adaptation by target size (OSINT-driven)
- In some cases: data-deletion-only negotiation, no decryptor

---

## Behavioral IOCs

| Indicator | Example |
|-----------|---------|
| "hello! pay for key!" | One-line opening |
| "Do google lockbit" | Reputation proof |
| "last price" | Ultimatum |
| "you can afford" | Financial OSINT |
| Onion FSS links | Proprietary infrastructure |
| Replies under 50 characters | Robotic style |

---

## Critical Insights

1. **Smallest average message size** in the dataset — efficiency over relationship building
2. **80x pricing spread** between enterprise ($8M) and SMB ($100K)
3. **Massive data-proof pattern** in Leaked2025 chats — full download available
4. **Limited discounting** (~15%) — less flexible than Conti/Akira
5. **Dismissive toward financial excuses** — monosyllabic rejection replies

---

## Classification

```
Style:         Minimalist-Transactional
Flexibility:   Variable (by target size)
Pressure:      Medium-High
Sophistication: High
Maturity:      Very High (mature RaaS)
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`lockbit/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/lockbit) |
| **Typical files** | `lockbit3.txt`, `[rand].README.txt`, `ReadMeForDecrypt.txt` |
| **Extension / artifact** | `.lockbit3 / .abcd` |
| **Key note phrases** | *"LockBit 3.0 the world's fastest"*, *"Your data is stolen and encrypted"*, *"TOR darknet sites"* |
| **Chat continuity** | LockBit 3.0 branding note; chat reduces to *hello! pay for key!*. |

**If the note contains...** → confirms **lockbit3.0** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Gosecretsdump`, `LaZagne`, `LostMyPassword`, `Mimikatz`, `NirSoft ExtPassword`, `PasswordFox`, `ProcDump`, `Veeam-Get-Creds`, `Backstab/Process Explorer driver (BYOVD)`, `Defender Control` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Massive Cobalt Strike/RMM; chat reduces to *hello! pay for key!*. |

**If these artifacts appear in the environment** → strengthens **lockbit3.0** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`LockBit/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/LockBit) |
| **TTPs (MITRE)** | [`LockBit-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/LockBit/LockBit-TTP.md) |
| **CVEs** | — |
| **Key TTPs** | *T1190 — Exploração massiva de CVEs (Fortinet, Exchange, etc.)*; *T1219 — RMM e Cobalt Strike no precursor*; *T1486 — LockBit 3.0 builder / afiliados* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 42 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
