# Ransomware Negotiation Profile Mapping

> **CTI analysis** — Behavioral profiles of 25 ransomware groups based on 241 real negotiations (~11,473 messages) from the [Ransomchats](https://github.com/Casualtek/Ransomchats) dataset.

---

## Objective

This mapping documents **how each group communicates with victims** during the ransom negotiation phase — tone, tactics, price flexibility, proof patterns, and linguistic markers. It is intended for:

- **IR/DFIR teams** — early identification of the responsible group
- **Professional negotiators** — response strategy preparation
- **CTI analysts** — behavioral correlation across incidents
- **Academic research** — ransomware ecosystem evolution

---

## Comparative Table

| Group | Chats | Msgs | Price Flex. | Pressure | Sophist. | Predominant style |
|-------|------:|-----:|-------------|----------|----------|-------------------|
| Akira | 60 | 2,408 | High | Medium-High | High | Corporate-professional |
| lockbit3.0 | 42 | 2,220 | Variable | Medium-High | High | Terse/robotic |
| Conti | 32 | 1,709 | High | High | High | Legal-commercial |
| REvil | 20 | 1,065 | Low-Medium | High | High | Cold/condescending |
| Dragonforce | 14 | 375 | Medium | Medium | Medium | Direct/confident |
| trinity | 14 | 713 | None | Low | Low | Minimalist/transactional |
| Avaddon | 7 | 380 | Medium | High | Medium | Sarcastic/aggressive |
| Nightspire | 7 | 367 | Medium | Very High | Medium-High | Financial OSINT-driven |
| fog | 6 | 333 | Medium-High | Low-Medium | Medium | Casual/pragmatic |
| Hive | 8 | 372 | None* | Low | Low | Formal supply-chain |
| BlackBasta | 5 | 257 | Medium | Medium-High | High | Business-like |
| Darkside | 5 | 425 | Low | Very High | Medium | Cold/intimidating |
| Mallox | 3 | 108 | Medium | Low | Medium | BOT + human |
| Babuk | 2 | 150 | Medium-High | High | High | Technical/threatening |
| BlackMatter | 2 | 121 | Medium | Medium | High | Sarcastic/masked |
| Cloak | 2 | 120 | Low | High | Medium | Procedural/bureaucratic |
| NoEscape | 2 | 10 | N/A | Medium-High | Low | Formal/polite |
| Qilin | 2 | 39 | N/A | High | Medium-High | Akira-like standard |
| Ranzy | 2 | 56 | None | Low | None | Smash-and-grab |
| Avos | 1 | 86 | High | Medium | Medium | RaaS staff/affiliate |
| Hunters Intl. | 1 | 29 | Very Low | High | Medium | Pure ultimatum |
| mount-locker | 1 | 60 | Low-Medium | High | High | Legal-financial |
| Pear | 1 | 42 | Low-Medium | High | High | Strict contract |
| RunSomeWares | 1 | 27 | Medium-High | Medium | High | Pragmatic/cooperative |
| RansomHub | 1 | 1 | N/A | High** | N/A | FAQ template |

*\*Hive: inflexible for downstream supply-chain victims*  
*\*\*RansomHub: pressure only in the initial template, no dialogue*

---

## Six-Style Negotiation Taxonomy

### 1. Corporate-Professional
**Akira, Conti, BlackBasta, Qilin, Avos, RunSomeWares**

- Standardized, reusable scripts across years of operations
- Numbered post-payment service bundles (decryptor, deletion log, technical report)
- Financial due diligence: cyber insurance, statements, audits
- Patient tone with gradual pressure escalation

### 2. Aggressive-Ultimatum
**Hunters International, Darkside, Nightspire, Pear, Avaddon**

- High initial price and little real flexibility
- Intense legal, regulatory, and reputational pressure
- Short timers (24–48h) with explicit consequences
- Rapid escalation when victims mention authorities (FBI, SEC)

### 3. Minimalist-Transactional
**lockbit3.0, Ranzy, trinity, fog**

- Short replies (1–3 lines, often monosyllabic)
- Little to no price negotiation
- Focus on direct payment without rapport
- lockbit3.0: *"hello! pay for key!"* as a typical opener

### 4. Sarcastic-Psychological
**Avaddon, BlackMatter, REvil**

- Irony and condescension (*"you write a lot of text but all of this doesnt matter"*)
- Uses prior chat history against victims who pull back
- Knows intimate infrastructure details in real time
- Dismisses financial arguments using exfiltrated victim documents

### 5. Procedural-Bureaucratic
**Cloak, mount-locker, NoEscape**

- Numbered rules (6 rules + 11 steps) before any price disclosure
- Authority gatekeeping (*"authorized representative"*)
- Legal framework as primary pressure (class-action, GDPR)
- Process-first focus over outcome

### 6. Distinct Operating Models
**Hive** (supply-chain), **Avos** (RaaS Staff/affiliate), **Mallox** (BOT+human)

- Hive: refuses to negotiate with SMBs indirectly impacted through MSPs
- Avos: central operator / affiliate split limits exfiltration proof availability
- Mallox: BOT applies automatic percentage discount with expiration date

---

## Cross-Cutting Insights

### Pricing
1. **Aggressive anchoring** is universal — initial demand is typically 3–10x above the final accepted value (Conti: $920K -> $172K; Avos: $150K -> $85K)
2. **Time-based discounts** (24–72h) are the most common concession, not discounts based on real inability to pay
3. **Cyber insurance** is a pricing factor in ~40% of mature groups (Conti, Akira, Babuk, Darkside, REvil)
4. **Recovery firms** are referenced by Conti itself as a 10–50% markup

### Capability Proof
1. **Test decrypt** of 2–3 files is the universal standard among mature groups
2. **Partial exfiltration listing** (10–30%) as a second proof layer
3. **On-demand files** from the list as possession proof
4. Older groups (Ranzy, trinity) often **offer no proof at all**

### Pressure and Extortion
1. **Staged publication** (1–3% -> 10% -> full release) is the dominant TTP
2. **Legal pressure** (GDPR, class-action, SEC) increased significantly post-2023
3. **Financial OSINT** (public filings, cyber insurance, revenue) is a key differentiator in 2024+ groups (Nightspire, Pear)
4. **Mentioning FBI/authorities** often **increases** aggressiveness

### Temporal Evolution

| Era | Period | Characteristics |
|-----|--------|-----------------|
| **Primitive** | 2020–2021 | Short chats, fixed pricing, no double extortion (Ranzy, trinity, early REvil) |
| **Professionalization** | 2021–2022 | Corporate scripts, cyber insurance leverage, post-payment bundles (Conti, Darkside, Babuk) |
| **Maturity** | 2023–2024 | Financial due diligence, legal pressure, multiple channels (Akira, BlackBasta, lockbit3.0) |
| **Sophistication** | 2025–2026 | Public OSINT, detailed contracts, LE-triggered escalation (Nightspire, Pear, RunSomeWares) |

---

## Rapid Identification by Linguistic Signals

| If the victim sees... | Probable group |
|-----------------------|----------------|
| *"support chat"* + *"surprise security audit"* | **Akira** |
| *"hello! pay for key!"* (one-line reply) | **LockBit 3.0** |
| *"How may I help you?"* + company verification | **Hive** / **BlackMatter** |
| 6 rules + 11 steps before pricing | **Cloak** |
| *"Tick tock"* + sarcasm and emoticons | **Avaddon** |
| Per-endpoint pricing (0.25 BTC/PC) | **trinity** |
| BOT applies discount automatically | **Mallox** |
| *"Public filings show..."* + 10-K style data | **Nightspire** |
| FAQ template with no human dialogue | **RansomHub** |
| *"we are businessmen"* + long legal contract | **Conti** |
| *"bosses are demanding $X"* + casual tone | **fog** |
| *"I'm okay to get nothing"* + ultimatum | **Hunters International** |
| *"Staff"* / *"affiliate"* + customer support | **Avos** |
| *"non-negotiable"* + numbered conditions (a–e) | **Pear** |

---

## Groups with Limited Dataset Coverage

Profiles for these groups should be **validated with additional CTI sources**:

| Group | Chats | Limitation |
|-------|------:|------------|
| RansomHub | 1 | Only 1 message (FAQ template) |
| Hunters International | 1 | Single chat, ultimatum without negotiation |
| Avos | 1 | Single case, RaaS model |
| Pear | 1 | Detailed contract but no pricing rounds |
| RunSomeWares | 1 | Cooperative style but single sample |
| mount-locker | 1 | Legal framework, no long negotiation |
| NoEscape | 2 | No captured pricing negotiation |
| Ranzy | 2 | Minimalist, no double extortion |

---

## Individual Profiles

| Group | File |
|-------|------|
| Akira | [Akira.md](Akira.md) |
| Avaddon | [Avaddon.md](Avaddon.md) |
| Avos | [Avos.md](Avos.md) |
| Babuk | [Babuk.md](Babuk.md) |
| BlackBasta | [BlackBasta.md](BlackBasta.md) |
| BlackMatter | [BlackMatter.md](BlackMatter.md) |
| Cloak | [Cloak.md](Cloak.md) |
| Conti | [Conti.md](Conti.md) |
| Darkside | [Darkside.md](Darkside.md) |
| Dragonforce | [Dragonforce.md](Dragonforce.md) |
| fog | [fog.md](fog.md) |
| Hive | [Hive.md](Hive.md) |
| Hunters International | [Hunters International.md](Hunters%20International.md) |
| lockbit3.0 | [lockbit3.0.md](lockbit3.0.md) |
| Mallox | [Mallox.md](Mallox.md) |
| mount-locker | [mount-locker.md](mount-locker.md) |
| Nightspire | [Nightspire.md](Nightspire.md) |
| NoEscape | [NoEscape.md](NoEscape.md) |
| Pear | [Pear.md](Pear.md) |
| Qilin | [Qilin.md](Qilin.md) |
| RansomHub | [RansomHub.md](RansomHub.md) |
| Ranzy | [Ranzy.md](Ranzy.md) |
| REvil | [REvil.md](REvil.md) |
| RunSomeWares | [RunSomeWares.md](RunSomeWares.md) |
| trinity | [trinity.md](trinity.md) |

---

## Methodology

1. Review of 2–4 representative chats per group (60+ chats qualitatively analyzed)
2. Quantitative analysis: message counts, average length, keyword frequency
3. Qualitative analysis: tone, negotiation flow, TTPs, linguistic patterns
4. Correlation with public CTI literature (Analyst1, Huntress, PCMag, SEC4U, ransomware.live)

## Limitations

- Anonymized data — full victim context unavailable
- Survivorship bias — only chats that reached public collection
- Timestamps frequently absent or imprecise
- Some chats involve professional negotiators, not the victim directly

---

*Source: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 241 chats analyzed*
