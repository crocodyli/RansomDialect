# Cloak — Perfil de Negociação (CTI)

> 2 chats, 120 mensagens. Período: 2023.

---

## Resumo Executivo

Cloak possui a **maior formalização procedural do dataset**: 6 regras + plano de 11 passos numerados antes de qualquer preço. Gatekeeping de autoridade (*"authorized representative"*) e venda de dados a terceiros como pressão alternativa ao leak público.

## Tom e Comunicação

- **Estilo:** Formal/procedural — manual operacional
- **Abertura:** Mensagem longa com regras e passos antes de preço
- **Marcadores:** *"Anonymous"* / *"Client"*, *"authorized representative"*, *"mutual respect is the key"*

## Negociação

| Aspecto | Comportamento |
|---------|---------------|
| Preço | Não divulgado até representante autorizado; *"we know about your income"* |
| Prova | Passos 3–5: 2 arquivos ≤5MB para reverse decryption |
| Pressão | Venda de dados a terceiros com timer; amostras no leak site onion |
| Gatekeeping | Recusa negociar com admins ou equipes de limpeza |

## Insights

1. Maior formalização procedural do dataset
2. Venda a terceiros como pressão alternativa
3. Recusa não-autorizados categoricamente
4. Múltiplos domínios/empresas no mesmo chat
5. Foco em processo sobre resultado

```
Flexibilidade: Baixa | Pressão: Alta | Sofisticação: Média
```
---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`cloak/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/cloak) |
| **Arquivos típicos** | `readme_for_unlock.txt`, `readme_for_unlock_oct2024.txt`, `readme_for_unlock_nov2024.txt` |
| **Extensão / artefato** | `.cloak / .pwned` |
| **Frases-chave da nota** | *"ATTENTION"*, *"network is hacked and files are encrypted"*, *"accounting and other internal documentation"* |
| **Continuidade com o chat** | Nota lista exfiltração; chat impõe 6 regras + 11 passos antes do preço. |

**Se a nota contém...** → confirma **Cloak** antes de abrir o portal de negociação.
---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — hunt/IR durante crise. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem entrada dedicada no RTM (jun/2026) |
| **Checklist geral** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | Sem matriz RTM dedicada; chat procedural (6 regras + 11 passos) é o IOC principal. |

Índice: [`operational_mapping.json`](../operational_mapping.json)
---

## Kill Chain MITRE (ThreatActors-TTPs)

> Fonte externa: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs).

| Campo | Detalhe |
|-------|---------|
| **Status** | Sem pasta correspondente (jun/2026) |
| **Alternativa** | Consultar matrizes RTM e perfil de negociação deste repositório |

Índice: [`operational_mapping.json`](../operational_mapping.json)
