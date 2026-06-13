# Cloak — Negotiation Profile (CTI)

> 2 chats, 120 messages. Period: 2023.

---

## Executive Summary

Cloak has the **most procedural formalization in the dataset**: 6 rules plus an 11-step plan before any pricing discussion. It enforces authority gatekeeping (*"authorized representative"*) and uses third-party data sale as an alternative pressure model to public leak publication.

## Tone and Communication

- **Style:** Formal/procedural — operational playbook format
- **Opening:** Long rules-and-steps message before pricing
- **Markers:** *"Anonymous"* / *"Client"*, *"authorized representative"*, *"mutual respect is the key"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Not disclosed until authorized representative is validated; *"we know about your income"* |
| Proof | Steps 3–5: 2 files <=5MB for reverse decryption |
| Pressure | Sale to third parties with timer; onion leak-site samples |
| Gatekeeping | Refuses admins or cleanup teams as negotiators |

## Insights

1. Highest procedural formalization in the dataset
2. Third-party sale used as alternative pressure vector
3. Categorically refuses unauthorized negotiators
4. Multiple domains/companies can appear in the same chat
5. Process-first mindset over outcome speed

```
Flexibility: Low | Pressure: High | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`cloak/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/cloak) |
| **Typical files** | `readme_for_unlock.txt`, `readme_for_unlock_oct2024.txt`, `readme_for_unlock_nov2024.txt` |
| **Extension / artifact** | `.cloak / .pwned` |
| **Key note phrases** | *"ATTENTION"*, *"network is hacked and files are encrypted"*, *"accounting and other internal documentation"* |
| **Chat continuity** | Note lists exfiltration; chat enforces 6 rules + 11 steps before pricing. |

**If the note contains...** → confirms **Cloak** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — hunt/IR during crisis. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Field | Detail |
|-------|--------|
| **Status** | No dedicated RTM entry (Jun 2026) |
| **General checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | No dedicated RTM matrix; procedural chat (6 rules + 11 steps) is the main IOC. |

Index: [`operational_mapping.json`](../operational_mapping.json)
---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 2 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
