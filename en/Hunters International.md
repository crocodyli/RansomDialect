# Hunters International — Negotiation Profile (CTI)

> 1 chat, 29 messages. Period: 2024. **Limited dataset.**

---

## Executive Summary

One of the **most inflexible operators in the dataset**. Pure *"take it or leave it"* model: *"I'm okay to get nothing"*, *"We are not in a hurry"*. Explicitly rejects $1.5M and $4M counteroffers against a $10M demand.

## Tone and Communication

- **Style:** Cold/minimalist; ultimatum-driven
- **Opening:** *"Hi, how may I assist you?"* -> confirms 2.79M files, 2.3 TB
- **Markers:** *"I'm okay to get nothing"*, *"price is final"*, *"each case is unique"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Rigid ($10M); discount only for "small companies" |
| Proof | Decrypt proof in ~20 min; file tree confirmation |
| Pressure | Mass email to competitors/partners/customers |
| Refusal | $1.5M and $4M explicitly rejected |

## Insights

1. Among the least flexible groups in the dataset
2. Rejects substantial offers without counterproposal
3. Uses victim history but refuses comparison logic
4. Fast technical proof turnaround (~20 min)
5. Waits for banking availability rather than accepting available BTC

```
Flexibility: Very Low | Pressure: High | Sophistication: Medium
⚠️ Only 1 chat — validate with additional sources
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`hunters/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hunters) |
| **Typical files** | `READ ME NOW!.txt`, `Contact Us.txt`, `Contact Us2.txt` |
| **Extension / artifact** | `.hunters (variantes)` |
| **Key note phrases** | *"HUNTERS INTERNATIONAL group"*, *"military-grade AES"*, *"large amount of sensitive data was exfiltrated"* |
| **Chat continuity** | Ultimatum note; chat confirms inflexibility (*I'm okay to get nothing*). |

**If the note contains...** → confirms **Hunters International** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Advanced IP Scanner`, `Advanced Port Scanner`, `RClone`, `WinSCP` |
| **Matrices** | [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Ultimatum operation from intrusion; chat confirms total inflexibility. |

**If these artifacts appear in the environment** → strengthens **Hunters International** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`Hunters International/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/Hunters%20International) |
| **TTPs (MITRE)** | [`Hunters International-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Hunters%20International/Hunters%20International-TTP.md) |
| **CVEs** | — |
| **Key TTPs** | *T1190 — Acesso inicial via serviços expostos*; *T1486 — AES + double extortion*; *T1490 — Inibição de recovery/backup* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 1 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
