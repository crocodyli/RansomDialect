# Qilin — Negotiation Profile (CTI)

> 2 chats, 39 messages. Period: 2024–2025.

---

## Executive Summary

Qilin uses a **script that is nearly interchangeable with Akira/RansomHub** — 7 post-payment deliverables, file tree evidence, 3 proof files, plus 3 test decrypt samples. Its differentiator is threat of selling data to **tax authorities**.

## Tone and Communication

- **Style:** Professional/standardized; patient
- **Opening:** 7 post-payment deliverables -> file tree -> proofs
- **Markers:** *"forget about us forever"*, *"activation key"*, *"On Monday we are waiting"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Not detailed in captured chats (proof-first pattern) |
| Proof | Partial listing via file.io; 3 named files; encrypted-file decrypt tests |
| Pressure | Notification to clients/staff; sale to competitors/media/tax authorities |
| Patience | Accepts log files; multi-day timelines; patient across weekends |

## Insights

1. Script is highly interchangeable with Akira/RansomHub patterns
2. Threat of sale to tax authorities is a distinct pressure differentiator
3. Accepts log files for decryption testing
4. Patient operational pacing with multi-day timelines
5. Dataset stage is still proof-heavy rather than price-round-heavy

```
Flexibility: N/A | Pressure: High | Sophistication: Medium-High
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`qilin/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/qilin) |
| **Typical files** | `README-RECOVER-[rand].txt`, `DtMXQFOCos-RECOVER-README.txt` |
| **Extension / artifact** | `.qilin / .7z extension variants` |
| **Key note phrases** | *"-- Qilin"*, *"Compromising and sensitive data"*, *"Employees p"* |
| **Chat continuity** | Akira-like note style; chat offers 7 deliverables and tax-authority sale threat. |

**If the note contains...** → confirms **Qilin** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | [`Qilin`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Qilin.md) |
| **Key tools** | `Nmap`, `ScreenConnect`, `EDRSandBlast`, `Mimikatz`, `Cobalt Strike`, `Proxychains`, `fsutil`, `EasyUpload`, `Nping`, `PCHunter` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | EasyUpload.io and RTM profile; Akira-like chat with 7 deliverables. |

**If these artifacts appear in the environment** → strengthens **Qilin** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 2 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
