# Fontes de Dados — Ransomchats

> Documentação da origem dos chats e mapeamento do comportamento de cada ator de ransomware.

---

## Origem dos Dados

Todos os chats de negociações utilizados nesta análise foram obtidos do repositório público **[Ransomchats](https://github.com/Casualtek/Ransomchats)**, mantido por **Casualtek** (Valéry Marchive).

| Campo | Detalhe |
|-------|---------|
| **Repositório** | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| **Licença** | MIT License (Copyright 2023 Valéry Marchive) |
| **Formato** | JSON normalizado (`chat_id` + array `messages`) |
| **Conteúdo** | Negociações reais entre vítimas e grupos de ransomware |
| **Anonimização** | Dados sensíveis marcados como `[redacted]`; vítimas não divulgadas publicamente permanecem anônimas |
| **Índice oficial** | `chat_index.json` — 25 grupos, 241 chats, ~11.473 mensagens |
| **Visualização** | [ransomch.at](https://ransomch.at/) · [ransomware.live](https://www.ransomware.live/#/negotiations) |

### Como os dados chegam ao repositório

1. Backups HTML dos portais de chat dos grupos são coletados (por contribuidores, pesquisadores ou vítimas).
2. Scripts em `parsers/` convertem HTML → JSON (BeautifulSoup).
3. Conteúdo é anonimizado manualmente antes da publicação.
4. Nenhum chat é publicado sem consentimento explícito para *parsing* e redação.

### Escopo desta análise local

A pasta `profiles/` contém perfis comportamentais derivados dos JSONs do repositório, organizados em:

- **`pt/`** — perfis em português
- **`en/`** — perfis em inglês
- **`pt/00-VISAO-GERAL.md`** — visão comparativa (PT)
- **`en/00-OVERVIEW.md`** — visão comparativa (EN)

---

## O que cada ator faz na negociação

Mapeamento do **papel comportamental** de cada grupo durante a fase de extorsão — o que o operador faz, como se comunica e quais táticas emprega.

| Ator | Chats | O que o ator faz na negociação | Tom | Perfil |
|------|------:|-------------------------------|-----|--------|
| **Akira** | 60 | Atua como "suporte técnico"; due diligence financeira; pacote modular de 5 serviços; follow-ups proativos | Corporativo, paciente → pressão 24h | [PT](pt/Akira.md) · [EN](en/Akira.md) |
| **lockbit3.0** | 42 | Respostas de 1 linha; preço por porte do alvo; FSS onion próprio; "hello! pay for key!" | Robotizado, desdenhoso | [PT](pt/lockbit3.0.md) · [EN](en/lockbit3.0.md) |
| **Conti** | 32 | Contrato jurídico; usa seguro cyber exfiltrado; escada de preços; remove blog temporariamente | Jurídico-comercial | [PT](pt/Conti.md) · [EN](en/Conti.md) |
| **REvil** | 20 | Refuta argumentos com docs roubados; publicação escalonada; esconde blog durante talks | Frio, condescendente | [PT](pt/REvil.md) · [EN](en/REvil.md) |
| **trinity** | 14 | Preço por endpoint (BTC/PC); inventário de hosts; prova social via "coworkers" | Seco, transacional | [PT](pt/trinity.md) · [EN](en/trinity.md) |
| **Dragonforce** | 14 | Âncora em BTC; timer 2 semanas; foco em credibilidade da marca | Direto, confiante | [PT](pt/Dragonforce.md) · [EN](en/Dragonforce.md) |
| **Hive** | 8 | Supply-chain: recusa SMBs downstream; redireciona ao vendor MSP | Formal, inflexível | [PT](pt/Hive.md) · [EN](en/Hive.md) |
| **Avaddon** | 7 | Sarcasmo e escalada emocional; General Decryptor único; DDoS e spam a terceiros | Sarcástico → agressivo | [PT](pt/Avaddon.md) · [EN](en/Avaddon.md) |
| **Nightspire** | 7 | OSINT de filings públicos (10-K); pressão SEC/contratos; escalada com menção a FBI | Agressivo, calculista | [PT](pt/Nightspire.md) · [EN](en/Nightspire.md) |
| **fog** | 6 | Abertura mínima ("hi"); delega a "bosses"; conhecimento técnico do .fog | Casual, pragmático | [PT](pt/fog.md) · [EN](en/fog.md) |
| **BlackBasta** | 5 | Framing "businessman"; desconto por prazo; piso rígido ~$150K | Business-like | [PT](pt/BlackBasta.md) · [EN](en/BlackBasta.md) |
| **Darkside** | 5 | OSINT financeiro profundo; ameaça short sellers e imprensa (Forbes, NYT) | Frio, intimidador | [PT](pt/Darkside.md) · [EN](en/Darkside.md) |
| **Mallox** | 3 | BOT aplica desconto % automaticamente; desconfia de backups | Funcional, BOT+humano | [PT](pt/Mallox.md) · [EN](en/Mallox.md) |
| **Babuk** | 2 | Pergunta sobre seguro; pricing via Zoominfo; ameaças GDPR/prisão CEO | Técnico → ameaçador | [PT](pt/Babuk.md) · [EN](en/Babuk.md) |
| **BlackMatter** | 2 | Humor sarcástico; conhece infra em tempo real; verificação obrigatória | Irônico, sofisticado | [PT](pt/BlackMatter.md) · [EN](en/BlackMatter.md) |
| **Cloak** | 2 | 6 regras + 11 passos antes do preço; venda de dados a terceiros | Procedural, burocrático | [PT](pt/Cloak.md) · [EN](en/Cloak.md) |
| **NoEscape** | 2 | Tom polido; test decrypt via portal; publica se silêncio | Formal, cortês | [PT](pt/NoEscape.md) · [EN](en/NoEscape.md) |
| **Qilin** | 2 | Script Akira-like; 7 entregáveis; ameaça venda a fisco | Profissional, paciente | [PT](pt/Qilin.md) · [EN](en/Qilin.md) |
| **Ranzy** | 2 | Preço fixo $7K; sem prova; sem double extortion | Minimalista | [PT](pt/Ranzy.md) · [EN](en/Ranzy.md) |
| **Avos** | 1 | Modelo RaaS Staff/affiliate; customer support enterprise | Profissional, moderado | [PT](pt/Avos.md) · [EN](en/Avos.md) |
| **Hunters International** | 1 | Ultimato puro; recusa $1,5M e $4M; "I'm okay to get nothing" | Frio, inflexível | [PT](pt/Hunters%20International.md) · [EN](en/Hunters%20International.md) |
| **mount-locker** | 1 | Framework legal (class-action); compara perdas legais vs. resgate | Educado, firme | [PT](pt/mount-locker.md) · [EN](en/mount-locker.md) |
| **Pear** | 1 | Contrato numerado (a–e); leak proativo de caso sensível | Rígido, impaciente | [PT](pt/Pear.md) · [EN](en/Pear.md) |
| **RansomHub** | 1 | Template FAQ automatizado; sem diálogo capturado | Automatizado | [PT](pt/RansomHub.md) · [EN](en/RansomHub.md) |
| **RunSomeWares** | 1 | Pesquisa reputação/família; cooperativo se vítima engaja | Pragmático | [PT](pt/RunSomeWares.md) · [EN](en/RunSomeWares.md) |

---

## Padrões transversais por tipo de ator

### Atores "corporativos" (Akira, Conti, BlackBasta, Qilin)
Fazem *due diligence* financeira, oferecem pacotes pós-pagamento estruturados e negociam com flexibilidade real após ancoragem alta.

### Atores "minimalistas" (LockBit 3.0, Ranzy, trinity, fog)
Minimizam interações, fixam preço rapidamente e evitam *rapport*. LockBit adapta preço ao porte; trinity cobra por endpoint.

### Atores "psicológicos" (Avaddon, BlackMatter, REvil)
Usam sarcasmo, ironia e documentos exfiltrados contra argumentos da vítima. Escalada emocional rápida.

### Atores "procedurais" (Cloak, mount-locker, Pear)
Impõem regras formais, *gatekeeping* de autoridade, frameworks legais ou contratos detalhados antes de negociar valores.

### Atores com modelo operacional único
- **Hive** — ataque *supply-chain*; não negocia com vítimas indiretas.
- **Avos** — separação entre Staff central e *affiliate*.
- **Mallox** — automação de desconto via BOT no chat.
- **Hunters International** — modelo *take-it-or-leave-it* extremo.

---

## Referências e créditos

| Recurso | Link |
|---------|------|
| Repositório fonte | [github.com/Casualtek/Ransomchats](https://github.com/Casualtek/Ransomchats) |
| Leitor de chats | [ransomch.at](https://ransomch.at/) |
| Integração CTI | [ransomware.live/negotiations](https://www.ransomware.live/#/negotiations) |
| Contribuições | @g0njxa, Rakesh Krishnan, @JMousqueton, eCime.ch |
| Pesquisa LockBit | [Analyst1 — Negotiating with LockBit](https://analyst1.com/blog-negotiating-with-lockbit-uncovering-the-evolution-of-operations-and-newly-established-rules/) |
| Pesquisa Akira | [Analyst1 — Akira 2024 Review](https://analyst1.com/ransomware-extortion-activity-in-2024-a-year-in-review/) |
| Análise estilométrica | [Calvin So — Medium](https://medium.com/@callyso0414/tracing-ransomware-threat-actors-through-stylometric-analysis-and-chat-log-examination-23f0f84abba8) |

---

## Limitações

- Dados anonimizados — contexto completo da vítima indisponível.
- Viés de sobrevivência — apenas chats que chegaram à coleta pública.
- Alguns grupos têm amostra muito pequena (1–2 chats).
- Perfis derivados por análise CTI local; não são documentação oficial do repositório.

---

*Análise derivada do dataset [Ransomchats](https://github.com/Casualtek/Ransomchats) — uso para pesquisa, defesa e threat intelligence.*
