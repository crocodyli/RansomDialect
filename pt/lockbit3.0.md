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

*Fonte: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 42 chats analisados · [EN](../en/lockbit3.0.md)*
