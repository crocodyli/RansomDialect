# NoEscape — Negotiation Profile (CTI)

> 2 chats, 10 messages. Period: 2023. **Very limited dataset.**

---

## Executive Summary

NoEscape shows a **polite tone contrasted with legal pressure** (*"Hello sir"*, *"your silence will only worsen"*). The dataset contains no captured price negotiation — focus remains on portal-based test decrypt and automated publication after timer expiration.

## Tone and Communication

- **Style:** Formal/polite
- **Opening:** Identification + price (~$80K) + test decrypt instructions (<=5MB)
- **Markers:** *"Hello sir"*, *"Can i help you?"*, onion blog link

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Not negotiated in available chats |
| Proof | Test decryptor only through landing page |
| Pressure | Blog press release; 24h *"last warning"*; legal actions |
| Behavior | Pressure monologue without victim response |

## Insights

1. No captured price negotiation rounds
2. Polite tone combined with legal pressure
3. Portal-first operation, chat-secondary behavior
4. Publishes without dialogue if victim remains silent
5. Possibly an Avaddon/Hive-style successor pattern

```
Flexibility: N/A | Pressure: Medium-High | Sophistication: Low
⚠️ Only 2 chats with no negotiation — incomplete profile
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`noescape/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/noescape) |
| **Typical files** | `HOW_TO_RECOVER_FILES.txt`, `HOW_TO_RECOVER_FILES_no_personal_id.txt` |
| **Extension / artifact** | `.noescape` |
| **Key note phrases** | *"HOW TO RECOVER FILES"*, *"personal id"*, *"DO NOT MODIFY FILES"* |
| **Chat continuity** | Formal note with personal ID; polished chat with portal test decrypt. |

**If the note contains...** → confirms **NoEscape** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — hunt/IR during crisis. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Field | Detail |
|-------|--------|
| **Status** | No dedicated RTM entry (Jun 2026) |
| **General checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | No RTM entry; formal chat with portal test decrypt. |

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
