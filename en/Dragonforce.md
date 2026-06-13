# Dragonforce — Negotiation Profile (CTI)

> 14 chats, 375 messages. Period: 2023–2024.

---

## Executive Summary

Dragonforce emphasizes **brand credibility** (*"We're not newbies"*, *"DragonForce, we don't make mistakes"*). It anchors pricing in BTC (not USD), sets a two-week timer, and becomes flexible after victim pushback.

## Tone and Communication

- **Style:** Direct/confident; mildly dismissive
- **Opening:** *"exploring your financial possibilities"* -> list -> BTC price
- **Markers:** *"the bosses"*, temp.sh links, *"losing your reputation would be worse"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | Flexible after pushback; BTC-anchored |
| Proof | Portal test decrypt; 2–3 files from listing |
| Pressure | Two-week timer; reputation pressure as main lever |
| Refusal | Does not decrypt large files as proof |

## Insights

1. References competing factions to reduce victim fear arguments
2. Explicit timer used as publication trigger
3. Short replies in chats without active negotiation
4. Focus on brand credibility over data-volume emphasis
5. Inconsistent party labels (DragonForce / Attacker)

```
Flexibility: Medium | Pressure: Medium | Sophistication: Medium
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`dragonforce/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/dragonforce) |
| **Typical files** | `[rand].README.txt`, `readme.xt` |
| **Extension / artifact** | `.dragonforce` |
| **Key note phrases** | *"files have been stolen... and encrypted"*, *"We work for money"*, *"communication process:"* |
| **Chat continuity** | Structured step-based note; chat anchors on BTC with 2-week timer. |

**If the note contains...** → confirms **Dragonforce** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | [`DragonForce`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/DragonForce.md) |
| **Key tools** | `AdFind`, `ADVobfuscator`, `LaZagne`, `Cobalt Strike`, `PsExec`, `MEGA`, `Advanced IP Scanner`, `Darkside/TrueSight driver (BYOVD)`, `Mimikatz`, `RClone` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Structured kill chain; chat anchors BTC with 2-week timer. |

**If these artifacts appear in the environment** → strengthens **Dragonforce** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`DragonForce/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/DragonForce) |
| **TTPs (MITRE)** | [`DragonForce-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/DragonForce/DragonForce-TTP.md) |
| **CVEs** | — |
| **Key TTPs** | *T1190 — Vetores de acesso expostos*; *T1048 — Exfiltração antes do lock*; *T1486 — Operação RaaS com timer de leak* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 14 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
