# Hive — Negotiation Profile (CTI)

> 8 chats, 372 messages. Period: 2021–2022.

---

## Executive Summary

Hive shows a **unique supply-chain negotiation pattern** in the dataset: it categorically refuses to negotiate with downstream SMBs indirectly impacted through an MSP. It redirects these victims to the compromised upstream vendor. Pricing is fixed at $1M with no flexibility.

## Tone and Communication

- **Style:** Formal; inflexible in supply-chain cases
- **Opening:** *"Hello and welcome to Hive. How may I help you?"* -> company identification request
- **Markers:** *"introduce your company first"*, *"our target is [vendor]"*, *"not you, our goal is"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Fixed $1M for primary target; zero flexibility for downstream victims |
| Proof | Verification via corporate email -> protonmail |
| Pressure | Redirects to vendor; limited direct leak pressure |
| Supply-chain | Multiple victims visible in the same chat (cascade effect) |

## Insights

1. Refuses negotiation with indirectly impacted downstream SMBs
2. Multiple victims can appear in the same visible chat context
3. Single fixed price with no flexibility for smaller businesses
4. Uses vendor-accountability narrative consistently
5. Limited direct leak pressure — focus on third-party liability

```
Flexibility: None (downstream) | Pressure: Low | Sophistication: Low
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`hive/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hive) |
| **Typical files** | `HOW_TO_DECRYPT.txt`, `hive.txt` |
| **Extension / artifact** | `.hive` |
| **Key note phrases** | *"network has been breached"*, *"hiveleak... onion"*, *"purchase our decryption software"* |
| **Chat continuity** | Standard leak-site note; formal *How may I help you?* chat refusing downstream SMBs. |

**If the note contains...** → confirms **Hive** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `GMER`, `PCHunter`, `Advanced IP Scanner`, `Bloodhound`, `SoftPerfect NetScan`, `MEGA`, `PrivatLab`, `RClone`, `Sendspace`, `UFile` |
| **Matrices** | [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Supply-chain via MSP; chat refuses downstream SMB negotiations. |

**If these artifacts appear in the environment** → strengthens **Hive** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 8 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
