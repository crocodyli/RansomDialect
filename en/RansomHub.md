# RansomHub — Negotiation Profile (CTI)

> 1 chat, 1 message. Period: 2024. **Incomplete profile.**

---

## Executive Summary

The dataset is **insufficient for a full profile**. The only captured message is an automated FAQ template with no human dialogue. Format suggests automated onboarding similar to Qilin/Akira patterns.

## Captured Content

**FAQ template:**
- *"What happened?"* — list of compromised data categories
- *"What if I decline?"* — social media exposure, leak site, lawsuits, permanent halt

## What is NOT present in the dataset

- Price
- Decrypt proof
- Any type of negotiation round
- Response to victim questions

## Insights (template-based)

1. FAQ format suggests automated onboarding workflow
2. Emphasizes legal/reputational consequences over technical details
3. Likely abandoned or truncated chat capture
4. Script likely similar to Qilin (7-deliverable model)
5. **Validate with additional CTI sources before operational use**

```
Flexibility: N/A | Pressure: High (template only) | Sophistication: N/A
⚠️ INCOMPLETE PROFILE — only 1 message
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`ransomhub/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ransomhub) |
| **Typical files** | `readme_[id].txt`, `readme_[id]_2.txt` |
| **Extension / artifact** | `.ransomhub` |
| **Key note phrases** | *"Visit our Blog"*, *"Your data is stolen and encrypted"*, *"TOR darknet"* |
| **Chat continuity** | Note is FAQ template; only captured chat is also automated template. |

**If the note contains...** → confirms **RansomHub** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Mimikatz`, `BadRentdrv2`, `ThreatFire System Monitor driver (BYOVD)`, `Angry IP Scanner`, `Nmap`, `SoftPerfect NetScan`, `WKTools`, `PSCP`, `RClone`, `WinSCP` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | RMM common in precursor; chat is automated FAQ template. |

**If these artifacts appear in the environment** → strengthens **RansomHub** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`RansomHub/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/RansomHub) |
| **TTPs (MITRE)** | [`RansomHub-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/RansomHub/RansomHub-TTP.md) |
| **CVEs** | — |
| **Key TTPs** | *T1190 — Initial access via afiliados*; *T1219 — RMM comum no kill chain*; *T1486 — Modelo RaaS com leak site* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 1 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
