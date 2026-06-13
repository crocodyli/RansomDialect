# Ranzy — Negotiation Profile (CTI)

> 2 chats, 56 messages. Period: 2020–2021.

---

## Executive Summary

Ranzy is one of the **simplest groups in the dataset** — a "smash and grab" model with no visible double extortion. Replies are typically 1–3 words, with fixed pricing ($7,000), no decrypt proof, and no negotiation dynamics.

## Tone and Communication

- **Style:** Minimalist/casual
- **Opening:** *"hi"* -> *"price for your case is $7,000"*
- **Markers:** howtobuybitcoins.info, *"yes correct address"*, *"ok, without discount"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Fixed; no discount; no negotiation |
| Proof | None |
| Pressure | No explicit pressure tactics |
| Payment | Direct BTC wallet; refuses address changes |

## Insights

1. No visible double extortion behavior
2. No decrypt proof or exfiltration listing
3. No discount or value negotiation patterns
4. 1–3 word response pattern dominates
5. Represents a primitive 2020–2021 ecosystem phase

```
Flexibility: None | Pressure: Low | Sophistication: None
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`ranzy/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ranzy) |
| **Typical files** | `ranzy.txt` |
| **Extension / artifact** | `.ranzy` |
| **Key note phrases** | *"Your servers is LOCKED"*, *"eviluser@tutanota.com"*, *"personal id:"* |
| **Chat continuity** | Minimal email-based note; chat confirms fixed $7K price without double extortion. |

**If the note contains...** → confirms **Ranzy** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `UFile` |
| **Matrices** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Smash-and-grab operation; chat fixes $7K without double extortion. |

**If these artifacts appear in the environment** → strengthens **Ranzy** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 2 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
