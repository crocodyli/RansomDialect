# Akira — Perfil de Negociação (CTI)

> Maior volume do dataset: 60 chats, 2.408 mensagens. Período: 2023–2025.

---

## Metadados

| Campo | Valor |
|-------|-------|
| Chats | 60 |
| Mensagens totais | 2.408 |
| Msgs ator / vítima | 1.193 / 1.215 |
| Tamanho médio msg. ator | 154,9 caracteres |
| Flexibilidade de preço | **Alta** |
| Intensidade de pressão | **Média-Alta** |
| Sofisticação de provas | **Alta** |

---

## Resumo Executivo

Akira opera como uma **"empresa de suporte técnico"** com scripts altamente padronizados. O tom é profissional e paciente na superfície, mas com escalada de pressão via deadlines de 24h e publicação no blog onion. É um dos grupos mais sofisticados em due diligence financeira e oferece o pacote pós-pagamento mais completo do dataset.

---

## Tom e Estilo de Comunicação

- **Tom:** Corporativo, calmo, quase consultivo — como um helpdesk de TI
- **Persona:** "Suporte Akira" / "auditoria de segurança surpresa"
- **Cadência:** Follow-ups proativos (*"Standing by"*, *"so?"*, *"Waiting for the update"*)
- **Escalada:** Acusa vítima de *"jogar sujo"* ou *"waste our time"* antes de publicar

**Abertura típica:**
> *"Hello. You've reached an Akira support chat. Currently, we are preparing the list of data we took from your network. For now you have to know that dealing with us is the best possible way to settle this quick and cheap."*

Variante sarcástica:
> *"Congratulations, you have passed a surprise information security audit and become a victim of ransomware."*

---

## Fluxo de Negociação

```
1. Abertura "support chat" + pedido de autorização do negociador
2. Envio de lista de arquivos exfiltrados (.rar / privnote)
3. Pacote de 5 serviços numerados (decryptor, remoção, relatório, etc.)
4. Due diligence financeira (extratos, seguro cyber, auditorias)
5. Test decrypt: 2–3 arquivos criptografados (≤10 MB)
6. Prova de posse: 2–3 arquivos da lista sob demanda
7. Negociação de preço com "upper management"
8. Pagamento BTC com test transaction
9. Entrega: decryptor CLI (--secret key), deletion logs, relatório técnico
```

---

## Estratégia de Precificação

- **Ancoragem:** Valores de $80K a $2,4M observados no dataset
- **Flexibilidade:** Alta — aceita contra-ofertas significativas (ex.: $2,4M → $1M, ~58% desconto)
- **Modular:** Preço pode ser negociado por partes (*"whole deal or in parts"*)
- **Alavancas:** Seguro cyber, liquidez da vítima, velocidade de pagamento
- **Tática:** *"upper management"* como autoridade que aprova descontos

---

## Prova de Descriptografia e Exfiltração

1. Lista de arquivos exfiltrados via privnote ou anexo direto
2. 2–3 arquivos criptografados uploadados → devolvidos descriptografados
3. 2–3 arquivos da lista como prova de posse
4. Entrega de `unlocker.7z` / `unlockers.7z` com instruções CLI

---

## Táticas de Pressão

- Publicação no blog onion após silêncio prolongado
- Deadline de 24h para resposta
- Acusação de má-fé: *"Your attempts to waste our time could force our exit"*
- Publica **antes** do acordo se vítima demora
- Ameaça de upload de dados adicionais

---

## TTPs na Fase de Negociação

- Due diligence financeira ativa (pede extratos, apólice de seguro)
- Test transaction BTC antes do pagamento integral
- Relatório pós-pagamento detalhado (kerberoasting, Forti VPN, etc.)
- Deletion logs entregues em .rar
- Decryptor com parâmetro `--secret` explícito

---

## IOCs Comportamentais (Indicadores Linguísticos)

| Indicador | Exemplo |
|-----------|---------|
| Prefixo `>` nas mensagens | `> Standing by.` |
| "support chat" | Abertura padrão |
| "dealing with us is the best possible way" | Script de abertura |
| "whole deal or in parts" | Negociação modular |
| "please wait" / "wait a bit" | 23+ ocorrências no dataset |
| "are you going to work with us?" | Pressão de engajamento |
| Referência a seguro cyber | Due diligence |
| privnote.com links | Entrega de listas |

---

## Insights Críticos

