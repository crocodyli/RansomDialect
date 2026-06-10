# REvil (Sodinokibi) — Negotiation Profile (CTI)

> 20 chats, 1,065 messages. Period: 2020–2021.

---

## Metadata

| Field | Value |
|-------|-------|
| Chats | 20 |
| Total messages | 1,065 |
| Price flexibility | **Low-Medium** |
| Pressure intensity | **High** |
| Proof sophistication | **High** |

---

## Executive Summary

REvil represents a **high-maturity RaaS** operation from the 2020–2021 era. It counters victim financial arguments with exfiltrated documents from the victim's own environment. It dismisses crisis narratives (COVID) as *"cover"*. It hides blog publication during active negotiations and uses staged publication by data type as calibrated pressure.

---

## Tone and Communication Style

- **Tone:** Professional, cold, condescending — especially with lawyers
- **Persona:** Experienced negotiator with *"deals with many companies every day"*
- **Rhetorical tactic:** *"you write a lot of text but all of this doesnt matter"*
- **Counter-argumentation:** Uses stolen documents to refute victim claims

**Typical opening:**
> Reply to counsel with prior financial analysis of the victim. Hides blog post while talks are active.

---

## Negotiation Flow

```
1. Upfront financial analysis (exfiltrated docs, insurance, revenue)
2. High initial demand ($7.5M observed)
3. Hides blog publication during negotiation
4. Counters arguments with exfiltrated documents
5. Incremental adjustments: $7.5M -> $6.75M (quickly) -> $5M
6. Rejects low offers ($500K–$1M) as "ridiculous"
7. Staged publication on failure: PII -> customers -> specs
8. Timer extension (+7 days) as rare concession
```

---

## Pricing Strategy

- **Anchoring:** $7.5M -> $5M after adjustments
- **Rejection:** $500K–$1M categorically rejected as *"ridiculous"*
- **Discount logic:** Based on payment speed, not affordability
- **Counter-argument:** Returns exfiltrated financial report + insurance manual to challenge insolvency claims

---

## Decryption and Exfiltration Proof

1. Returns exfiltrated financial report as access proof
2. Shows victim cyber insurance manual as demonstration
3. Staged publication used as proof of damaging capability

---

## Pressure Tactics

- Password/email dump of CEO
- Publication by phases: PII -> customer data -> technical specs
- Timer with rare extension (+7 days) as concession
- Dismissal of COVID narrative as *"cover"*
- Hides blog during talks — signaling publication control

---

## Negotiation-Phase TTPs

- Lawyer-mediated engagement (preferred channel)
- Active use of exfiltrated docs against victim arguments
- Publication pacing calibrated by data type
- Timer as urgency mechanism with negotiable extension
- Deep financial analysis before active negotiation

---

## Behavioral IOCs

| Indicator | Example |
|-----------|---------|
| "We have deals with many companies every day" | Declared experience |
| "price updated to $5M" | Formal adjustment |
| "you write a lot of text but all of this doesnt matter" | Condescension |
| "ridiculous" (for low offers) | Categorical rejection |
| COVID references as "cover" | Narrative dismissal |

---

## Critical Insights

1. **Uses victim-origin documents** to refute financial arguments — sophisticated TTP
2. **Hides blog publication during negotiations** — demonstrates active control and uses it as concession
3. **Staged release by data type** — PII first, then customers, then specs
4. **Timer extension is a rare concession** — not offered easily
5. **Dismissive toward recovery firms and legal counsel** but negotiates when operationally useful

---

## Classification

```
Style:         Sarcastic-Psychological / Corporate
Flexibility:   Low-Medium
Pressure:      High
Sophistication: High
Maturity:      Very High (group dismantled in 2021)
```

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 20 chats analyzed*
