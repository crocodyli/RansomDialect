# Darkside — Negotiation Profile (CTI)

> 5 chats, 425 messages. Period: 2020–2021.

---

## Executive Summary

Darkside was an early **capital-market pressure pioneer** — threatening to contact traders to short victim stock. It customizes openings with company name, cyber insurance details (Beazley), credit lines, and NASDAQ references. Tone is cold and calculated.

## Tone and Communication

- **Style:** Professional/cold; threatening with detailed financial intel
- **Opening:** Personalized greeting + financial intelligence + exfil volume
- **Markers:** *"Are you ready for a dialog?"*, *"we always do what was promised"*, *"your liquidity allows"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Rigid; $10M initial; only 24h time-based discount |
| Proof | Free decrypt test via portal; returned file with rename instructions |
| Pressure | Forbes, NYT, Bloomberg; short sellers; staged publication |
| OSINT | Beazley, Response Limit, specific policy intelligence |

## Insights

1. Pioneer in capital-market pressure (short sellers)
2. Requires a concrete proposal to extend timer
3. Knows specific cyber insurance policy details
4. Can monologue when victim is unresponsive
5. Discounts tied to speed, not true affordability

```
Flexibility: Low | Pressure: Very High | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`darkside/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/darkside) |
| **Typical files** | `darkside.txt` |
| **Extension / artifact** | `.darkside` |
| **Key note phrases** | *"Welcome to DarkSide"*, *"universal decryptor"*, *"backups are deleted"* |
| **Chat continuity** | Cold direct note; chat escalates with financial OSINT and media threats. |

**If the note contains...** → confirms **Darkside** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Mimikatz`, `SessionGopher`, `Darkside/TrueSight driver (BYOVD)`, `ADRecon`, `AdFind`, `Advanced IP Scanner`, `SoftPerfect NetScan`, `Bashupload`, `MEGA`, `pCloud` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Bashupload/exfil tools; chat escalates financial OSINT and media threats. |

**If these artifacts appear in the environment** → strengthens **Darkside** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 5 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
