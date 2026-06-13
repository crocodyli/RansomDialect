# RansomDialect

> Behavioral CTI profiles of ransomware negotiation chats — how each threat actor talks, pressures, and closes deals.

Perfis CTI do "dialeto" de negociação de 25 grupos ransomware — tom, táticas e playbook por ator.  
Derived from [Ransomchats](https://github.com/Casualtek/Ransomchats) (241 chats) + cross-references to [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) (notes), [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) (tools) and [ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) (MITRE kill chain).

---

## Extortion lifecycle coverage

```
T-7d → T-1h          T+0              T+N
RTM + crocodyli  →  ThreatLabz  →  RansomDialect (Ransomchats)
(intrusion/hunt)    (ransom note)    (negotiation chat)
```

---

## Languages / Idiomas

| Idioma | Entrada |
|--------|---------|
| **Português** | [`pt/00-VISAO-GERAL.md`](./pt/00-VISAO-GERAL.md) → [`pt/`](./pt/) |
| **English** | [`en/00-OVERVIEW.md`](./en/00-OVERVIEW.md) → [`en/`](./en/) |

---

## What's inside

- **25 threat actor profiles** — negotiation tone, pricing, pressure tactics, proof-of-decryption patterns
- **Ransom note mapping** — early attribution (T+0) via [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes)
- **Operational mapping** — pre-extortion hunt/IR via [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) + MITRE kill chain via [ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
- **Comparative overview** — taxonomy, cross-group insights, quick identification tables (ops + note + chat)
- **Bilingual** — full PT and EN versions

---

## Data sources

| Source | Role | Link |
|--------|------|------|
| **Ransomchats** | Negotiation chats (T+N) — primary dataset | [Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) (MIT) |
| **ThreatLabz** | Ransom notes (T+0) — external mapping | [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) |
| **RTM** | Tools in intrusions (T-7d → T-1h) — hunt/IR | [BushidoUK/Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) |
| **crocodyli** | MITRE TTPs + CVEs — kill chain | [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) |

| Document | Description |
|----------|-------------|
| [`FONTES.md`](./FONTES.md) | Origem dos dados + mapeamento de cada ator (PT) |
| [`SOURCES.md`](./SOURCES.md) | Data origin + actor mapping (EN) |
| [`notes_mapping.json`](./notes_mapping.json) | Índice ator → ThreatLabz (21 mapeados, 4 sem entrada) |
| [`operational_mapping.json`](./operational_mapping.json) | Índice ator → RTM + crocodyli (20 RTM, 6 crocodyli) |
| [`ransomwarelive_index.json`](./ransomwarelive_index.json) | Índice ator → URLs de perfil (integração ransomware.live) |

Also available: [ransomch.at](https://ransomch.at/) · [ransomware.live](https://www.ransomware.live/#/negotiations)

---

## Related projects

| Project | Relationship |
|---------|--------------|
| [Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) | Primary data — negotiation chats |
| [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) | Ransom notes (T+0) — referenced, not vendored |
| [BushidoUK/Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) | Tools in intrusions — hunt/IR |
| [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) | MITRE TTPs — referenced, not vendored |
| [ransomware.live](https://www.ransomware.live/#/negotiations) | Live tracker + negotiations UI |

---

## Quick links — top actors by volume

| Actor | Chats | PT | EN |
|-------|------:|----|----|
| Akira | 60 | [pt/Akira.md](./pt/Akira.md) | [en/Akira.md](./en/Akira.md) |
| lockbit3.0 | 42 | [pt/lockbit3.0.md](./pt/lockbit3.0.md) | [en/lockbit3.0.md](./en/lockbit3.0.md) |
| Conti | 32 | [pt/Conti.md](./pt/Conti.md) | [en/Conti.md](./en/Conti.md) |
| REvil | 20 | [pt/REvil.md](./pt/REvil.md) | [en/REvil.md](./en/REvil.md) |

---

## Upload / sync

Se estiver atualizando o repositório manualmente no GitHub, siga a ordem em [`UPLOAD.md`](./UPLOAD.md).

---

## License

MIT — see [`LICENSE`](./LICENSE).  
Chat data © [Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats). Ransom notes © [Zscaler ThreatLabz](https://github.com/ThreatLabz/ransomware_notes). Tool matrix © [BushidoUK/RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix). TTP data © [crocodyli](https://github.com/crocodyli/ThreatActors-TTPs). Profiles and analysis © RansomDialect contributors.

---

*For research, defense, and threat intelligence only.*
