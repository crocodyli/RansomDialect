# BlackMatter — Negotiation Profile (CTI)

> 2 chats, 121 messages. Period: 2021.

---

## Executive Summary

BlackMatter uses **sarcastic humor to mask a sophisticated operation**. It demonstrates intimate real-time knowledge of victim infrastructure (destroyed Rubrik, Sunday restore attempts). It also suspects researchers unless clear affiliation proof is provided.

## Tone and Communication

- **Style:** Sarcastic/casual with a professional layer
- **Opening:** *"Hello and welcome to BlackMatter. How may I help you?"* -> immediate $15M demand
- **Markers:** *"virustotal.com"*, *"good pentest"*, *"time is on our side"*, *"Oh [redacted] you so clever)"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Seven-figure floor; quick 10% discount; rejects conditional offers |
| Proof | Screenshots (ibb.co) of hashes; samples via privatlab; DB lists |
| Pressure | Intimate infrastructure knowledge; compares victim with competitor case |
| Verification | Mandatory: domain, admin identity, backup software |

## Insights

1. Suspects researchers/curious parties without affiliation proof
2. Tracks operational details in near real time
3. Compares with other victims in the same sector
4. Informal tone hides high operational sophistication
5. Refuses structured negotiation by data category

```
Flexibility: Medium | Pressure: Medium | Sophistication: High
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`blackmatter/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackmatter) |
| **Typical files** | `blackmatter.txt` |
| **Extension / artifact** | `.blackmatter / .pay2key` |
| **Key note phrases** | *"BLACK ... Matter"*, *"How may I help you?"*, *"universal decryptor"* |
| **Chat continuity** | ASCII art in note; chat keeps sarcasm and real-time infra awareness. |

**If the note contains...** → confirms **BlackMatter** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `PrivatLab` |
| **Matrices** | [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Typical Impacket/Mimikatz; chat uses sarcasm and live infra awareness. |

**If these artifacts appear in the environment** → strengthens **BlackMatter** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 2 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
