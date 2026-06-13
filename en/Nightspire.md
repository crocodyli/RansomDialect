# Nightspire — Negotiation Profile (CTI)

> 7 chats, 367 messages. Period: 2025–2026.

---

## Executive Summary

Nightspire reflects a **new-generation negotiation model** — using public filings (revenue $14.8M, profit $2.1M) to anchor pricing. It escalates aggressively when victims mention FBI (*"FBI won't stop your board"*). Focus is on downtime cost plus contractual penalties ($500K+).

## Tone and Communication

- **Style:** Aggressive/professional; public financial OSINT-oriented
- **Opening:** Direct pricing ($100K–$150K BTC) + sensitive-data detailing
- **Markers:** *"We already researched your company"*, *"Public filings show"*, *"FBI won't stop your board"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Incrementally flexible ($100K -> $90K -> $135K -> $110K); linked to revenue/profit ratios |
| Proof | Listing via gofile.io; contract/PII samples as pressure |
| Pressure | Contractual penalties; SEC exposure; competitor spam; dark web markets |
| Escalation | FBI/authority mentions increase aggressiveness |

## Insights

1. Uses public-filing OSINT (10-K style) for pricing logic
2. Aggressively escalates on law-enforcement mentions
3. Small concessions (~10%) framed as "goodwill"
4. Emphasizes downtime + contractual penalties
5. More sophisticated tone than typical 2020–2021 groups

```
Flexibility: Medium | Pressure: Very High | Sophistication: Medium-High
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`nightspire/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/nightspire) |
| **Typical files** | `nightspire_readme.txt`, `[NSPIRE_MSG].txt`, `readme.txt` |
| **Extension / artifact** | `.nspire / .nightspire` |
| **Key note phrases** | *"sensetive data are stolen and encrypted"*, *"pay within 3 days"*, *"DO NOT USE THIRD PARTY SOFTWARE"* |
| **Chat continuity** | 3-day deadline note; chat escalates with 10-K filing OSINT and FBI mentions. |

**If the note contains...** → confirms **Nightspire** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Everything.exe`, `MEGA`, `WinSCP` |
| **Matrices** | [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Pre-lock exfiltration; chat escalates with 10-K filing OSINT. |

**If these artifacts appear in the environment** → strengthens **Nightspire** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 7 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
