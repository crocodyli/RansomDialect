# Conti — Negotiation Profile (CTI)

> Second largest volume: 32 chats, 1,709 messages. Period: 2021–2022.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 32 |
| Total messages | 1,709 |
| Actor / victim msgs | ~850 / ~859 |
| Price flexibility | **High** |
| Pressure intensity | **High** |
| Proof sophistication | **High** |

---

## Executive Summary

Conti represents the peak of **ransomware professionalization** in the 2021–2022 era. It uses legal-commercial language (*"we are businessmen"*, *"contract with us"*), leverages exfiltrated cyber insurance documents as pricing input, and closes deals at significant fractions of the initial demand. It explicitly frames recovery firms as a 10–50% markup.

---

## Tone and Communication Style

- **Tone:** Corporate, assertive, occasionally aggressive
- **Persona:** Authorized negotiator with hierarchical limits (*"I am not authorized"*)
- **Framing:** A legitimate business transaction, not crime
- **Documentation:** Long, legal "contract" style text in the opening

**Typical opening:**
> Attack summary + BTC/USD price + 30% exfiltration datapack + free test decrypt offer.

---

## Negotiation Flow

```
1. Attack summary + initial price (often $500K–$920K)
2. Datapack delivery (30% listing) + sample
3. Test decrypt: 2 victim-selected files, free
4. Descending price ladder negotiation
5. 25% discount for payment within 2 business days
6. Temporary blog removal (24h) as concession
7. BTC payment -> decryptor + full package delivery
```

---

## Pricing Strategy

- **Aggressive anchoring:** $920K observed as initial demand
- **Documented descending ladder:** $920K -> $600K -> $350K -> $255K -> **$172K accepted**
- **Close rate:** ~19% of initial demand
- **Time-based discount:** 25% for payment within 2 business days
- **Insurance factor:** Uses exfiltrated cyber insurance policy to calibrate price
- **Anti-intermediary:** *"recovery companies add 10-50%"* — discourages external negotiators

---

## Decryption and Exfiltration Proof

1. Datapack with 30% of exfiltrated file listing
2. 2 victim-selected files decrypted for free
3. References dark-market value (~$500B) to contextualize data value

---

## Pressure Tactics

- Partial publication of 1–3% of data within 3 days
- Exposure of victim cyber insurance policy
- Publication of victims negotiating too slowly
- Threat of data auction/sale on dark markets
- Strict countdown timer

---

## Negotiation-Phase TTPs

- Active analysis of exfiltrated cyber insurance data
- Temporary 24h blog takedown during active talks
- Full post-payment package (decryptor, deletion, report)
- Engagement with lawyers and recovery firms
- Staged publication by data type

---

## Behavioral IOCs

| Indicator | Example |
|-----------|---------|
| "we are businessmen" | Commercial framing |
| "contract with us" | Legal language |
| "recovery companies add 10-50%" | Anti-intermediary |
| "I am not authorized" | Simulated hierarchy |
| Datapack / 30% listing | Exfiltration proof |
| BTC price with USD equivalent | Dual pricing |

---

## Critical Insights

1. **Pioneer in using exfiltrated cyber insurance** as a pricing variable
2. **Closes at ~19% of initial demand** — more flexible in practice than rhetoric suggests
3. **Discourages recovery firms** by citing markup — pushes direct negotiation
4. **Temporarily removes blog posts** during active negotiation as goodwill
5. **Publishes slow-moving victims** — pressure through public example

---

## Classification

```
Style:         Corporate-Legal
Flexibility:   High
Pressure:      High
Sophistication: High
Maturity:      Very High (2021–2022 era, group dismantled)
```

---

## Ransom Note (ThreatLabz)

> Mapping for early attribution (T+0). Source: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notes are **not** vendored here, only referenced.

| Field | Detail |
|-------|--------|
| **ThreatLabz folder** | [`conti/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/conti) |
| **Typical files** | `conti1.txt`, `conti2.txt`, `conti3.txt`, `conti4.txt` |
| **Extension / artifact** | `.conti` |
| **Key note phrases** | *"encrypted by CONTI strain"*, *"cannot be recovered... without contacting our team"*, *"we are businessmen"* |
| **Chat continuity** | Initial legal note; chat expands contract, cyber insurance, and price ladder. |

**If the note contains...** → confirms **Conti** before opening the negotiation portal.

---

## Pre-Extortion Artifacts (RTM)

> Phase **T-7d → T-1h** — tools observed in intrusions leading to deployment. Source: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **not** vendored here.

| Field | Detail |
|-------|--------|
| **RTM GroupProfile** | — |
| **Key tools** | `Mimikatz`, `ProcDump`, `Router Scan`, `SharpChrome`, `GMER`, `PCHunter`, `AdFind`, `Bloodhound`, `PowerView`, `Seatbelt` |
| **Matrices** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Hunt checklist** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Chat/note continuity** | Dropfiles/RClone in exfiltration; chat uses exfiltrated cyber insurance for pricing. |

**If these artifacts appear in the environment** → strengthens **Conti** attribution alongside note and negotiation profile.

---

## MITRE Kill Chain (ThreatActors-TTPs)

> External source: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Field | Detail |
|-------|--------|
| **Status** | No matching folder (Jun 2026) |
| **Alternative** | Use RTM matrices and negotiation profile in this repository |

Index: [`operational_mapping.json`](../operational_mapping.json)
*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 32 chats analyzed* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
