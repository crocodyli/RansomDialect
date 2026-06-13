# Data Sources — RansomDialect

> Documentation of chat origins and behavioral mapping of each ransomware actor.

---

## Data Origin

All negotiation chats used in this analysis were obtained from the public repository **[Ransomchats](https://github.com/Casualtek/Ransomchats)**, maintained by **Casualtek** (Valéry Marchive).

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

1. HTML backups of group chat portals are collected (by contributors, researchers, or victims)
2. Scripts in `parsers/` convert HTML → JSON (BeautifulSoup)
3. Content is manually anonymized before publication
4. No chat is published without explicit consent for parsing and redaction

### Local analysis scope

This folder contains behavioral profiles derived from repository JSONs:

- **`pt/`** — Portuguese profiles
- **`en/`** — English profiles
- **`pt/00-VISAO-GERAL.md`** — comparative overview (PT)
- **`en/00-OVERVIEW.md`** — comparative overview (EN)
- **`notes_mapping.json`** — actor → ThreatLabz folder index (ransom notes)
- **`operational_mapping.json`** — actor → RTM + crocodyli (intrusion/hunt)
- **`ransomwarelive_index.json`** — actor → profile URLs (ransomware.live integration)

---

## Ransom Notes — ThreatLabz (T+0)

Secondary source for **early attribution** at incident discovery. External repository **[ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes)** (Zscaler ThreatLabz) — `.txt` files per family, **not vendored** in this project.

| Field | Detail |
|-------|---------|
| **Repository** | [github.com/ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) |
| **Content** | Historical and current ransom notes (pre-chat phase) |
| **Local index** | [`notes_mapping.json`](./notes_mapping.json) |
| **Scope** | 21 of 25 actors mapped; 4 with no ThreatLabz folder |

### Actor → ThreatLabz mapping

| Ransomchats actor | ThreatLabz folder | Status |
|-------------------|-------------------|--------|
| Akira | [`akira/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/akira) | mapped |
| lockbit3.0 | [`lockbit/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/lockbit) | mapped |
| Conti | [`conti/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/conti) | mapped |
| REvil | [`revil/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/revil) | mapped |
| trinity | [`trinity/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/trinity) | mapped |
| Dragonforce | [`dragonforce/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/dragonforce) | mapped |
| Hive | [`hive/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hive) | mapped |
| Avaddon | [`avaddon/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avaddon) | mapped |
| Nightspire | [`nightspire/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/nightspire) | mapped |
| fog | [`fog/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/fog) | mapped |
| BlackBasta | [`blackbasta/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackbasta) | mapped |
| Darkside | [`darkside/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/darkside) | mapped |
| Mallox | [`mallox/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/mallox) | mapped |
| BlackMatter | [`blackmatter/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/blackmatter) | mapped |
| Cloak | [`cloak/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/cloak) | mapped |
| NoEscape | [`noescape/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/noescape) | mapped |
| Qilin | [`qilin/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/qilin) | mapped |
| Ranzy | [`ranzy/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ranzy) | mapped |
| Avos | [`avoslocker/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/avoslocker) | mapped |
| Hunters International | [`hunters/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/hunters) | mapped |
| RansomHub | [`ransomhub/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/ransomhub) | mapped |
| Babuk | — | not listed (Jun 2026) |
| mount-locker | — | not listed (Jun 2026) |
| Pear | — | not listed (Jun 2026) |
| RunSomeWares | — | not listed (Jun 2026) |

Each individual profile includes a **Ransom Note (ThreatLabz)** section with key phrases, typical files, and chat continuity.

---

## Operational Context — RTM + ThreatActors-TTPs (T-7d → T-1h)

External sources for **hunt/IR and MITRE kill chain** in the pre-extortion phase — complement note (T+0) and chat (T+N).

| Source | Repository | Local index | Scope (25 actors) |
|--------|------------|-------------|-------------------|
| **Ransomware-Tool-Matrix (RTM)** | [BushidoUK/Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) | [`operational_mapping.json`](./operational_mapping.json) | **20** with tools in matrix or GroupProfile; **5** not listed (Cloak, NoEscape, Pear, RunSomeWares, trinity) |
| **ThreatActors-TTPs (crocodyli)** | [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) | same | **6** with MITRE folder (Akira, BlackBasta, Dragonforce, Hunters International, lockbit3.0, RansomHub) |

### RTM — dedicated GroupProfiles

| Actor | RTM GroupProfile |
|-------|------------------|
| Akira | [`GroupProfiles/Akira.md`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Akira.md) |
| BlackBasta | [`GroupProfiles/BlackBasta.md`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/BlackBasta.md) |
| Dragonforce | [`GroupProfiles/DragonForce.md`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/DragonForce.md) |
| Qilin | [`GroupProfiles/Qilin.md`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Qilin.md) |

Threat hunt checklist: [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv)

Each profile includes **Pre-Extortion Artifacts (RTM)** and **MITRE Kill Chain (ThreatActors-TTPs)** when applicable.

---

## What each actor does in negotiation

Mapping of each group's **behavioral role** during the extortion phase.

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
Conduct financial due diligence, offer structured post-payment packages, negotiate with real flexibility after high anchoring.

### "Minimalist" actors (LockBit 3.0, Ranzy, trinity, fog)
Minimize interaction, set price quickly, avoid rapport. LockBit adapts price to target size; trinity charges per endpoint.

### "Psychological" actors (Avaddon, BlackMatter, REvil)
Use sarcasm, irony, and exfiltrated documents against victim arguments. Rapid emotional escalation.

### "Procedural" actors (Cloak, mount-locker, Pear)
Impose formal rules, authority gatekeeping, legal frameworks or detailed contracts before negotiating value.

### Actors with unique operational models
- **Hive** — supply-chain attack; won't negotiate with indirect victims
- **Avos** — Staff central / affiliate separation
- **Mallox** — BOT-driven automatic discount in chat
- **Hunters International** — extreme take-it-or-leave-it model

---

## References and credits

| Resource | Link |
|----------|------|
| Source repository (chats) | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| Ransom notes (T+0) | [github.com/ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) |
| Notes index | [`notes_mapping.json`](./notes_mapping.json) |
| Tool matrix (T-7d→T-1h) | [github.com/BushidoUK/Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) |
| MITRE TTPs (crocodyli) | [github.com/crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) |
| Operational index | [`operational_mapping.json`](./operational_mapping.json) |
| ransomware.live index | [`ransomwarelive_index.json`](./ransomwarelive_index.json) |
| Chat reader | [ransomch.at](https://ransomch.at/) |
| CTI integration | [ransomware.live/negotiations](https://www.ransomware.live/#/negotiations) |
| Contributors | @g0njxa, Rakesh Krishnan, @JMousqueton, eCime.ch |
| LockBit research | [Analyst1 — Negotiating with LockBit](https://analyst1.com/blog-negotiating-with-lockbit-uncovering-the-evolution-of-operations-and-newly-established-rules/) |
| Akira research | [Analyst1 — Akira 2024 Review](https://analyst1.com/ransomware-extortion-activity-in-2024-a-year-in-review/) |
| Stylometric analysis | [Calvin So — Medium](https://medium.com/@callyso0414/tracing-ransomware-threat-actors-through-stylometric-analysis-and-chat-log-examination-23f0f84abba8) |

---

## Limitations

- Anonymized data — full victim context unavailable
- Survival bias — only chats that reached public collection
- Some groups have very small samples (1–2 chats)
- Profiles derived from local CTI analysis; not official repository documentation
- Ransom notes referenced externally (ThreatLabz); 4 actors without a matching folder
- Operational data (RTM/crocodyli) referenced externally; partial per-actor coverage

---

*Analysis derived from the [Ransomchats](https://github.com/Casualtek/Ransomchats) dataset + [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes), [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix), and [ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) mappings — for research, defense, and threat intelligence.*
