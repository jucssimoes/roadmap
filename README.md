[README.md](https://github.com/user-attachments/files/27503054/README.md)
# Roadmap Wehandle 2026

Roadmap anual da BU Gestão de Terceiros da Wehandle — compartilhado com clientes.

**Acessar online:** https://jucssimoes.github.io/roadmap/ *(ativar GitHub Pages — ver instruções abaixo)*

## O que tem aqui

```
.
├── index.html           # Roadmap em HTML (auto-contido, abre em qualquer navegador)
├── data/
│   └── initiatives.json # Fonte de verdade — 34 iniciativas em 4 faixas
└── docs/                # Documentação pra manter o roadmap
    ├── CLAUDE.md            # rules invioláveis (leia primeiro)
    ├── AGENTS.md            # table of contents pra docs
    ├── architecture.md      # decisões arquiteturais
    ├── content-model.md     # schema de iniciativa
    ├── style-guide.md       # paleta + tom de voz
    ├── decisions-log.md     # 17 ADRs cronológicos
    ├── lessons-learned.md   # erros e correções (compounding engineering)
    ├── content-collection.md # processo de coleta por módulo
    ├── wehandle-context.md  # contexto da empresa, módulos, terminologia
    └── prompts/             # templates pra tarefas comuns
        ├── add-initiative.md
        ├── update-initiative.md
        └── add-figma-embed.md
```

## Como atualizar o roadmap

1. Edite `data/initiatives.json` (fonte de verdade).
2. Sincronize a array `initiatives` dentro do `<script>` do `index.html` (cole o conteúdo do `initiatives` array do JSON).
3. Atualize o "Atualizado em DD/MM" no header do HTML.
4. Commit + push. Se Pages estiver ativo, o site atualiza sozinho em ~1 min.

## Como ativar GitHub Pages

1. Settings → Pages
2. Branch: `main` · Folder: `/ (root)`
3. Save
4. Aguardar 1 min, acessar `https://jucssimoes.github.io/roadmap/`

> O HTML tem meta tag `noindex,nofollow` então não aparece em busca pública. URL pode ser compartilhada com clientes sem aparecer no Google.

## Como usar como agente (próxima sessão)

Se for trabalhar este roadmap em uma nova sessão (sua ou de IA), leia nessa ordem:

1. `docs/CLAUDE.md` — regras invioláveis
2. `docs/AGENTS.md` — table of contents
3. `docs/wehandle-context.md` — contexto Wehandle
4. `docs/architecture.md` — decisões já tomadas

Pra tarefas comuns (adicionar iniciativa, atualizar status, embedar Figma), siga os templates em `docs/prompts/`.

## Stack

HTML + CSS + Vanilla JS. Zero dependências de build, zero npm. Embeds Figma via `embed.figma.com` (sem login do cliente).

## Histórico

- **v1** · 07/05/2026 — versão inicial. 34 iniciativas, 12 com Figma.

## Owner

Juliana Simões (GM BU GT) · juliana.simoes@wehandle.com.br
