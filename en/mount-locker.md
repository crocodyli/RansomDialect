# MountLocker — Negotiation Profile (CTI)

> 1 chat, 60 messages. Period: 2020. **Limited dataset.**

---

## Executive Summary

MountLocker uses a **legal framework as its primary pressure vector** — class-action lawsuits (including ZDNet reference), and legal-loss comparisons. Tone is polite (*"Sincerely, yours"*) but firm. It rejects COVID/wildfire arguments.

## Tone and Communication

- **Style:** Professional/corporate; legal-financial argumentation
- **Opening:** *"Greetings! We are ready to help you!"* -> good/bad scenario -> $9M -> 1TB exfiltrated
- **Markers:** *"businessmans"*, *"Sincerely, yours"*, password-protected chat option

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Rigid ($9M); expects offer between 5–50% of demand |
| Proof | <=5MB test decrypt file; sample via privatlab |
| Pressure | Class-action risk; detailed PII exposure; onion blog; timer |
| OSINT | References estimated revenue (~$1B) to justify demand |

## Insights

1. Legal framework is the main pressure vector
2. Dismisses COVID/wildfire arguments as irrelevant
3. Expects 5–50% counteroffers, not 90% reductions
4. Politer tone than average 2020 groups
5. Offers password-protected chat channel

```
Flexibility: Low-Medium | Pressure: High | Sophistication: High
⚠️ Only 1 chat — validate with additional sources
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). External source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Field | Detail |
|-------|--------|
| **Status** | No matching ThreatLabz folder (verified Jun 2026) |
| **Known artifact** | .mount-locker (conhecido em CTI; sem nota no ThreatLabz) |
| **Alternative attribution** | No ThreatLabz entry — use legal framework and *Greetings! We are ready to help you!* in chat. |

See [`notes_mapping.json`](../notes_mapping.json) for the full index.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `MEGA` |
| **Matrices** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Few catalogued tools; chat uses legal framework as pressure. |

**If these artifacts appear in the environment** → strengthens **mount-locker** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 1 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
