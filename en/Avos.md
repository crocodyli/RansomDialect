# Avos (AvosLocker) — Negotiation Profile (CTI)

> 1 chat, 86 messages. Period: 2021. **Limited dataset.**

---

## Executive Summary

Avos shows a **RaaS staff/affiliate split model**. Central Staff provides "customer support" but delegates key decisions to the affiliate that performed the intrusion. Tone is professional and moderate, distinct from overtly aggressive groups.

## Tone and Communication

- **Style:** Professional, "enterprise client" model + customer support
- **Opening:** *"As you are an enterprise client of ours, we will provide you with customer support"*
- **Markers:** *"Staff"*, *"affiliate"*, *"our terms and we never go against them"*, *"Thank you for your business"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Flexible: $150K -> $100K -> $85K accepted |
| Proof | Manual decrypt via riseup.net/anonfiles (.avos2 unsupported on portal) |
| Pressure | Refuses listing before agreement; blog threat; extendable deadline (Labor Day) |
| Architecture | Central Staff + data-holding affiliate — limits exfiltration proof speed |

## Insights

1. Operator/affiliate separation creates response latency
2. Extends deadline for banking holidays
3. Negotiates in BTC even when landing asks XMR
4. Exceptionally detailed post-payment report (Mimikatz, Forti VPN, Exchange)
5. Patient when victim provides broken links

```
Flexibility: High | Pressure: Medium | Sophistication: Medium
⚠️ Only 1 chat — validate with additional sources
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`avoslocker/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avoslocker) |
| **Typical files** | `avoslocker.txt` |
| **Extension / artifact** | `.avos / .avos2` |
| **Key note phrases** | *"Your files have been encrypted"*, *"do not shutting down your computer"*, *"decryption key & application"* |
| **Chat continuity** | Formal AvosLocker note; chat separates central Staff and RaaS affiliate. |

**If the note contains...** → confirms **Avos** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `LaZagne`, `Mimikatz`, `XenArmor`, `Avast Anti-Rootkit driver`, `NirSoft WinLister`, `Nmap`, `SoftPerfect NetScan`, `FileZilla`, `Gofile[.]io`, `PSCP` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | RaaS Staff/affiliate model mirrors central operator vs. affiliate split in chat. |

**If these artifacts appear in the environment** → strengthens **Avos** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 1 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
