# LockBit 3.0 — Negotiation Profile (CTI)

> Third largest volume: 42 chats, 2,220 messages. Period: 2022–2025.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 42 |
| Total messages | 2,220 |
| Actor / victim msgs | 1,313 / 907 |
| Avg. actor message length | ~50 characters (smallest in dataset) |
| Price flexibility | **Variable** (by target size) |
| Pressure intensity | **Medium-High** |
| Proof sophistication | **High** |

---

## Executive Summary

LockBit 3.0 has the **shortest responses in the dataset** — often a single line. The tone is robotic, direct, and dismissive. It adapts price drastically to target size (Entrust: $8M vs SMB: $100K). It operates its own infrastructure (onion FSS, blog) and shows mature RaaS operational automation.

---

## Tone and Communication Style

- **Tone:** Terse, robotic, dismissive when challenged
- **Persona:** Efficient operator with no interest in rapport
- **Cadence:** One-line replies; rarely explains or elaborates
- **Irony:** Especially toward security companies (*"Do google lockbit"*)

**Typical opening:**
> *"hello! pay for key! after payment you will be able to restore your operations."*

Or automated test-decrypt instructions.

---

## Negotiation Flow

```
1. Monosyllabic opening with price or payment instruction
2. 10% listing with password (partial exfiltration download)
3. Onion FSS for files >10MB
4. Test decrypt in chat (encrypted file upload)
5. Minimal negotiation - limited discount (~15%)
6. "last price" as ultimatum
7. Payment -> decryptor + deletion confirmation
```

---

## Pricing Strategy

- **Enterprise:** $8M (Entrust) -> 15% discount = $6.8M
- **Mid-market:** $120K -> $100K
- **SMB:** Lower values with little negotiation
- **Typical phrase:** *"you can afford"* — based on financial OSINT
- **Discount:** Limited (~15%) for enterprise; *"last price"* as hard ceiling
- **Special case:** In some Leaked2025 chats, negotiates deletion only (no decryptor)

---

## Decryption and Exfiltration Proof

1. 10% listing with password-protected download
2. Proprietary onion File Sharing Service (FSS) for large files
3. Direct test decrypt in chat
4. Massive data proof — full download availability in Leaked2025 chats

---

## Pressure Tactics

- Irony toward cyber/security firms
- Threat of publication on leak blog
- *"our principles have become worth more than money"* — refusal to negotiate "on principle"
- *"last price"* as no-margin ultimatum
- Criminal reputation leverage (*"Do google lockbit"*)

---

## Negotiation-Phase TTPs

- Proprietary infrastructure: onion FSS, blog, payment portal
- Temporary blog takedown as concession
- Test decrypt automation
- Price adaptation by target size (OSINT-driven)
- In some cases: data-deletion-only negotiation, no decryptor

---

## Behavioral IOCs

| Indicator | Example |
|-----------|---------|
| "hello! pay for key!" | One-line opening |
| "Do google lockbit" | Reputation proof |
| "last price" | Ultimatum |
| "you can afford" | Financial OSINT |
| Onion FSS links | Proprietary infrastructure |
| Replies under 50 characters | Robotic style |

---

## Critical Insights

1. **Smallest average message size** in the dataset — efficiency over relationship building
2. **80x pricing spread** between enterprise ($8M) and SMB ($100K)
3. **Massive data-proof pattern** in Leaked2025 chats — full download available
4. **Limited discounting** (~15%) — less flexible than Conti/Akira
5. **Dismissive toward financial excuses** — monosyllabic rejection replies

---

## Classification

```
Style:         Minimalist-Transactional
Flexibility:   Variable (by target size)
Pressure:      Medium-High
Sophistication: High
Maturity:      Very High (mature RaaS)
```

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 42 chats analyzed*
