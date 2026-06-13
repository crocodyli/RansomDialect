# trinity — Negotiation Profile (CTI)

> 14 chats, 713 messages.

---

## Executive Summary

trinity uses a **rare per-device pricing model** in this dataset — 0.25 BTC per PC, 0.5 BTC per server. No double extortion is visible in captured chats. It uses prior payments from *"coworkers"* as social proof. Chats are short and negotiation depth is minimal.

## Tone and Communication

- **Style:** Minimalist; dry; transactional
- **Opening:** *"Hi"* -> BTC price per endpoint
- **Markers:** *"Price for decrypt X btc"*, *"we don't work with middlemen"*, proactive host inventory

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Fixed per machine; no discount; cites other payers |
| Proof | 1 file <1MB free; does not decrypt backups |
| Pressure | Minimal; exposes another payer email as social proof |
| Refusal | Categorically rejects intermediaries |

## Insights

1. Per-device model is rare (most groups price per-network)
2. Sends host inventory proactively
3. Uses "coworker" payment examples as social proof
4. No visible double-extortion dynamics in chats
5. Negotiation is nearly absent — mostly direct transaction flow

```
Flexibility: None | Pressure: Low | Sophistication: Low
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`trinity/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/trinity) |
| **Typical files** | `README.txt` |
| **Extension / artifact** | `.trinitylocker` |
| **Key note phrases** | *"TRINITY LOCKER"*, *"helpdesk101@onionmail.com"*, *"download TOR"* |
| **Chat continuity** | Tor/email portal note; chat charges 0.25 BTC per endpoint with no flexibility. |

**If the note contains...** → confirms **trinity** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — hunt/IR during crisis. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Field | Detail |
|-------|--------|
| **Status** | No dedicated RTM entry (Jun 2026) |
| **General checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Operational minimalism; per-endpoint pricing chat with no flexibility. |

Index: [`operational_mapping.json`](../operational_mapping.json)
---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 14 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
