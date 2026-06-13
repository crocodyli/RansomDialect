# Conti — Perfil de Negociação (CTI)

> Segundo maior volume: 32 chats, 1.709 mensagens. Período: 2021–2022.

---

## Metadados

| Campo | Valor |
|-------|-------|
| Chats | 32 |
| Mensagens totais | 1.709 |
| Msgs ator / vítima | ~850 / ~859 |
| Flexibilidade de preço | **Alta** |
| Intensidade de pressão | **Alta** |
| Sofisticação de provas | **Alta** |

---

## Resumo Executivo

Conti representa o ápice da **profissionalização ransomware** da era 2021–2022. Opera com linguagem jurídico-comercial (*"we are businessmen"*, *"contract with us"*), usa documentos de seguro cyber exfiltrados como alavanca de pricing, e fecha negócios a frações significativas do pedido inicial. Referencia explicitamente recovery firms como markup de 10–50%.

---

## Tom e Estilo de Comunicação

- **Tom:** Corporativo, assertivo, ocasionalmente agressivo
- **Persona:** Negociador autorizado com limites hierárquicos (*"I am not authorized"*)
- **Framing:** Transação comercial legítima, não crime
- **Documentação:** Texto de "contrato" longo e jurídico na abertura

**Abertura típica:**
> Resumo do ataque + preço em BTC/USD + datapack de 30% da exfiltração + oferta de test decrypt gratuito.

---

## Fluxo de Negociação

```
1. Resumo do ataque + preço inicial (frequentemente $500K–$920K)
2. Entrega de datapack (30% listing) + exemplo
3. Test decrypt: 2 arquivos escolhidos pela vítima, grátis
4. Negociação com escada descendente de preços
5. Desconto 25% se pagamento em 2 dias úteis
6. Remoção temporária do blog (24h) como concessão
7. Pagamento BTC → entrega de decryptor + pacote completo
```

---

## Estratégia de Precificação

- **Ancoragem agressiva:** $920K observado como pedido inicial
- **Escada descendente documentada:** $920K → $600K → $350K → $255K → **$172K aceito**
- **Taxa de fechamento:** ~19% do pedido inicial
- **Desconto temporal:** 25% por pagamento em 2 dias úteis
- **Fator seguro:** Usa apólice de seguro cyber exfiltrada para calibrar preço
- **Anti-intermediário:** *"recovery companies add 10-50%"* — desincentiva negociadores externos

---

## Prova de Descriptografia e Exfiltração

1. Datapack com 30% do listing de arquivos exfiltrados
2. 2 arquivos escolhidos pela vítima descriptografados gratuitamente
3. Referência a mercado dark de $500B como contexto de valor dos dados

---

## Táticas de Pressão

- Publicação parcial de 1–3% dos dados em 3 dias
- Exposição de apólice de seguro cyber da vítima
- Publicação de vítimas que negociam lentamente
- Ameaça de leilão/venda de dados no mercado dark
- Timer com contagem regressiva rígida

---

## TTPs na Fase de Negociação

- Análise ativa de seguro cyber exfiltrado
- Remoção temporária do blog (24h) como concessão durante talks
- Pacote pós-pagamento completo (decryptor, deletion, relatório)
- Engajamento com advogados e recovery firms
- Publicação escalonada por tipo de dado

---

## IOCs Comportamentais

| Indicador | Exemplo |
|-----------|---------|
| "we are businessmen" | Framing comercial |
| "contract with us" | Linguagem jurídica |
| "recovery companies add 10-50%" | Anti-intermediário |
| "I am not authorized" | Hierarquia simulada |
| Datapack / 30% listing | Prova de exfiltração |
| Preço em BTC com equivalente USD | Precificação dual |

---

## Insights Críticos

1. **Pioneiro em usar seguro cyber exfiltrado** como variável de pricing
2. **Fecha em ~19% do pedido** — maior flexibilidade real que a retórica sugere
3. **Desincentiva recovery firms** citando markup — tenta negociação direta
4. **Remove blog temporariamente** durante negociação ativa como goodwill
5. **Publica vítimas lentas** — pressão por exemplo social

---

## Classificação

```
Estilo:         Corporativo-Jurídico
Flexibilidade:  Alta
Pressão:        Alta
Sofisticação:   Alta
Maturidade:     Muito Alta (era 2021–2022, grupo desmantelado)
```

---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`conti/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/conti) |
| **Arquivos típicos** | `conti1.txt`, `conti2.txt`, `conti3.txt`, `conti4.txt` |
| **Extensão / artefato** | `.conti` |
| **Frases-chave da nota** | *"encrypted by CONTI strain"*, *"cannot be recovered... without contacting our team"*, *"we are businessmen"* |
| **Continuidade com o chat** | Nota jurídica inicial; chat expande contrato, seguro cyber e escada de preços. |

**Se a nota contém...** → confirma **Conti** antes de abrir o portal de negociação.

---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `Mimikatz`, `ProcDump`, `Router Scan`, `SharpChrome`, `GMER`, `PCHunter`, `AdFind`, `Bloodhound`, `PowerView`, `Seatbelt` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Dropfiles/RClone na exfiltração; chat usa seguro cyber exfiltrado para pricing. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Conti** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
*Fonte: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 32 chats analisados · [EN](../en/Conti.md)* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
