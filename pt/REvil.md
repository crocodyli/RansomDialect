# REvil (Sodinokibi) — Perfil de Negociação (CTI)

> 20 chats, 1.065 mensagens. Período: 2020–2021.

---

## Metadados

| Campo | Valor |
|-------|-------|
| Chats | 20 |
| Mensagens totais | 1.065 |
| Flexibilidade de preço | **Baixa-Média** |
| Intensidade de pressão | **Alta** |
| Sofisticação de provas | **Alta** |

---

## Resumo Executivo

REvil representa o **RaaS de alta maturidade** da era 2020–2021. Contrapõe argumentos financeiros da vítima com documentos exfiltrados da própria empresa. Despreza narrativas de crise (COVID) como *"cover"*. Esconde publicação no blog durante negociação ativa e usa publicação escalonada por tipo de dado como pressão calibrada.

---

## Tom e Estilo de Comunicação

- **Tom:** Profissional, frio, condescendente — especialmente com advogados
- **Persona:** Negociador experiente com *"deals with many companies every day"*
- **Tática retórica:** *"you write a lot of text but all of this doesnt matter"*
- **Contra-argumentação:** Usa docs roubados para refutar alegações da vítima

**Abertura típica:**
> Resposta a advogado com análise financeira prévia da vítima. Esconde post do blog durante talks ativos.

---

## Fluxo de Negociação

```
1. Análise financeira prévia (docs exfiltrados, seguro, receita)
2. Preço inicial alto ($7,5M observado)
3. Esconde publicação no blog durante negociação
4. Contra-argumenta com documentos exfiltrados
5. Ajustes incrementais: $7,5M → $6,75M (rápido) → $5M
6. Recusa ofertas baixas ($500K–$1M) como "ridiculous"
7. Publicação escalonada se falha: PII → clientes → specs
8. Extensão de timer (+7 dias) como concessão rara
```

---

## Estratégia de Precificação

- **Ancoragem:** $7,5M → $5M após ajustes
- **Recusa:** $500K–$1M categoricamente como *"ridiculous"*
- **Desconto:** Por velocidade de pagamento, não por capacidade
- **Contra-argumento:** Devolve relatório financeiro exfiltrado + manual de seguro para refutar alegações de insolvência

---

## Prova de Descriptografia e Exfiltração

1. Devolve relatório financeiro exfiltrado como prova de acesso
2. Manual de seguro cyber da vítima como demonstração
3. Publicação faseada como prova de capacidade de dano

---

## Táticas de Pressão

- Dump de passwords/email do CEO
- Publicação por partes: PII → dados de clientes → especificações técnicas
- Timer com extensão rara (+7 dias) como concessão
- Desprezo por narrativa COVID: *"cover"*
- Esconde blog durante talks — revela controle sobre publicação

---

## TTPs na Fase de Negociação

- Engajamento via advogado (canal preferido)
- Usa docs exfiltrados ativamente contra argumentos da vítima
- Pacing de publicação calibrado por tipo de dado
- Timer como mecanismo de urgência com extensão negociável
- Análise financeira profunda pré-negociação

---

## IOCs Comportamentais

| Indicador | Exemplo |
|-----------|---------|
| "We have deals with many companies every day" | Experiência declarada |
| "price updated to $5M" | Ajuste formal |
| "you write a lot of text but all of this doesnt matter" | Condescendência |
| "ridiculous" (para ofertas baixas) | Rejeição categorica |
| Referência a COVID como "cover" | Desprezo por narrativas |

---

## Insights Críticos

1. **Usa documentos da própria vítima** para refutar argumentos financeiros — TTP sofisticado
2. **Esconde blog durante negociação** — demonstra controle e usa como concessão
3. **Publicação escalonada por tipo** — PII primeiro, depois clientes, depois specs
4. **Extensão de timer é concessão rara** — não oferecida facilmente
5. **Despreza recovery firms e advogados** mas negocia com eles quando necessário

---

## Classificação

```
Estilo:         Sarcástico-Psicológico / Corporativo
Flexibilidade:  Baixa-Média
Pressão:        Alta
Sofisticação:   Alta
Maturidade:     Muito Alta (grupo desmantelado 2021)
```

---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`revil/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/revil) |
| **Arquivos típicos** | `revil1.txt`, `revil2.txt`, `revil3.txt` |
| **Extensão / artefato** | `{EXT} (variável por campanha)` |
| **Frases-chave da nota** | *"Welcome. Again."*, *"What guarantees?"*, *"NEVER restore without instructions"* |
| **Continuidade com o chat** | Nota estruturada em FAQ; chat torna-se condescendente e refuta com docs roubados. |

**Se a nota contém...** → confirma **REvil** antes de abrir o portal de negociação.

---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | — |
| **Tools-chave** | `AdFind`, `Bloodhound`, `PrivatLab`, `RClone`, `Sendspace`, `BITSAdmin`, `Cobalt Strike` |
| **Matrizes** | [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`LOLBAS`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/LOLBAS.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Exfil tools variados; chat condescendente com docs roubados. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **REvil** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
*Fonte: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 20 chats analisados · [EN](../en/REvil.md)* · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)
