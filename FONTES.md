# Fontes de Dados â€” Ransomchats

> DocumentaÃ§Ã£o da origem dos chats e mapeamento do comportamento de cada ator de ransomware.

---

## Origem dos Dados

Todos os chats de negociaÃ§Ã£o utilizados nesta anÃ¡lise foram obtidos do repositÃ³rio pÃºblico **[Ransomchats](https://github.com/Casualtek/Ransomchats)**, mantido por **Casualtek** (ValÃ©ry Marchive).

| Campo | Detalhe |
|-------|---------|
| **RepositÃ³rio** | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| **LicenÃ§a** | MIT License (Copyright 2023 ValÃ©ry Marchive) |
| **Formato** | JSON normalizado (`chat_id` + array `messages`) |
| **ConteÃºdo** | NegociaÃ§Ãµes reais entre vÃ­timas e grupos de ransomware |
| **AnonimizaÃ§Ã£o** | Dados sensÃ­veis marcados como `[redacted]`; vÃ­timas nÃ£o divulgadas publicamente permanecem anÃ´nimas |
| **Ãndice oficial** | `chat_index.json` â€” 25 grupos, 241 chats, ~11.473 mensagens |
| **VisualizaÃ§Ã£o** | [ransomch.at](https://ransomch.at/) Â· [ransomware.live](https://www.ransomware.live/#/negotiations) |

### Como os dados chegam ao repositÃ³rio

1. Backups HTML dos portais de chat dos grupos sÃ£o coletados (por contribuidores, pesquisadores ou vÃ­timas)
2. Scripts em `parsers/` convertem HTML â†’ JSON (BeautifulSoup)
3. ConteÃºdo Ã© anonimizado manualmente antes da publicaÃ§Ã£o
4. Nenhum chat Ã© publicado sem consentimento explÃ­cito para parsing e redaÃ§Ã£o

### Escopo desta anÃ¡lise local

A pasta `profiles/` contÃ©m perfis comportamentais derivados dos JSONs do repositÃ³rio, organizados em:

- **`pt/`** â€” perfis em portuguÃªs
- **`en/`** â€” perfis em inglÃªs
- **`pt/00-VISAO-GERAL.md`** â€” visÃ£o comparativa (PT)
- **`en/00-OVERVIEW.md`** â€” visÃ£o comparativa (EN)

---

## O que cada ator faz na negociaÃ§Ã£o

Mapeamento do **papel comportamental** de cada grupo durante a fase de extorsÃ£o â€” o que o operador faz, como se comunica e quais tÃ¡ticas emprega.

| Ator | Chats | O que o ator faz na negociaÃ§Ã£o | Tom | Perfil |
|------|------:|-------------------------------|-----|--------|
| **Akira** | 60 | Atua como "suporte tÃ©cnico"; due diligence financeira; pacote modular de 5 serviÃ§os; follow-ups proativos | Corporativo, paciente â†’ pressÃ£o 24h | [PT](pt/Akira.md) Â· [EN](en/Akira.md) |
| **lockbit3.0** | 42 | Respostas de 1 linha; preÃ§o por porte do alvo; FSS onion prÃ³prio; "hello! pay for key!" | Robotizado, desdenhoso | [PT](pt/lockbit3.0.md) Â· [EN](en/lockbit3.0.md) |
| **Conti** | 32 | Contrato jurÃ­dico; usa seguro cyber exfiltrado; escada de preÃ§os; remove blog temporariamente | JurÃ­dico-comercial | [PT](pt/Conti.md) Â· [EN](en/Conti.md) |
| **REvil** | 20 | Refuta argumentos com docs roubados; publicaÃ§Ã£o escalonada; esconde blog durante talks | Frio, condescendente | [PT](pt/REvil.md) Â· [EN](en/REvil.md) |
| **trinity** | 14 | PreÃ§o por endpoint (BTC/PC); inventÃ¡rio de hosts; prova social via "coworkers" | Seco, transacional | [PT](pt/trinity.md) Â· [EN](en/trinity.md) |
| **Dragonforce** | 14 | Ancora em BTC; timer 2 semanas; foco em credibilidade da marca | Direto, confiante | [PT](pt/Dragonforce.md) Â· [EN](en/Dragonforce.md) |
| **Hive** | 8 | Supply-chain: recusa SMBs downstream; redireciona ao vendor MSP | Formal, inflexÃ­vel | [PT](pt/Hive.md) Â· [EN](en/Hive.md) |
| **Avaddon** | 7 | Sarcasmo e escalada emocional; General Decryptor Ãºnico; DDoS e spam a terceiros | SarcÃ¡stico â†’ agressivo | [PT](pt/Avaddon.md) Â· [EN](en/Avaddon.md) |
| **Nightspire** | 7 | OSINT de filings pÃºblicos (10-K); pressÃ£o SEC/contratos; escalada com menÃ§Ã£o a FBI | Agressivo, calculista | [PT](pt/Nightspire.md) Â· [EN](en/Nightspire.md) |
| **fog** | 6 | Abertura mÃ­nima ("hi"); delega a "bosses"; conhecimento tÃ©cnico do .fog | Casual, pragmÃ¡tico | [PT](pt/fog.md) Â· [EN](en/fog.md) |
| **BlackBasta** | 5 | Framing "businessman"; desconto por prazo; piso rÃ­gido ~$150K | Business-like | [PT](pt/BlackBasta.md) Â· [EN](en/BlackBasta.md) |
| **Darkside** | 5 | OSINT financeiro profundo; ameaÃ§a short sellers e imprensa (Forbes, NYT) | Frio, intimidador | [PT](pt/Darkside.md) Â· [EN](en/Darkside.md) |
| **Mallox** | 3 | BOT aplica desconto % automaticamente; desconfia de backups | Funcional, BOT+humano | [PT](pt/Mallox.md) Â· [EN](en/Mallox.md) |
| **Babuk** | 2 | Pergunta sobre seguro; pricing via Zoominfo; ameaÃ§as GDPR/prisÃ£o CEO | TÃ©cnico â†’ ameaÃ§ador | [PT](pt/Babuk.md) Â· [EN](en/Babuk.md) |
| **BlackMatter** | 2 | Humor sarcÃ¡stico; conhece infra em tempo real; verificaÃ§Ã£o obrigatÃ³ria | IrÃ´nico, sofisticado | [PT](pt/BlackMatter.md) Â· [EN](en/BlackMatter.md) |
| **Cloak** | 2 | 6 regras + 11 passos antes do preÃ§o; venda de dados a terceiros | Procedural, burocrÃ¡tico | [PT](pt/Cloak.md) Â· [EN](en/Cloak.md) |
| **NoEscape** | 2 | Tom polido; test decrypt via portal; publica se silÃªncio | Formal, cortÃªs | [PT](pt/NoEscape.md) Â· [EN](en/NoEscape.md) |
| **Qilin** | 2 | Script Akira-like; 7 entregÃ¡veis; ameaÃ§a venda a fisco | Profissional, paciente | [PT](pt/Qilin.md) Â· [EN](en/Qilin.md) |
| **Ranzy** | 2 | PreÃ§o fixo $7K; sem prova; sem double extortion | Minimalista | [PT](pt/Ranzy.md) Â· [EN](en/Ranzy.md) |
| **Avos** | 1 | Modelo RaaS Staff/affiliate; customer support enterprise | Profissional, moderado | [PT](pt/Avos.md) Â· [EN](en/Avos.md) |
| **Hunters International** | 1 | Ultimato puro; recusa $1,5M e $4M; "I'm okay to get nothing" | Frio, inflexÃ­vel | [PT](pt/Hunters%20International.md) Â· [EN](en/Hunters%20International.md) |
| **mount-locker** | 1 | Framework legal (class-action); compara perdas legais vs. resgate | Educado, firme | [PT](pt/mount-locker.md) Â· [EN](en/mount-locker.md) |
| **Pear** | 1 | Contrato numerado (aâ€“e); leak proativo de caso sensÃ­vel | RÃ­gido, impaciente | [PT](pt/Pear.md) Â· [EN](en/Pear.md) |
| **RansomHub** | 1 | Template FAQ automatizado; sem diÃ¡logo capturado | Automatizado | [PT](pt/RansomHub.md) Â· [EN](en/RansomHub.md) |
| **RunSomeWares** | 1 | Pesquisa reputaÃ§Ã£o/famÃ­lia; cooperativo se vÃ­tima engaja | PragmÃ¡tico | [PT](pt/RunSomeWares.md) Â· [EN](en/RunSomeWares.md) |

---

## PadrÃµes transversais por tipo de ator

### Atores "corporativos" (Akira, Conti, BlackBasta, Qilin)
Fazem due diligence financeira, oferecem pacotes pÃ³s-pagamento estruturados, negociam com flexibilidade real apÃ³s ancoragem alta.

### Atores "minimalistas" (LockBit 3.0, Ranzy, trinity, fog)
Minimizam interaÃ§Ã£o, fixam preÃ§o rapidamente, evitam rapport. LockBit adapta preÃ§o ao porte; trinity cobra por endpoint.

### Atores "psicolÃ³gicos" (Avaddon, BlackMatter, REvil)
Usam sarcasmo, ironia e documentos exfiltrados contra argumentos da vÃ­tima. Escalada emocional rÃ¡pida.

### Atores "procedurais" (Cloak, mount-locker, Pear)
ImpÃµem regras formais, gatekeeping de autoridade, frameworks legais ou contratos detalhados antes de negociar valor.

### Atores com modelo operacional Ãºnico
- **Hive** â€” ataque supply-chain; nÃ£o negocia com vÃ­timas indiretas
- **Avos** â€” separaÃ§Ã£o Staff central / affiliate
- **Mallox** â€” automaÃ§Ã£o de desconto via BOT no chat
- **Hunters International** â€” modelo take-it-or-leave-it extremo

---

## ReferÃªncias e crÃ©ditos

| Recurso | Link |
|---------|------|
| RepositÃ³rio fonte | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| Leitor de chats | [ransomch.at](https://ransomch.at/) |
| IntegraÃ§Ã£o CTI | [ransomware.live/negotiations](https://www.ransomware.live/#/negotiations) |
| ContribuiÃ§Ãµes | @g0njxa, Rakesh Krishnan, @JMousqueton, eCime.ch |
| Pesquisa LockBit | [Analyst1 â€” Negotiating with LockBit](https://analyst1.com/blog-negotiating-with-lockbit-uncovering-the-evolution-of-operations-and-newly-established-rules/) |
| Pesquisa Akira | [Analyst1 â€” Akira 2024 Review](https://analyst1.com/ransomware-extortion-activity-in-2024-a-year-in-review/) |
| AnÃ¡lise estilomÃ©trica | [Calvin So â€” Medium](https://medium.com/@callyso0414/tracing-ransomware-threat-actors-through-stylometric-analysis-and-chat-log-examination-23f0f84abba8) |

---

## LimitaÃ§Ãµes

- Dados anonimizados â€” contexto completo da vÃ­tima indisponÃ­vel
- ViÃ©s de sobrevivÃªncia â€” apenas chats que chegaram Ã  coleta pÃºblica
- Alguns grupos tÃªm amostra muito pequena (1â€“2 chats)
- Perfis derivados por anÃ¡lise CTI local; nÃ£o sÃ£o documentaÃ§Ã£o oficial do repositÃ³rio

---

*AnÃ¡lise derivada do dataset [Ransomchats](https://github.com/Casualtek/Ransomchats) â€” uso para pesquisa, defesa e threat intelligence.*

