# Mapeamento de Perfis de Negociação Ransomware

> **Análise CTI** — Perfis comportamentais de 25 grupos de ransomware baseados em 241 negociações reais (~11.473 mensagens) do dataset [Ransomchats](https://github.com/Casualtek/Ransomchats).  
> Versão em inglês: [`en/00-OVERVIEW.md`](../en/00-OVERVIEW.md) · Fontes: [`FONTES.md`](../FONTES.md)

---

## Objetivo

Este mapeamento documenta **como cada grupo se comunica com vítimas** durante a fase de negociação de resgate — tom, táticas, flexibilidade de preço, provas oferecidas e padrões linguísticos. Destina-se a:

- **Equipes de IR/DFIR** — identificação precoce do grupo responsável
- **Negociadores profissionais** — preparação de estratégia de resposta
- **Analistas CTI** — correlação comportamental entre incidentes
- **Pesquisa acadêmica** — evolução do ecossistema ransomware

---

## Tabela Comparativa

| Grupo | Chats | Msgs | Flex. Preço | Pressão | Sofist. | Estilo predominante |
|-------|------:|-----:|-------------|---------|---------|---------------------|
| Akira | 60 | 2.408 | Alta | Média-Alta | Alta | Corporativo-profissional |
| lockbit3.0 | 42 | 2.220 | Variável | Média-Alta | Alta | Terse/robotizado |
| Conti | 32 | 1.709 | Alta | Alta | Alta | Jurídico-comercial |
| REvil | 20 | 1.065 | Baixa-Média | Alta | Alta | Frio/condescendente |
| Dragonforce | 14 | 375 | Média | Média | Média | Direto/confiante |
| trinity | 14 | 713 | Nenhuma | Baixa | Baixa | Minimalista/transacional |
| Avaddon | 7 | 380 | Média | Alta | Média | Sarcástico/agressivo |
| Nightspire | 7 | 367 | Média | Muito Alta | Média-Alta | OSINT financeiro |
| fog | 6 | 333 | Média-Alta | Baixa-Média | Média | Casual/pragmático |
| Hive | 8 | 372 | Nenhuma* | Baixa | Baixa | Supply-chain formal |
| BlackBasta | 5 | 257 | Média | Média-Alta | Alta | Business-like |
| Darkside | 5 | 425 | Baixa | Muito Alta | Média | Frio/intimidador |
| Mallox | 3 | 108 | Média | Baixa | Média | BOT + humano |
| Babuk | 2 | 150 | Média-Alta | Alta | Alta | Técnico/ameaçador |
| BlackMatter | 2 | 121 | Média | Média | Alta | Sarcástico/mascarado |
| Cloak | 2 | 120 | Baixa | Alta | Média | Procedural/burocrático |
| NoEscape | 2 | 10 | N/D | Média-Alta | Baixa | Formal/cortês |
| Qilin | 2 | 39 | N/D | Alta | Média-Alta | Padrão Akira-like |
| Ranzy | 2 | 56 | Nenhuma | Baixa | Nenhuma | Smash-and-grab |
| Avos | 1 | 86 | Alta | Média | Média | Staff/affiliate RaaS |
| Hunters Intl. | 1 | 29 | Muito Baixa | Alta | Média | Ultimato puro |
| mount-locker | 1 | 60 | Baixa-Média | Alta | Alta | Legal-financeiro |
| Pear | 1 | 42 | Baixa-Média | Alta | Alta | Contrato rígido |
| RunSomeWares | 1 | 27 | Média-Alta | Média | Alta | Pragmático/cooperativo |
| RansomHub | 1 | 1 | N/D | Alta** | N/D | FAQ template |

*\*Hive: inflexível para vítimas downstream de supply-chain*  
*\*\*RansomHub: pressão apenas em template inicial, sem diálogo*

---

## Taxonomia de 6 Estilos de Negociação

### 1. Corporativo-Profissional
**Akira, Conti, BlackBasta, Qilin, Avos, RunSomeWares**

- Scripts padronizados e reutilizáveis em anos de operação
- Pacotes de serviços numerados pós-pagamento (decryptor, deletion log, relatório técnico)
- Due diligence financeira: seguro cyber, extratos, auditorias
- Tom paciente com escalada gradual de pressão

### 2. Agressivo-Ultimato
**Hunters International, Darkside, Nightspire, Pear, Avaddon**

- Preço inicial alto e pouca flexibilidade real
- Pressão legal, regulatória e reputacional intensa
- Timers curtos (24–48h) com consequências explícitas
- Escalada rápida quando vítima menciona autoridades (FBI, SEC)

### 3. Minimalista-Transacional
**lockbit3.0, Ranzy, trinity, fog**

- Respostas curtas (1–3 linhas, frequentemente monossilábicas)
- Pouca ou nenhuma negociação de preço
- Foco em pagamento direto sem rapport
- lockbit3.0: *"hello! pay for key!"* como abertura típica

### 4. Sarcástico-Psicológico
**Avaddon, BlackMatter, REvil**

- Ironia e condescendência (*"you write a lot of text but all of this doesnt matter"*)
- Usa histórico do chat contra a vítima que recua
- Conhece detalhes íntimos da infraestrutura em tempo real
- Despreza argumentos financeiros com documentos exfiltrados da própria vítima

### 5. Procedural-Burocrático
**Cloak, mount-locker, NoEscape**

- Regras numeradas (6 regras + 11 passos) antes de qualquer preço
- Gatekeeping de autoridade (*"authorized representative"*)
- Framework legal como pressão principal (class-action, GDPR)
- Foco em processo sobre resultado

### 6. Modelos Operacionais Distintos
**Hive** (supply-chain), **Avos** (Staff/affiliate RaaS), **Mallox** (BOT+humano)

- Hive: recusa negociar com SMBs afetados indiretamente via MSP
- Avos: separação operador central / afiliado limita provas de exfiltração
- Mallox: BOT aplica desconto % automaticamente com data de expiração

---

## Insights Transversais

### Precificação
1. **Ancoragem agressiva** é universal — preço inicial tipicamente 3–10× acima do valor final aceito (Conti: $920K → $172K; Avos: $150K → $85K)
2. **Desconto temporal** (24–72h) é a concessão mais comum, não desconto por incapacidade financeira real
3. **Seguro cyber** é fator de pricing em ~40% dos grupos maduros (Conti, Akira, Babuk, Darkside, REvil)
4. **Recovery firms** citadas como markup de 10–50% pelo próprio Conti

### Prova de Capacidade
1. **Test decrypt** de 2–3 arquivos é padrão universal entre grupos maduros
2. **Lista parcial de exfiltração** (10–30%) como segunda prova
3. **Arquivos sob demanda** da lista como prova de posse
4. Grupos antigos (Ranzy, trinity) frequentemente **não oferecem prova alguma**

### Pressão e Extorsão
1. **Publicação escalonada** (1–3% → 10% → completo) é TTP dominante
2. **Pressão legal** (GDPR, class-action, SEC) cresceu significativamente pós-2023
3. **OSINT financeiro** (filings públicos, seguro cyber, receita) é diferencial dos grupos 2024+ (Nightspire, Pear)
4. **Menção a FBI/autoridades** frequentemente **escala** a agressividade

### Evolução Temporal

| Era | Período | Características |
|-----|---------|-----------------|
| **Primitiva** | 2020–2021 | Chats curtos, preço fixo, sem double extortion (Ranzy, trinity, REvil early) |
| **Profissionalização** | 2021–2022 | Scripts corporativos, seguro cyber, pacotes pós-pagamento (Conti, Darkside, Babuk) |
| **Maturidade** | 2023–2024 | Due diligence financeira, pressão legal, múltiplos canais (Akira, BlackBasta, lockbit3.0) |
| **Sofisticação** | 2025–2026 | OSINT público, contratos detalhados, escalada por LE (Nightspire, Pear, RunSomeWares) |

---

## Identificação Rápida por Sinais Linguísticos

| Se a vítima vê... | Provável grupo |
|-------------------|----------------|
| *"support chat"* + *"auditoria de segurança surpresa"* | **Akira** |
| *"hello! pay for key!"* (resposta de 1 linha) | **LockBit 3.0** |
| *"How may I help you?"* + verificação de empresa | **Hive** / **BlackMatter** |
| 6 regras + 11 passos antes do preço | **Cloak** |
| *"Tick tock"* + sarcasmo e emoticons | **Avaddon** |
| Preço por endpoint (0.25 BTC/PC) | **trinity** |
| BOT aplica desconto automaticamente | **Mallox** |
| *"Public filings show..."* + dados 10-K | **Nightspire** |
| FAQ template sem diálogo humano | **RansomHub** |
| *"we are businessmen"* + contrato jurídico longo | **Conti** |
| *"bosses are demanding $X"* + tom casual | **fog** |
| *"I'm okay to get nothing"* + ultimato | **Hunters International** |
| *"Staff"* / *"affiliate"* + customer support | **Avos** |
| *"non-negotiable"* + condições numeradas (a–e) | **Pear** |

---

## Grupos com Dataset Limitado

Perfis destes grupos devem ser **validados com outras fontes CTI**:

| Grupo | Chats | Limitação |
|-------|------:|-----------|
| RansomHub | 1 | Apenas 1 mensagem (template FAQ) |
| Hunters International | 1 | Único chat, ultimato sem negociação |
| Avos | 1 | Caso único, modelo RaaS |
| Pear | 1 | Contrato detalhado mas sem rodadas de preço |
| RunSomeWares | 1 | Cooperativo mas amostra única |
| mount-locker | 1 | Framework legal, sem negociação longa |
| NoEscape | 2 | Sem negociação de preço capturada |
| Ranzy | 2 | Minimalista, sem double extortion |

---

## Perfis Individuais

| Grupo | Arquivo |
|-------|---------|
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

## Metodologia

1. Leitura de 2–4 chats representativos por grupo (60+ chats analisados qualitativamente)
2. Análise quantitativa: contagem de mensagens, tamanho médio, frequência de palavras-chave
3. Análise qualitativa: tom, fluxo de negociação, TTPs, padrões linguísticos
4. Correlação com literatura CTI pública (Analyst1, Huntress, PCMag, SEC4U, ransomware.live)

## Limitações

- Dados anonimizados — contexto completo da vítima indisponível
- Viés de sobrevivência — apenas chats que chegaram à coleta pública
- Timestamps frequentemente ausentes ou imprecisos
- Alguns chats envolvem negociadores profissionais, não a vítima diretamente

---

*Análise CTI — Ransomchats Dataset — Uso para pesquisa, defesa e threat intelligence.*
