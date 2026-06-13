# BlackBasta — Negotiation Profile (CTI)

> 5 chats, 257 messages. Period: 2023–2024.

---

## Executive Summary

BlackBasta operates with **serious-business framing** (*"act as a businessman"*). It is impatient with perceived delays, offers deadline-linked discounts (25% if paid within the week), and closes at $150K after an initial offer around $39K from the victim side.

## Tone and Communication

- **Style:** Professional/business-like; impatient with stalling
- **Opening:** Private chat -> identification -> exfil volume -> price -> five post-payment guarantees
- **Markers:** *"we'll be in touch"*, *"act as a businessman"*, *"Are you seriously?"*

## Negotiation

| Aspect | Behavior |
|--------|----------|
| Price | 10–25% discount; hard floor (~$150K); rejects "meager" offers |
| Proof | List via temp.sh; 3–5 files; decrypt of "unimportant" files |
| Pressure | Weekend publication; specific PII (SSN, passports) |
| Post-payment | Windows+Linux decryptor; deletion log via qaz.im; report (phishing, PtH) |

## Insights

1. Deadline-linked discounting (25% within the week)
2. Accuses victims of stalling even when chat is offline
3. Closes at $150K after ~$39K offer (~74% spread)
4. Detailed post-payment security report
5. "Businessman" framing is deliberate positioning

```
Flexibility: Medium | Pressure: Medium-High | Sophistication: High
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`blackbasta/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackbasta) |
| **Typical files** | `blackbasta1.txt`, `blackbasta2.txt`, `instructions_read_me.txt` |
| **Extension / artifact** | `.basta` |
| **Key note phrases** | *"Your data are stolen and encrypted"*, *"company id for log in"*, *"decrypt one file for free"* |
| **Chat continuity** | Direct Tor portal note; chat adopts *businessman* framing and ~$150K floor. |

**If the note contains...** → confirms **BlackBasta** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | [`BlackBasta`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/BlackBasta.md) |
| **Key tools** | `AdFind`, `AnyDesk`, `Backstab`, `Mimikatz`, `Brute Ratel (BRc4)`, `BITSAdmin`, `Rclone`, `Bloodhound`, `Atera`, `Cobalt Strike` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Qlik/ConnectWise initial access; chat keeps businessman framing and ~$150K floor. |

**If these artifacts appear in the environment** → strengthens **BlackBasta** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> Pre-extortion TTPs, CVEs, and history. Source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **Folder** | [`BlackBasta/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/BlackBasta) |
| **TTPs (MITRE)** | [`BlackBasta-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/BlackBasta/BlackBasta-TTP.md) |
| **CVEs** | — |
| **Key TTPs** | *T1190 — Exploração de appliances expostos (Qlik, ConnectWise)*; *T1219 — RMM (ScreenConnect, RDP) para persistência*; *T1486 — Deploy via GPO / PsExec* |

Cross-reference with [ransomware.live](https://www.ransomware.live/) and RTM matrix.

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 5 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
