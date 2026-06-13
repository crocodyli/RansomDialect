# Babuk — Negotiation Profile (CTI)

> 2 chats, 150 messages. Period: 2021–2022.

---

## Executive Summary

Babuk combines **technical formality with aggressive legal threats** (GDPR, CEO imprisonment). It explicitly asks about ransomware insurance and uses Zoominfo turnover estimates for pricing. It removes public blog posts as a pre-payment concession.

## Tone and Communication

- **Style:** Formal/technical -> threatening when frustrated
- **Opening:** *"Technical support is ready"* -> asks about recovery company and insurance
- **Markers:** *"reasonable discount"*, *"insurance will pay everything"*, *"any dialogues only in this chat"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Turnover-based (Zoominfo): $400K -> $100K -> $85K |
| Proof | 4–5 files + ecdh_pub_k.bin via file.io/dropmefiles |
| Pressure | GDPR/CEO prison threats; employees' personal photos; 2-day deadline |
| Screening | Asks about insurance and recovery firm before negotiating |

## Insights

1. Explicitly asks whether ransomware insurance exists
2. Removes forum post as pre-payment concession
3. Uses Zoominfo for pricing (with SMB estimation errors)
4. Provides pre-deal technical support (ecdh_pub_k.bin)
5. Demands discussion with owners, not intermediaries

```
Flexibility: Medium-High | Pressure: High | Sophistication: High
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). External source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes).

| Field | Detail |
|-------|--------|
| **Status** | No matching ThreatLabz folder (verified Jun 2026) |
| **Known artifact** | .babuk (conhecido em CTI; sem nota no ThreatLabz) |
| **Alternative attribution** | No ThreatLabz entry — use *Technical support is ready* and insurance screening in chat. |

See [`notes_mapping.json`](../notes_mapping.json) for the full index.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `File[.]io` |
| **Matrices** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Credential theft tools precede cyber insurance screening in chat. |

**If these artifacts appear in the environment** → strengthens **Babuk** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 2 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
