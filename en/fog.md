# fog — Negotiation Profile (CTI)

> 6 chats, 333 messages. Period: 2024–2025.

---

## Executive Summary

fog has one of the **shortest opening scripts** in the dataset (*"hi"* -> RAR list -> price). It delegates decisions to *"bosses"* and shows technical understanding of its own ransomware (`.fog.savepoint`). Tone is cooperative in successful deals.

## Tone and Communication

- **Style:** Casual/minimalist; pragmatic
- **Opening:** *"hi"* -> RAR list -> proof + test decrypt + *"bosses are demanding $X"*
- **Markers:** *"bosses"*, *"Do we work?"*, *"Standing by"*, *"We work with bitcoins"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Flexible with boss approval ($800K -> $715K; ~$150K closed) |
| Proof | 3 encrypted files decrypted; technical knowledge of .fog.savepoint |
| Pressure | Implicit; no aggressive escalation in analyzed chats |
| Post-payment | .exe decryptor for Win/ESXi; refuses split payments |

## Insights

1. One of the shortest openings in the dataset
2. Negotiation mediated through "bosses" as external authority
3. Technical familiarity with own ransomware behavior
4. Cooperative tone when victim seriously engages
5. Shares CSO Online link for BTC acquisition

```
Flexibility: Medium-High | Pressure: Low-Medium | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`fog/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/fog) |
| **Typical files** | `readme.txt`, `readme2.txt` |
| **Extension / artifact** | `.fog` |
| **Key note phrases** | *"We call ourselves Fog"*, *"victim of a cyber attack"*, *"The sooner you contact us"* |
| **Chat continuity** | Minimal note with Fog identity; chat keeps *hi* opening and *bosses* delegation. |

**If the note contains...** → confirms **fog** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `DonPAPI`, `Veeam-Get-Creds`, `Advanced Port Scanner`, `SharpShares`, `SoftPerfect NetScan`, `PsExec`, `Powercat`, `Proxychains`, `Certipy`, `Impacket` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Lean operation; minimalist chat with *bosses* delegation. |

**If these artifacts appear in the environment** → strengthens **fog** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 6 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
