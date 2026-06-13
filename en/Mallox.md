# Mallox — Negotiation Profile (CTI)

> 3 chats, 108 messages. Period: 2023.

---

## Executive Summary

Mallox is one of the few groups with **BOT-driven discount automation** in chat. It universally distrusts victim backup claims (*"All customers say so"*). Roles are split across BOT, Support, and Hervios.

## Tone and Communication

- **Style:** Direct; BOT + human operator mix
- **Opening:** Landing-page price; BOT applies % discount with expiration date
- **Markers:** *"Discount X%. Discount expiration date"*, *"I'm not interested in your personal income"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | BOT applies automatic discount; floor around ~$30K from $33.7K |
| Proof | Test file via dropmefiles; delays if technician offline |
| Pressure | Minimal; *"company needs the data, they can pay"* |
| Refusal | Monosyllabic replies (*"no"*) to low offers |

## Insights

1. BOT-based discount automation is rare in this dataset
2. Universally skeptical of backup-restoration claims
3. Frequent intermediary/recovery-firm mediation
4. Partial Chinese/English chat blend
5. Inconsistent naming (Hervios/hiervos)

```
Flexibility: Medium | Pressure: Low | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`mallox/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/mallox) |
| **Typical files** | `FILE RECOVERY.txt`, `HOW TO BACK FILES.txt` |
| **Extension / artifact** | `.mallox / .ma1x0` |
| **Key note phrases** | *"files are encrypted and can not be used"*, *"decrypt one file for free"*, *"Do not try to change or restore files yourself"* |
| **Chat continuity** | Note offers site test decrypt; chat uses BOT with automatic % discount. |

**If the note contains...** → confirms **Mallox** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Dropmefiles`, `File[.]io`, `Sendspace` |
| **Matrices** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Dropmefiles/File.io; chat uses BOT with automatic % discount. |

**If these artifacts appear in the environment** → strengthens **Mallox** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 3 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
