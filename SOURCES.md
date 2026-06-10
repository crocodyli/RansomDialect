# Data Sources — Ransomchats

> Documentation of chat origins and behavioral mapping of each ransomware actor.

---

## Data Origin

All negotiation chats used in this analysis were obtained from the public repository **[Ransomchats](https://github.com/Casualtek/Ransomchats)**, maintained by **Casualtek** (Valéry Marchive)[cite: 1].

| Field | Detail |
|-------|--------|
| **Repository** | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| **License** | MIT License (Copyright 2023 Valéry Marchive) |
| **Format** | Normalized JSON (`chat_id` + `messages` array) |
| **Content** | Real negotiations between victims and ransomware groups |
| **Anonymization** | Sensitive data marked as `[redacted]`; non-publicly disclosed victims remain anonymous |
| **Official index** | `chat_index.json` — 25 groups, 241 chats, ~11,473 messages |
| **Viewers** | [ransomch.at](https://ransomch.at/) · [ransomware.live](https://www.ransomware.live/#/negotiations) |

### How data reaches the repository

1. HTML backups of group chat portals are collected (by contributors, researchers, or victims)[cite: 1].
2. Scripts in `parsers/` convert HTML → JSON (BeautifulSoup)[cite: 1].
3. Content is manually anonymized before publication[cite: 1].
4. No chat is published without explicit consent for parsing and redaction[cite: 1].

### Local analysis scope

This repository contains behavioral profiles derived from repository JSONs:

- **`pt/`** — Portuguese profiles
- **`en/`** — English profiles
- **`pt/00-VISAO-GERAL.md`** — comparative overview (PT)
- **`en/00-OVERVIEW.md`** — comparative overview (EN)

---

## What each actor does in negotiation

Mapping of each group's **behavioral role** during the extortion phase[cite: 1].

| Actor | Chats | What the actor does in negotiation | Tone | Profile |
|-------|------:|-----------------------------------|------|---------|
| **Akira** | 60 | Acts as "tech support"; financial due diligence; modular 5-service package; proactive follow-ups | Corporate, patient → 24h pressure | [PT](pt/Akira.md) · [EN](en/Akira.md) |
| **lockbit3.0** | 42 | One-line responses; price by target size; own FSS onion; "hello! pay for key!" | Robotic, dismissive | [PT](pt/lockbit3.0.md) · [EN](en/lockbit3.0.md) |
| **Conti** | 32 | Legal contract framing; uses exfiltrated cyber insurance; price ladder; temporary blog removal | Legal-commercial | [PT](pt/Conti.md) · [EN](en/Conti.md) |
| **REvil** | 20 | Refutes arguments with stolen docs; staged publication; hides blog during talks | Cold, condescending | [PT](pt/REvil.md) · [EN](en/REvil.md) |
| **trinity** | 14 | Per-endpoint pricing (BTC/PC); host inventory; social proof via "coworkers" | Dry, transactional | [PT](pt/trinity.md) · [EN](en/trinity.md) |
| **Dragonforce** | 14 | BTC anchoring; 2-week timer; brand credibility focus | Direct, confident | [PT](pt/Dragonforce.md) · [EN](en/Dragonforce.md) |
| **Hive** | 8 | Supply-chain: refuses downstream SMBs; redirects to MSP vendor | Formal, inflexible | [PT](pt/Hive.md) · [EN](en/Hive.md) |
| **Avaddon** | 7 | Sarcasm and emotional escalation; single General Decryptor; DDoS and third-party spam | Sarcastic → aggressive | [PT](pt/Avaddon.md) · [EN](en/Avaddon.md) |
| **Nightspire** | 7 | Public filings OSINT (10-K); SEC/contract pressure; escalation on FBI mention | Aggressive, calculated | [PT](pt/Nightspire.md) · [EN](en/Nightspire.md) |
| **fog** | 6 | Minimal opening ("hi"); delegates to "bosses"; technical .fog knowledge | Casual, pragmatic | [PT](pt/fog.md) · [EN](en/fog.md) |
| **BlackBasta** | 5 | "Businessman" framing; time-bound discount; rigid floor ~$150K | Business-like | [PT](pt/BlackBasta.md) · [EN](en/BlackBasta.md) |
| **Darkside** | 5 | Deep financial OSINT; threatens short sellers and press (Forbes, NYT) | Cold, intimidating | [PT](pt/Darkside.md) · [EN](en/Darkside.md) |
| **Mallox** | 3 | BOT applies automatic % discount; distrusts backup claims | Functional, BOT+human | [PT](pt/Mallox.md) · [EN](en/Mallox.md) |
| **Babuk** | 2 | Asks about insurance; Zoominfo pricing; GDPR/CEO prison threats | Technical → threatening | [PT](pt/Babuk.md) · [EN](en/Babuk.md) |
| **BlackMatter** | 2 | Sarcastic humor; real-time infra knowledge; mandatory verification | Ironic, sophisticated | [PT](pt/BlackMatter.md) · [EN](en/BlackMatter.md) |
| **Cloak** | 2 | 6 rules + 11 steps before price; third-party data sale | Procedural, bureaucratic | [PT](pt/Cloak.md) · [EN](en/Cloak.md) |
| **NoEscape** | 2 | Polished tone; portal test decrypt; publishes on silence | Formal, courteous | [PT](pt/NoEscape.md) · [EN](en/NoEscape.md) |
| **Qilin** | 2 | Akira-like script; 7 deliverables; tax authority sale threat | Professional, patient | [PT](pt/Qilin.md) · [EN](en/Qilin.md) |
| **Ranzy** | 2 | Fixed $7K price; no proof; no double extortion | Minimalist | [PT](pt/Ranzy.md) · [EN](en/Ranzy.md) |
| **Avos** | 1 | RaaS Staff/affiliate model; enterprise customer support | Professional, moderate | [PT](pt/Avos.md) · [EN](en/Avos.md) |
| **Hunters International** | 1 | Pure ultimatum; refuses $1.5M and $4M; "I'm okay to get nothing" | Cold, inflexible | [PT](pt/Hunters%20International.md) · [EN](en/Hunters%20International.md) |
| **mount-locker** | 1 | Legal framework (class-action); compares legal losses vs. ransom | Polite, firm | [PT](pt/mount-locker.md) · [EN](en/mount-locker.md) |
| **Pear** | 1 | Numbered contract (a–e); proactive sensitive case leak | Rigid, impatient | [PT](pt/Pear.md) · [EN](en/Pear.md) |
| **RansomHub** | 1 | Automated FAQ template; no dialogue captured | Automated | [PT](pt/RansomHub.md) · [EN](en/RansomHub.md) |
| **RunSomeWares** | 1 | Researches reputation/family; cooperative when victim engages | Pragmatic | [PT](pt/RunSomeWares.md) · [EN](en/RunSomeWares.md) |

---

## Cross-cutting patterns by actor type

### "Corporate" actors (Akira, Conti, BlackBasta, Qilin)
Conduct financial due diligence, offer structured post-payment packages, negotiate with real flexibility after high anchoring[cite: 1].

### "Minimalist" actors (LockBit 3.0, Ranzy, trinity, fog)
Minimize interaction, set price quickly, avoid rapport. LockBit adapts price to target size; trinity charges per endpoint[cite: 1].

### "Psychological" actors (Avaddon, BlackMatter, REvil)
Use sarcasm, irony, and exfiltrated documents against victim arguments. Rapid emotional escalation[cite: 1].

### "Procedural" actors (Cloak, mount-locker, Pear)
Impose formal rules, authority gatekeeping, legal frameworks or detailed contracts before negotiating value[cite: 1].

### Actors with unique operational models
- **Hive** — supply-chain attack; won't negotiate with indirect victims[cite: 1]
- **Avos** — Staff central / affiliate separation[cite: 1]
- **Mallox** — BOT-driven automatic discount in chat[cite: 1]
- **Hunters International** — extreme take-it-or-leave-it model[cite: 1]

---

## References and credits

| Resource | Link |
|----------|------|
| Source repository | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| Chat reader | [ransomch.at](https://ransomch.at/) |
| CTI integration | [ransomware.live/negotiations](https://www.ransomware.live/#/negotiations) |
| Contributors | @g0njxa, Rakesh Krishnan, @JMousqueton, eCime.ch |
| LockBit research | [Analyst1 — Negotiating with LockBit](https://analyst1.com/blog-negotiating-with-lockbit-uncovering-the-evolution-of-operations-and-newly-established-rules/) |
| Akira research | [Analyst1 — Akira 2024 Review](https://analyst1.com/ransomware-extortion-activity-in-2024-a-year-in-review/) |
| Stylometric analysis | [Calvin So — Medium](https://medium.com/@callyso0414/tracing-ransomware-threat-actors-through-stylometric-analysis-and-chat-log-examination-23f0f84abba8) |

---

## Limitations

- Anonymized data — full victim context unavailable[cite: 1]
- Survival bias — only chats that reached public collection[cite: 1]
- Some groups have very small samples (1–2 chats)[cite: 1]
- Profiles derived from local CTI analysis; not official repository documentation[cite: 1]

---

*Analysis derived from the [Ransomchats](https://github.com/Casualtek/Ransomchats) dataset — for research, defense, and threat intelligence.*
