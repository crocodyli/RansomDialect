# Akira — Negotiation Profile (CTI)

> Largest volume in the dataset: 60 chats, 2,408 messages. Period: 2023–2025.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 60 |
| Total messages | 2,408 |
| Actor / victim msgs | 1,193 / 1,215 |
| Avg. actor message length | 154.9 characters |
| Price flexibility | **High** |
| Pressure intensity | **Medium-High** |
| Proof sophistication | **High** |

---

## Executive Summary

Akira operates as a **"technical support company"** with highly standardized scripts. Its surface tone is professional and patient, but pressure escalates through 24h deadlines and onion blog publication. It is one of the most sophisticated groups in financial due diligence and offers the most complete post-payment package in the dataset.

---

## Tone and Communication Style

- **Tone:** Corporate, calm, nearly consultative — similar to an IT helpdesk
- **Persona:** "Akira support" / "surprise security audit"
- **Cadence:** Proactive follow-ups (*"Standing by"*, *"so?"*, *"Waiting for the update"*)
- **Escalation:** Accuses victims of *"playing dirty"* or *"waste our time"* before publishing

**Typical opening:**
> *"Hello. You've reached an Akira support chat. Currently, we are preparing the list of data we took from your network. For now you have to know that dealing with us is the best possible way to settle this quick and cheap."*

Sarcastic variant:
> *"Congratulations, you have passed a surprise information security audit and become a victim of ransomware."*

---

## Negotiation Flow

```
1. "Support chat" opening + request to confirm negotiator authority
2. Delivery of exfiltrated file list (.rar / privnote)
3. Five numbered post-payment services (decryptor, deletion, report, etc.)
4. Financial due diligence (statements, cyber insurance, audits)
5. Test decrypt: 2–3 encrypted files (<=10 MB)
6. Possession proof: 2–3 files from the list on demand
7. Price negotiation with "upper management"
8. BTC payment with test transaction
9. Delivery: CLI decryptor (--secret key), deletion logs, technical report
```

---

## Pricing Strategy

- **Anchoring:** Values from $80K to $2.4M observed in the dataset
- **Flexibility:** High — accepts significant counteroffers (e.g., $2.4M -> $1M, ~58% discount)
- **Modular:** Price can be negotiated in parts (*"whole deal or in parts"*)
- **Levers:** Cyber insurance, victim liquidity, payment speed
- **Tactic:** *"upper management"* as the authority approving discounts

---

## Decryption and Exfiltration Proof

1. Exfiltrated file list via privnote or direct attachment
2. 2–3 uploaded encrypted files returned decrypted
3. 2–3 files from the list as possession proof
4. Delivery of `unlocker.7z` / `unlockers.7z` with CLI instructions

---

## Pressure Tactics

- Publication on onion blog after prolonged silence
- 24h response deadline
- Bad-faith accusation: *"Your attempts to waste our time could force our exit"*
- Publishes **before** agreement if victim delays
- Threat of uploading additional data

---

## Negotiation-Phase TTPs

- Active financial due diligence (requests statements, insurance policy)
- BTC test transaction before full payment
- Detailed post-payment report (kerberoasting, Forti VPN, etc.)
- Deletion logs delivered in .rar
- Decryptor with explicit `--secret` parameter

---

## Behavioral IOCs (Linguistic Indicators)

| Indicator | Example |
|-----------|---------|
| `>` prefix in messages | `> Standing by.` |
| "support chat" | Standard opening |
| "dealing with us is the best possible way" | Opening script |
| "whole deal or in parts" | Modular negotiation |
| "please wait" / "wait a bit" | 23+ occurrences in dataset |
| "are you going to work with us?" | Engagement pressure |
| Cyber insurance references | Due diligence |
| privnote.com links | List delivery |

---

## Critical Insights

1. **Script reused across years** — identical phrases in 2023 and 2025 chats
2. **"Upper management"** is likely a rhetorical lever, not necessarily real hierarchy
3. **Pre-deal publication** is used as delay punishment — does not wait for full negotiation failure
4. **Highest proactive follow-up rate** in the dataset — operator does not wait for victim response
5. **Discounts up to 58%** when victims document limited liquidity

---

## Classification

```
Style:         Corporate-Professional
Flexibility:   High
Pressure:      Medium-High
Sophistication: High
Maturity:      Very High (2023–2025)
```

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 60 chats analyzed*
