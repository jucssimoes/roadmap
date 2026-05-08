# Architecture · Roadmap 2026

## Filosofia

Pesquisa que fundamentou as decisões: ProdPad (Janna Bastow — Now/Next/Later) · ProductPlan (theme-based) · pesquisa B2B SaaS · padrão Linear/ProductBoard/Notion. Convergência: **status como eixo principal + módulo como tag** é o padrão moderno pra roadmap cliente B2B.

## Eixos

- **X = mês**, granularidade **mensal**, **Jan→Dez 2026**, com linha "hoje" sempre visível.
- **Y = status**, 5 swim lanes (de cima pra baixo, ordem cronológica de lifecycle):
  1. Lançado
  2. Em piloto
  3. Em desenvolvimento
  4. Em definição
  5. Previsto

**Por que essa ordem:** lifecycle natural — iniciativas progridem "subindo" entre swim lanes. Cliente abre o roadmap querendo ver o que está "saindo agora" (Lançado/Em piloto no topo).

**Toggle "ocultar lançadas"** no header reduz ruído.

## 4 Faixas (módulos macro)

| Faixa | Cor | Iniciativas | Sub-áreas |
|---|---|---|---|
| GT — Gestão de Terceiros | Rosa Wehandle | 19 | 7 |
| Mobilização | Marinho Wehandle | 9 | 3 |
| EHS em Campo | Teal | 2 | 1 |
| Evoluções de Operação | Warm gray | 4 | 3 |

**Justificativa pras 4 faixas:** as 3 primeiras são módulos do produto. A 4ª é narrativa nova — atacando dores operacionais (atendimento, validação, dados) com automações internas.

**Ordem fixa dentro de cada swim lane:** GT → Mobilização → EHS → Operação.

## Sub-áreas

### GT (7)
Configurações · Serviços · Colaboradores · Central de Documentos · Mensagerias · BIs - relatórios · Internacionalização da plataforma

### Mobilização (3)
Acessos · Integração de Segurança · Crachás

### EHS em Campo (1)
Auditoria em Campo

### Evoluções de Operação (3)
Atendimento · Validação · Dados

**Visual:** dentro de cada swim lane, cards do mesmo módulo+sub-área são agrupados com **chave colorida** (faixa lateral 4px da cor do módulo) + **header textual** ("GT · Configurações").

## Card de iniciativa

### Compacto
```
[barra colorida de status] | Nome da iniciativa            [T] [📐]
                            Descrição curta · 1 linha
```
- Cor da barra = cor do **status atual**
- Comprimento = **período** (mês início → fim)
- Badge T/F/T·F/I = ambiente
- Ícone 📐 = tem Figma embedado

### Expandido (modal)
- Tags do topo: módulo, sub-área, ambiente
- Nome
- Período + Status atual
- Descrição completa
- Valor pro cliente (opcional)
- O que está incluído (lista de bullets — pra iniciativa-mãe)
- Tela do design (iframe Figma se `figmaEmbed`)

## Cores

### Status (barras + swim lane labels)
| Status | Cor | Background |
|---|---|---|
| Lançado | `#1D9E75` | `#E1F5EE` |
| Em piloto | `#8B5CF6` | `#F5F3FF` |
| Em desenvolvimento | `#378ADD` | `#E6F1FB` |
| Em definição | `#EF9F27` | `#FAEEDA` |
| Previsto | `#888780` | `#F5F4F0` |

### Módulos (chaves)
| Módulo | Cor | Background |
|---|---|---|
| GT | `#C0185C` (rosa Wehandle) | `#FBEAF0` |
| Mobilização | `#0D1B3E` (marinho Wehandle) | `#DBE2EF` |
| EHS em Campo | `#0F766E` (teal) | `#CCFBF1` |
| Operação | `#5F5E5A` (warm gray) | `#EEEDE8` |

### Brand
- Linha "hoje": rosa
- Borda inferior do header: rosa
- Header text: marinho

## Período

**Decisão:** cobrir o **ciclo todo** (discovery + dev + entrega). Honesto, não esconde discovery.

## Iniciativas que NÃO aparecem

- Trabalho client-specific (ex.: "Crachá Klabin")
- Refactors técnicos puros
- Permissão de Trabalho (Prothera) — fora de escopo 2026

## Ambiente "Interno Wehandle"

Toda iniciativa de **Evoluções de Operação** = ambiente "I". Única faixa onde isso aparece.
