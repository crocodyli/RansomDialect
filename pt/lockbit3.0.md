# LockBit 3.0 — Perfil de Negociação (CTI)

> Terceiro maior volume: 42 chats, 2.220 mensagens. Período: 2022–2025.

---

## Metadados

| Campo | Valor |
|-------|-------|
| Chats | 42 |
| Mensagens totais | 2.220 |
| Msgs ator / vítima | 1.313 / 907 |
| Tamanho médio msg. ator | ~50 caracteres (menor do dataset) |
| Flexibilidade de preço | **Variável** (por porte do alvo) |
| Intensidade de pressão | **Média-Alta** |
| Sofisticação de provas | **Alta** |

---

## Resumo Executivo

LockBit 3.0 é o grupo com **respostas mais curtas do dataset** — frequentemente uma única linha. O tom é robotizado, direto e desdenhoso. Adapta preço drasticamente ao porte do alvo (Entrust: $8M vs. SMB: $100K). Opera infraestrutura própria (FSS onion, blog) e demonstra maturidade RaaS com automação de processos.

---

## Tom e Estilo de Comunicação

- **Tom:** Terse, robotizado, desdenhoso quando provocado
- **Persona:** Operador eficiente sem interesse em rapport
- **Cadência:** Respostas de 1 linha; raramente explica ou elabora
- **Ironia:** Especialmente com empresas de segurança (*"Do google lockbit"*)

**Abertura típica:**
> *"hello! pay for key! after payment you will be able to restore your operations."*

Ou instruções automatizadas de test decrypt.

---

## Fluxo de Negociação

```
1. Abertura monossilábica com preço ou instrução de pagamento
2. 10% listing com senha (download parcial de exfiltração)
3. FSS onion para arquivos >10MB
4. Test decrypt no chat (upload de arquivos criptografados)
5. Negociação mínima — desconto limitado (~15%)
6. "last price" como ultimato
7. Pagamento → decryptor + confirmação de deleção
```

---

## Estratégia de Precificação

- **Enterprise:** $8M (Entrust) → 15% desconto = $6,8M
- **Mid-market:** $120K → $100K
- **SMB:** Valores baixos com pouca negociação
- **Frase típica:** *"you can afford"* — baseado em OSINT financeiro
- **Desconto:** Limitado (~15%) em alvos enterprise; *"last price"* como teto
- **Caso especial:** Negocia apenas deleção (sem decrypt) em alguns chats Leaked2025

---

## Prova de Descriptografia e Exfiltração

1. 10% listing com senha para download
2. File Sharing Service (FSS) onion próprio para arquivos grandes
3. Test decrypt direto no chat
4. Prova de dados massiva — download completo em chats Leaked2025

---

## Táticas de Pressão

- Ironia com empresas de segurança/cyber
- Ameaça de publicação no blog
- *"our principles have become worth more than money"* — recusa negociar por princípio
- *"last price"* como ultimato sem margem
- Reputação criminal como alavanca (*"Do google lockbit"*)

---

## TTPs na Fase de Negociação

- Infraestrutura própria: FSS onion, blog, portal de pagamento
- Blog takedown temporário como concessão
- Automação de test decrypt
- Adaptação de preço por porte do alvo (OSINT)
- Em alguns casos: negocia apenas deleção de dados, sem decryptor

---

## IOCs Comportamentais

| Indicador | Exemplo |
|-----------|---------|
| "hello! pay for key!" | Abertura de 1 linha |
| "Do google lockbit" | Prova de reputação |
| "last price" | Ultimato |
| "you can afford" | OSINT financeiro |
| Links FSS onion | Infraestrutura própria |
| Respostas <50 caracteres | Estilo robotizado |

---

## Insights Críticos

1. **Menor tamanho médio de mensagem** do dataset — eficiência sobre relacionamento
2. **Variação de preço de 80×** entre enterprise ($8M) e SMB ($100K)
3. **Prova de dados massiva** em chats Leaked2025 — download completo disponível
4. **Desconto limitado** (~15%) — menos flexível que Conti/Akira
5. **Desprezo por desculpas financeiras** repetidas — respostas monossilábicas de rejeição

---

## Classificação

```
Estilo:         Minimalista-Transacional
Flexibilidade:  Variável (por porte)
Pressão:        Média-Alta
Sofisticação:   Alta
Maturidade:     Muito Alta (RaaS maduro)
```

---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`lockbit/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/lockbit) |
| **Arquivos típicos** | `lockbit3.txt`, `[rand].README.txt`, `ReadMeForDecrypt.txt` |
| **Extensão / artefato** | `.lockbit3 / .abcd` |
| **Frases-chave da nota** | *"LockBit 3.0 the world's fastest"*, *"Your data is stolen and encrypted"*, *"TOR darknet sites"* |
| **Continuidade com o chat** | Nota branding LockBit 3.0; chat reduz tudo a *hello! pay for key!*. |

**Se a nota contém...** → confirma **lockbit3.0** antes de abrir o portal de negociação.

---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Gosecretsdump`, `LaZagne`, `LostMyPassword`, `Mimikatz`, `NirSoft ExtPassword`, `PasswordFox`, `ProcDump`, `Veeam-Get-Creds`, `Backstab/Process Explorer driver (BYOVD)`, `Defender Control` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Cobalt Strike/RMM massivos; chat reduz a *hello! pay for key!*. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **lockbit3.0** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`LockBit/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/LockBit) |
| **TTPs (MITRE)** | [`LockBit-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/LockBit/LockBit-TTP.md) |
| **CVEs** | — |
| **TTPs-chave** | *T1190 — Exploração massiva de CVEs (Fortinet, Exchange, etc.)*; *T1219 — RMM e Cobalt Strike no precursor*; *T1486 — LockBit 3.0 builder / afiliados* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.

---

*Fonte: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 42 chats analisados · [EN](../en/lockbit3.0.md)* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
