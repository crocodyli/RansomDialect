# RunSomeWares (RSW) — Negotiation Profile (CTI)

> 1 chat, 27 messages. Period: 2025. **Limited dataset.**

---

## Executive Summary

RunSomeWares demonstrates **mature 2025-era TTPs** with a cooperative tone when victims engage seriously. It researches victim reputation/family profile for pricing logic. Timeline flexibility is offered when victims provide a concrete payment date.

## Tone and Communication

- **Style:** Direct/pragmatic; cooperative
- **Opening:** Exhaustive listing -> file proof -> test decrypt
- **Markers:** *"We analized the company's revenue"*, *"most influential family"*, *"Let's get a deal"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Flexible with revenue-based assessment; speed-based discounting |
| Proof | 5 files by name; binary decrypt tests; public share for large files |
| Pressure | *"Your time is up. This is last chance"*; newspaper headline threat |
| Flexibility | Extends timer when victim provides concrete payment date |

## Insights

1. Uses reputation/family research as pricing signal
2. Flexible on timeline when given concrete payment dates
3. Performs binary decryption with text-editor instruction support
4. Cooperative tone during serious engagement
5. Recent chat shows mature negotiation TTP stack

```
Flexibility: Medium-High | Pressure: Medium | Sophistication: High
⚠️ Only 1 chat — validate with additional sources
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). External source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Field | Detail |
|-------|--------|
| **Status** | No matching ThreatLabz folder (verified Jun 2026) |
| **Known artifact** | .RSW (conhecido em CTI; sem nota no ThreatLabz) |
| **Alternative attribution** | No ThreatLabz entry — use *We analized the company's revenue* and cooperative tone in chat. |

See [`notes_mapping.json`](../notes_mapping.json) for the full index.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — hunt/IR during crisis. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Field | Detail |
|-------|--------|
| **Status** | No dedicated RTM entry (Jun 2026) |
| **General checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Revenue OSINT during intrusion; cooperative chat when victim engages. |

Index: [`operational_mapping.json`](../operational_mapping.json)
---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 1 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
