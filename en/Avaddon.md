# Avaddon — Negotiation Profile (CTI)

> 7 chats, 380 messages. Period: 2021.

---

## Executive Summary

Avaddon combines **surface-level professionalism with real aggressiveness**. It uses sarcasm (*":D"*, *"Tick tock tick tock"*), rapidly escalates emotionally after refusal, and applies aggressive time-based discounts (15% -> 50%). It has a unique geographic policy: CIS targets get free decryptor access.

## Tone and Communication

- **Style:** Casual-professional -> sarcastic/aggressive under pressure
- **Opening:** *"You have been infected by the Avaddon ransomware. Price for you is $X"*
- **Markers:** *"We are a serious organization"*, *"Guys?"*, *"take a loan"*, *"Tick tock"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Rigid with time-based discount steps; asks *"How much can you offer?"* |
| Proof | Test Decryption on landing (<=2MB); General Decryptor for full network |
| Pressure | Blog, third-party spam, website DDoS, lawsuits, countdown |
| Flexibility | Medium — time-based discounts yes, value negotiation limited |

## Insights

1. Uses chat history against victims who backtrack (*"you wrote it"*)
2. Emotional escalation can happen within minutes after refusal
3. **Policy exception:** CIS targets = free decryptor
4. Does not negotiate per-file recovery — only General Decryptor
5. Overnight follow-ups (*"Guys?"* at 05:20)

```
Flexibility: Medium | Pressure: High | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`avaddon/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avaddon) |
| **Typical files** | `avaddon.txt` |
| **Extension / artifact** | `{{ext}} (variável por campanha)` |
| **Key note phrases** | *"Your network has been infected!"*, *"DO NOT DELETE THIS FILE"*, *"General Decryptor"* |
| **Chat continuity** | Aggressive note tone escalates to sarcasm and *Tick tock* in chat. |

**If the note contains...** → confirms **Avaddon** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Mimikatz`, `SharpDump`, `GMER`, `PowerTool`, `TDSSKiller`, `SoftPerfect NetScan`, `Anonfiles`, `MEGA`, `ProtonMail`, `Sendspace` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | DDoS and third-party spam in operations align with emotional escalation in chat. |

**If these artifacts appear in the environment** → strengthens **Avaddon** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 7 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
