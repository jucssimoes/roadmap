# AGENTS.md · Roadmap Wehandle 2026

> Table of contents pra agentes. Aponta pra docs específicas conforme a tarefa.

## Pra começar

Sempre leia `CLAUDE.md` no startup. Esse arquivo te ajuda a achar a doc certa pra cada cenário.

## Mapa rápido por tarefa

### Adicionar nova iniciativa
- Template: `prompts/add-initiative.md`
- Schema: `content-model.md`
- Catálogos válidos (módulos, sub-áreas, status, ambientes): `CLAUDE.md`
- Tom de voz: `style-guide.md` § tom de voz
- Onde gravar: `data/initiatives.json` (não no HTML)

### Atualizar status/período
- Template: `prompts/update-initiative.md`
- Em dúvida entre Em piloto e Lançado, prefira **Em piloto** (mais conservador)

### Adicionar embed Figma
- Template: `prompts/add-figma-embed.md`
- Formato: `https://embed.figma.com/design/{fileKey}/{name}?node-id={nodeId}&embed-host=share`
- Pra Figma Make: `https://embed.figma.com/make/{fileKey}/{name}?embed-host=share`

### Mudar arquitetura (faixa, sub-área, status)
- Lê: `architecture.md` + `decisions-log.md`
- Discute com Juliana antes
- Atualiza: `architecture.md`, `decisions-log.md`, `data/initiatives.json`, código HTML
- Registra lição: `lessons-learned.md`

### Reescrever iniciativa técnica em linguagem cliente
- Tom: `style-guide.md` § tom de voz
- Glossário Wehandle: `wehandle-context.md`

### Re-gerar HTML a partir do JSON
- O JS dele lê `initiatives` array hardcoded — substituir pelo conteúdo de `data/initiatives.json`
- Validar: abrir HTML, conferir 5 swim lanes preenchidas, contagens batendo, cards expandindo

## Mapa rápido por dúvida

| Dúvida | Onde achar |
|---|---|
| Por que status no eixo Y? | `decisions-log.md` ADR-004 |
| Por que Lançado no topo? | `architecture.md` § ordem das swim lanes |
| Cores válidas? | `style-guide.md` |
| Posso usar rosa pra status? | `CLAUDE.md` § princípios (não — rosa = módulo GT) |
| Quando é "Interno"? | Só faixa Operação |
| Como agrupar 14 ações? | Iniciativa-mãe + bullets em `details` (ex: Plano 11k) |
| Cliente específico aparece? | Não. "Operação grande" ou "piloto". |

## Arquivos críticos (não mexa sem entender)

- `data/initiatives.json` — fonte de verdade
- `index.html` — output final (raiz do repo)
- `CLAUDE.md` — regras invioláveis
- `decisions-log.md` — append-only

## Fluxo "compounding"

Sempre que descobrir algo novo (erro, padrão, atalho):
1. Resolva a tarefa atual.
2. Adiciona em `lessons-learned.md` com data e contexto.
3. Se for regra inviolável, propõe mudar `CLAUDE.md` à Juliana.
