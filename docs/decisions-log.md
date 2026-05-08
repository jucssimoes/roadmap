# Decisions Log · ADRs

Histórico cronológico de decisões. **Append-only**.

## ADR-001 · Roadmap pra cliente público
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Roadmap único, compartilhado com todos os clientes. Sem nome de cliente específico nos cards.

## ADR-002 · 4 faixas (3 módulos do produto + 1 narrativa "Evoluções de Operação")
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** GT, Mobilização, EHS em Campo + Evoluções de Operação (faixa interna com Atendimento/Validação/Dados).

## ADR-003 · 5 status canônicos
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Previsto · Em definição · Em desenvolvimento · Em piloto · Lançado. "Em piloto" = beta com cliente; "Lançado" = disponível pra todos.

## ADR-004 · Status como eixo Y, módulo como tag (HÍBRIDO)
**Data:** 07/05/2026 · **Status:** Aceito · **Supersede:** primeiro modelo "módulo no Y"
**Contexto:** Pesquisa em 4 fontes (ProdPad, ProductPlan, B2B SaaS) confirmou que padrão moderno é status/horizonte como eixo principal.
**Decisão:** Eixo Y = 5 swim lanes de status. Módulo aparece como tag colorida + sub-grupo dentro de cada swim lane.

## ADR-005 · Mês visível no eixo X
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Manter eixo X mensal Jan→Dez/2026 com linha "hoje". Compromisso entre flexibilidade (Now/Next/Later puro) e previsibilidade (B2B com data).

## ADR-006 · Sub-grupos por módulo + sub-área (chaves coloridas)
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Dentro de cada swim lane, cards agrupados por (módulo, sub-área), com header textual + faixa lateral 4px da cor do módulo.

## ADR-007 · Cor da barra = cor do status (sem % de progresso)
**Data:** 07/05/2026 · **Status:** Aceito · **Supersede:** "barra com % de progresso"
**Decisão:** Barra mostra **período** com cor **igual à cor do status atual**. Sem preenchimento parcial.

## ADR-008 · Lançadas continuam visíveis com toggle pra ocultar
**Data:** 07/05/2026 · **Status:** Aceito

## ADR-009 · Ambiente "Interno Wehandle" como 4º badge
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Badge "I" (cinza-escuro) aplicado a toda iniciativa de Operação.

## ADR-010 · Paleta de módulos = cores Wehandle + complementares
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** GT=Rosa, Mobilização=Marinho, EHS=Teal, Operação=Warm gray. Brand colors **nunca** codificam status/risco.

## ADR-011 · Squad/dono não aparece no roadmap
**Data:** 07/05/2026 · **Status:** Aceito

## ADR-012 · Cliente específico (Klabin, Scala) não aparece
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Cards não citam cliente nominado. Use "operação grande" ou "piloto".

## ADR-013 · Period = ciclo todo (não só dev+entrega)
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Mostrar período completo, do discovery até entrega. Honesto, não esconde discovery.

## ADR-014 · Embed Figma via embed.figma.com (sem login)
**Data:** 07/05/2026 · **Status:** Aceito · **Supersede:** "exportar PNGs manualmente"
**Decisão:** Campo `figmaEmbed` no schema. Modal renderiza iframe inline. Cliente sem login.

## ADR-015 · Iniciativa-mãe quando há 5+ ações detalhadas
**Data:** 07/05/2026 · **Status:** Aceito
**Contexto:** Plano 11k tinha 14 ações granulares.
**Decisão:** Agrupar em **iniciativas-mãe** com bullets em `details`. Estratégias internas (CORTA/AGUENTA/ENXERGA) **não aparecem**.

## ADR-016 · Vocabulário positivo
**Data:** 07/05/2026 · **Status:** Aceito
**Decisão:** Sempre comunicar **evolução positiva**, nunca admitir defeito. Renomeado "Menos invalidação, mais clareza" → "Validações mais claras e robustas".

## ADR-017 · Letter badges em vez de emoji
**Data:** 07/05/2026 · **Status:** Aceito · **Supersede:** emojis 🏢/🔧/🔄
**Decisão:** Letter badges em pill cinza neutra: "T", "F", "T·F", "I". Ícone Figma virou SVG inline.

## Próximas decisões em aberto

- Q3+Q4 do GT (Juliana vai passando aos poucos)
- Renomear gt-1 vs gt-2 pra distinguir as "duas formas de convite a fornecedor"
