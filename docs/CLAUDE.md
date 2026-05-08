# CLAUDE.md · Roadmap Wehandle 2026

> Rules + contexto essencial. Sempre leia este arquivo no startup.

## O que é este projeto

Roadmap anual da BU Gestão de Terceiros da Wehandle, **compartilhado com TODOS os clientes**. Mostra iniciativas em 4 faixas, organizadas por status (5 swim lanes) com timeline mensal Jan→Dez/26.

Owner: Juliana Simões (GM BU GT). Toda decisão estrutural passa por ela.

Output principal: `index.html` na raiz do repo — auto-contido, abre em qualquer navegador.

## Princípios inegociáveis

1. **Cliente, não squad.** Todo nome, descrição e tag em **linguagem de cliente B2B**. Nunca expor "GT2", "Squad Ionita", "Wellington", nomes técnicos de épicos Jira ou jargão interno.

2. **Status manda, módulo é contexto.** Eixo Y do roadmap é **status** (Previsto · Em definição · Em desenvolvimento · Em piloto · Lançado), eixo X é **mês**. Módulo aparece como tag colorida + sub-grupo dentro de cada swim lane.

3. **Terminologia oficial:** Tomador / Fornecedor / Colaborador. Nunca "cliente/prestador/contratado".

4. **Brand color tem regra.** Rosa Wehandle (`#C0185C`) e marinho (`#0D1B3E`) podem codificar **módulo**, nunca status/risco/erro. Cores semânticas são separadas.

5. **Não admitir defeito.** Linguagem do roadmap é evolução positiva. Nunca dizer "menos invalidação" — diga "validações mais claras e robustas".

6. **Toda decisão estrutural exige aprovação da Juliana.** Mudança em status, faixas, ambientes, anatomia do card → discutir antes de implementar.

7. **Conteúdo separado da apresentação.** Edite `data/initiatives.json`, sincronize a array no `<script>` do `index.html`. Nunca edite o HTML diretamente como única fonte.

## Quando pedir clarificação vs assumir

**Assuma e siga** quando: faltar shortDesc/descrição (escreva proposta) · faltar valor pro cliente (opcional) · sub-área tiver candidato óbvio.

**Pergunte antes** quando: ambiente não estiver claro · período sem fonte · status atual incerto · nova sub-área seria criada · novo módulo · iniciativa duplicada.

Use AskUserQuestion com 2-4 opções claras. Máximo 3 perguntas por turno (ela fica saturada).

## Catálogo de módulos

- **GT** (rosa) — Gestão de Terceiros · 19 iniciativas · 7 sub-áreas: Configurações · Serviços · Colaboradores · Central de Documentos · Mensagerias · BIs - relatórios · Internacionalização da plataforma
- **Mobilização** (marinho) — 9 iniciativas · 3 sub-áreas: Acessos · Integração de Segurança · Crachás
- **EHS em Campo** (teal) — 2 iniciativas · 1 sub-área: Auditoria em Campo
- **Evoluções de Operação** (warm gray) — 4 iniciativas · 3 sub-áreas: Atendimento · Validação · Dados *(faixa interna)*

## Catálogo de status

| Status | Significado |
|---|---|
| Previsto | Tá no plano de 2026, ainda não começou |
| Em definição | Equipe definindo escopo/regras (discovery) |
| Em desenvolvimento | Time construindo |
| Em piloto | Entregue, em teste com cliente beta antes do lançamento geral |
| Lançado | Disponível pra todos os clientes |

## Catálogo de ambientes

| Badge | Ambiente |
|---|---|
| T | Tomador |
| F | Fornecedor |
| T·F | Tomador + Fornecedor |
| I | Interno Wehandle (faixa Operação) |

## Anti-padrões (não faça)

- ❌ Adicionar campo novo no JSON sem atualizar `content-model.md`
- ❌ Mudar paleta sem atualizar `style-guide.md`
- ❌ Codificar status com cor de marca (rosa/marinho)
- ❌ Listar features granulares como cards separados (use iniciativa-mãe + bullets)
- ❌ Mostrar squad/dono no roadmap público
- ❌ Citar cliente específico (Klabin, Scala) — fala em "operação grande" ou "piloto"
