# Content Model · Schema de iniciativa

## Schema

```ts
interface Initiative {
  id: string;             // ex: "gt-1", "mob-3" — único, módulo + número sequencial
  name: string;           // título cliente-friendly. <60 chars
  shortDesc: string;      // 1 frase descritiva visível no card. <80 chars
  module: 'gt' | 'mob' | 'ehs' | 'op';
  subarea: string;        // sub-área válida do módulo
  env: 'tomador' | 'fornecedor' | 'ambos' | 'interno';
  start: number;          // 1=Jan, 12=Dez
  end: number;            // 1=Jan, 12=Dez. >= start
  status: 'lancado' | 'piloto' | 'dev' | 'definicao' | 'previsto';
  description: string;    // 1-3 frases pro modal
  value?: string;         // 1 frase opcional "valor pro cliente"
  details?: string[];     // bullets opcionais (iniciativa-mãe)
  figma?: boolean;        // true se tem tela mas sem embed (placeholder)
  figmaEmbed?: string;    // URL embed.figma.com (preferido)
}
```

## Regras

### `id`
- `<modulo>-<numero>`. Sequencial, **não reutiliza** número de iniciativa removida.

### `name`
- Linguagem cliente. Verbo no infinitivo OK ou substantivo. Sem nome de cliente, squad, dono. Sem jargão técnico.

### `shortDesc`
- 1 frase ~80 chars, sem ponto final. Foco no benefício ou fluxo.

### `module` + `subarea`
- Catálogo em `CLAUDE.md`. Sub-área deve existir no módulo.
- **Não inventar sub-área** sem aprovação.

### `env`
- **interno** só pra módulo `op`.

### `start` / `end`
- Inclusivo. Mesmo mês = `start = end`.
- Cobrir ciclo todo (discovery + dev + entrega).

### `status`
- Estado atual, não planejado. Em dúvida entre `piloto` e `lancado`: prefira `piloto`.

### `description`
- 1-3 frases. Tom B2B profissional. Sem hype.

### `value` (opcional)
- 1 frase começando com efeito pro cliente. Não force.

### `details` (opcional)
- Array de bullets. Use quando iniciativa-mãe agrega 5+ features.

### `figmaEmbed`
- URL `https://embed.figma.com/design/{fileKey}/{name}?node-id={nodeId}&embed-host=share`
- Figma Make: `https://embed.figma.com/make/{fileKey}/{name}?embed-host=share`
- Cliente NÃO precisa de login.

## Exemplo (gt-14)

```json
{
  "id": "gt-14",
  "name": "Contestação do status de validação",
  "shortDesc": "Fornecedor contesta validação direto na plataforma",
  "module": "gt",
  "subarea": "Central de Documentos",
  "env": "fornecedor",
  "start": 6,
  "end": 8,
  "status": "dev",
  "description": "Quando um documento é invalidado, o Fornecedor pode contestar diretamente na plataforma com argumentação e anexos, sem precisar abrir ticket de suporte. A contestação vai pro time de validação revisar.",
  "value": "Resolução mais rápida de divergências, sem fricção de canal externo.",
  "figmaEmbed": "https://embed.figma.com/design/OQhOWqAEVMs47TAyL81dzZ/Documentos---Contesta%C3%A7%C3%A3o---V1?node-id=0-1&embed-host=share"
}
```

## Exemplo com `details` (op-2)

```json
{
  "id": "op-2",
  "name": "Atendimento mais rápido e com contexto",
  "shortDesc": "Tickets com contexto, abertura em massa e fila otimizada",
  "module": "op",
  "subarea": "Atendimento",
  "env": "interno",
  "start": 4,
  "end": 7,
  "status": "dev",
  "description": "Conjunto de melhorias internas pra absorver picos de volume...",
  "details": [
    "Tickets nascem com doc_id, motivo, histórico e link",
    "Abertura direto da tela do documento",
    "Contestação em massa por planilha",
    "Fila separada de QA aleatório x revalidação",
    "Copiloto IA sugere ação, validador humano decide"
  ],
  "value": "Atendimento absorve mais volume sem perder qualidade — você espera menos."
}
```