1. **Script reutilizado por anos** — frases idênticas em chats de 2023 e 2025
2. **"Upper management"** é alavanca retórica, não necessariamente hierarquia real
3. **Publicação pré-acordo** como punição por demora — não espera falha total da negociação
4. **Maior taxa de follow-up proativo** do dataset — operador não espera a vítima
5. **Descontos de até 58%** quando vítima demonstra liquidez limitada com documentação

---

## Classificação

```
Estilo:         Corporativo-Profissional
Flexibilidade:  Alta
Pressão:        Média-Alta
Sofisticação:   Alta
Maturidade:     Muito Alta (2023–2025)
```

---

## Nota de Resgate (ThreatLabz)

> Mapeamento para atribuição precoce (T+0). Fonte: [ThreatLabz/ransomware_notes](https://github.com/ThreatLabz/ransomware_notes) — notas **não** incluídas neste repositório, apenas referenciadas.

| Campo | Detalhe |
|-------|---------|
| **Pasta ThreatLabz** | [`akira/`](https://github.com/ThreatLabz/ransomware_notes/tree/main/akira) |
| **Arquivos típicos** | `akira_readme.txt`, `akira_readme_2.txt`, `akira_readme_3.txt` |
| **Extensão / artefato** | `.akira` |
| **Frases-chave da nota** | *"surprise information security audit"*, *"internal infrastructure... fully or partially dead"*, *"backups... completely removed"* |
| **Continuidade com o chat** | Mesma persona de suporte técnico; a nota anuncia exfiltração e destruição de backups antes do portal de chat. |

**Se a nota contém...** → confirma **Akira** antes de abrir o portal de negociação.

---

## Artefatos Pré-Extorsão (RTM)

> Fase **T-7d → T-1h** — tools observadas em intrusões que levaram ao deploy. Fonte: [Ransomware-Tool-Matrix](https://github.com/BushidoUK/Ransomware-Tool-Matrix) — **não vendidas** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **GroupProfile RTM** | [`Akira`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/GroupProfiles/Akira.md) |
| **Tools-chave** | `Advanced IP Scanner`, `AnyDesk`, `PowerTool`, `DonPAPI`, `Impacket`, `Cloudflared`, `FileZilla`, `Masscan`, `MobaXterm`, `Zemana Anti-Rootkit` |
| **Matrizes** | [`CredentialTheft`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/CredentialTheft.md), [`DefenseEvasion`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DefenseEvasion.md), [`DiscoveryEnum`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/DiscoveryEnum.md), [`Exfiltration`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Exfiltration.md), [`Networking`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Networking.md), [`Offsec`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/Offsec.md), [`RMM-Tools`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/Tools/RMM-Tools.md) |
| **Checklist hunt** | [`RTM_ThreatHunt_Checklist.csv`](https://github.com/BushidoUK/Ransomware-Tool-Matrix/blob/main/RTM_ThreatHunt_Checklist.csv) |
| **Continuidade com chat/nota** | RClone/temp.sh na intrusão explicam privnote e listas de exfiltração no chat. |

**Se estes artefatos aparecem no ambiente** → reforça atribuição a **Akira** junto com nota e perfil de negociação.

---

## Kill Chain MITRE (ThreatActors-TTPs)

> TTPs, CVEs e histórico pré-extorsão. Fonte: [crocodyli/ThreatActors-TTPs](https://github.com/crocodyli/ThreatActors-TTPs) — **não vendido** neste repositório.

| Campo | Detalhe |
|-------|---------|
| **Pasta** | [`Akira/`](https://github.com/crocodyli/ThreatActors-TTPs/tree/main/Akira) |
| **TTPs (MITRE)** | [`Akira-TTP`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Akira/Akira-TTP.md) |
| **CVEs** | [`CVEs`](https://github.com/crocodyli/ThreatActors-TTPs/blob/main/Akira/CVEs-Akira.md) |
| **TTPs-chave** | *T1190 — Exploração de VPN/edge (Cisco, SonicWall)*; *T1133 — Acesso remoto com credenciais roubadas*; *T1486 — Criptografia + exfiltração pré-ransom* |

Referência cruzada com [ransomware.live](https://www.ransomware.live/) e matriz RTM.

---

*Fonte: [Ransomchats](https://github.com/Casualtek/Ransomchats) — 60 chats analisados · [EN](../en/Akira.md) · Notas: [ThreatLabz](https://github.com/ThreatLabz/ransomware_notes) · Ops: [RTM](https://github.com/BushidoUK/Ransomware-Tool-Matrix) · [TTPs](https://github.com/crocodyli/ThreatActors-TTPs)*
