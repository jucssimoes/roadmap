# Style Guide

## Paleta

### Wehandle brand
| Token | Hex | Uso |
|---|---|---|
| Rosa primário | `#C0185C` | Marca · módulo GT · linha "hoje" · borda do header |
| Rosa fundo suave | `#FBEAF0` | Background de destaque · módulo GT |
| Rosa borda | `#ED93B1` | Bordas em contexto rosa |
| Rosa texto | `#72243E` | Texto sobre rosa claro |
| Rosa texto forte | `#4B1528` | Alta hierarquia |
| Marinho | `#0D1B3E` | Header text · módulo Mobilização |

### Status
| Status | Cor | Background |
|---|---|---|
| Lançado | `#1D9E75` | `#E1F5EE` |
| Em piloto | `#8B5CF6` | `#F5F3FF` |
| Em desenvolvimento | `#378ADD` | `#E6F1FB` |
| Em definição | `#EF9F27` | `#FAEEDA` |
| Previsto | `#888780` | `#F5F4F0` |

### Módulos
| Módulo | Cor | Background |
|---|---|---|
| GT | `#C0185C` | `#FBEAF0` |
| Mobilização | `#0D1B3E` | `#DBE2EF` |
| EHS em Campo | `#0F766E` | `#CCFBF1` |
| Operação | `#5F5E5A` | `#EEEDE8` |

## Regras invioláveis de cor

1. **Brand colors (rosa, marinho) nunca codificam status, risco ou erro.**
2. **Status colors são separadas e semânticas.** 5 cores fixas.
3. **Módulo novo:** escolhe cor que não conflite com status.

## Tipografia

- Família: Inter (Google Fonts)
- Pesos: 400 / 600 / 700 / 800

## Tom de voz

### Princípios
1. Direto e B2B profissional. Sem hype, sem emoji decorativo.
2. Foco no benefício, não na implementação.
3. Linguagem positiva. Nunca admitir defeito.
4. Substantivos ou infinitivo. Sem call-to-action ("Clique aqui...")

### Comparações

| ❌ Não faça | ✅ Faça |
|---|---|
| Menos invalidação, mais clareza | Validações mais claras e robustas |
| Acabamos com o problema dos tickets | Atendimento mais rápido e com contexto |
| Cliente final | Tomador / Fornecedor / Colaborador |
| Lançamento incrível! | Lançado |
| 🚀 Revolucionamos... | (não use emoji em conteúdo) |

### Palavras a evitar
genuinamente · honestamente · basicamente · revolucionar · transformar · fantástico · incrível · "a gente"

### Palavras preferidas
operação · fluxo · previsto · lançado · consolidado · validação · conformidade · habilitação · mobilização

## Componentes

### Card
- Altura: 54px
- Border 1px da cor do status
- Barra lateral esquerda 4px
- Hover: `translateY(-1px)` + box-shadow

### Module group (chave)
- Faixa lateral 4px da cor do módulo
- Background gradient suave
- Header textual em uppercase

### Modal
- Max width: 600px
- Padding: 28px 32px
- Backdrop: `rgba(13, 27, 62, 0.6)` + blur 4px

## Acessibilidade

- Contraste WCAG AA mínimo
- Modal fechável com Esc
- Aria labels via `title`
