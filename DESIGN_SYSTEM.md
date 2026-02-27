# Design System — Jonas Leonardo Portfolio
**Especificação técnica completa para replicação, expansão e handoff para agências ou devs.**

---

## 1. Identidade Visual

### Paleta de Cores

| Token | Hex | Uso |
|---|---|---|
| `--ivory` | `#F2F5EA` | Background principal |
| `--ivory-dark` | `#E8EDD8` | Background alternativo leve |
| `--jet` | `#2C363F` | Texto principal, seções dark |
| `--jet-light` | `#4A5A65` | Texto secundário, labels |
| `--rose` | `#E75A7C` | Acento primário, CTAs, destaques |
| `--rose-light` | `#F2A0B4` | Acento suave, hover states |
| `--rose-pale` | `#FAE0E6` | Background de insight cards |
| `--dust` | `#D6DBD2` | Bordas, divisórias, grid de gráficos |
| `--dust-dark` | `#B8C0B4` | Labels mono, textos terciários |
| `--sage` | `#BBC7A4` | Acento secundário, dados históricos |
| `--sage-dark` | `#8FA07A` | Versão saturada do sage |
| `--sage-light` | `#D8E2C8` | Versão clara do sage |
| `--white` | `#FFFFFF` | Cards, superfícies elevadas |

**Lógica cromática:**
- **Ivory** como base cria sensação editorial, não digital-genérica
- **Rose** é o acento único — nunca use dois acentos competing
- **Jet** nas seções dark cria ritmo visual sem usar preto puro
- **Sage** sempre para dados históricos/secundários vs. Rose para dados primários/projetados

---

## 2. Tipografia

### Famílias

| Família | Peso | Uso | Import |
|---|---|---|---|
| **Playfair Display** | 400, 700, 900 (regular + italic) | Títulos, números grandes, brand | Google Fonts |
| **DM Sans** | 300, 400, 500 | Corpo de texto, descrições | Google Fonts |
| **DM Mono** | 400, 500 | Labels, tags, valores de dados, código | Google Fonts |

```html
<!-- Import obrigatório no <head> -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
```

### Escala Tipográfica

| Elemento | Família | Tamanho | Peso | Letter-spacing |
|---|---|---|---|---|
| H1 Hero | Playfair Display | `clamp(48px, 5vw, 74px)` | 900 | `-2px` |
| H2 Section | Playfair Display | `clamp(26px, 2.8vw, 42px)` | 700 | `-1px` |
| H3 Card | Playfair Display | `18–24px` | 700 | `-0.4px` |
| Números KPI | Playfair Display | `30–40px` | 900 | `-1.5px` |
| Body | DM Sans | `15px` | 300–400 | normal |
| Body small | DM Sans | `13–14px` | 300 | normal |
| Label / Tag | DM Mono | `9–10px` | 400–500 | `1.5–2.5px` |
| Código | DM Mono | `11px` | 400 | normal |

**Regra:** Labels e tags em DM Mono são **sempre uppercase** com `letter-spacing` generoso.
O `<em>` em títulos Playfair sempre em `--rose` para criar ritmo visual.

---

## 3. Espaçamento e Layout

### Grid

```
Desktop: padding lateral de 64px em todas as seções
Mobile: padding lateral de 24px (adicionar media query)
Gap entre células: 2px (cria efeito de "tiling" editorial)
```

### Sistema de Grid

| Classe | Colunas | Uso |
|---|---|---|
| `.grid-2` | `1fr 1fr` | Charts lado a lado, comparações |
| `.grid-3` | `1fr 1fr 1fr` | Decision cards, skill cards |
| `.grid-1-2` | `1fr 2fr` | Sidebar + conteúdo principal |
| `.grid-2-1` | `2fr 1fr` | Conteúdo + sidebar |
| `.skill-grid` | `repeat(4, 1fr)` | Cards de habilidades |
| `.kpi-row` | `repeat(4, 1fr)` | Métricas em linha |
| `.contact-grid` | `repeat(3, 1fr)` | Cards de contato |
| Section header | `100px 1fr` | Número + conteúdo |

### Seções

| Elemento | Valor |
|---|---|
| Section padding | `96px 64px` |
| Hero padding | `120px 64px 80px` |
| Card padding (grande) | `36px 36px 28px` |
| Card padding (médio) | `28px 24px` |
| Topbar height | `52px` |

---

## 4. Componentes

### Topbar
```css
position: fixed; top: 0; z-index: 100;
background: var(--ivory); border-bottom: 1px solid var(--dust);
height: 52px; padding: 0 64px;
```
- Logo: dot rose + label DM Mono uppercase
- Nav: links DM Mono 10px uppercase com hover `--rose`

### Hero Stats Grid
```
2×2 grid, gap: 2px
Card featured: background --jet
Card rose: background --rose
Cards neutros: background --white, border --dust
```

### Section Header Pattern
```
grid-template-columns: 100px 1fr
Número decorativo: Playfair 80px, color --dust, opacity 0.55
Eyebrow: DM Mono 10px, rose, ::before com linha 18px
Título: Playfair 700, com <em> em rose
```

### Insight Card
```
border-left: 3px solid var(--rose)
background: var(--rose-pale)
grid: 40px 1fr
Ícone: Playfair 28px bold rose
Tag: DM Mono 9px uppercase rose
```

### Chart Wrap
```
background: var(--white); border: 1px solid var(--dust)
padding: 36px 36px 28px
Tag absoluta: top/right 18px, DM Mono 9px
Título: Playfair 17px 700
Subtítulo: DM Mono 10px uppercase dust-dark
Source: DM Mono 9.5px, border-top dust, margin-top 20px
```

### Method Panel (Bases de Dados + Fórmulas)
```
background: var(--jet); color: var(--ivory)
padding: 40px
h4: DM Mono 10px, sage, ::before linha 14px sage
Source items: grid 20px 1fr, gap 14px, border-bottom rgba(white, 0.07)
Formula block: background rgba(rose, 0.08), border-left 2px rose
code: DM Mono 11px, rose-light, line-height 1.9
```

### Progress Bars
```
Track: height 4px, background --dust
Fill: height 100%, background --rose (ou .sage = --sage-dark)
Transition: width 1.6s cubic-bezier(0.4, 0, 0.2, 1)
Animação via IntersectionObserver
```

### Botões
```css
/* Primário */
background: var(--rose); color: white;
font-family: DM Mono; font-size: 10px; letter-spacing: 2px; uppercase;
padding: 14px 28px; border: 1.5px solid var(--rose);
hover: background transparent; color: var(--rose);

/* Secundário */
background: transparent; color: var(--jet);
border: 1.5px solid var(--dust);
hover: border-color: var(--jet);
```

---

## 5. Seções de Conteúdo

### Alternância de Backgrounds (Ritmo Visual)

```
Hero         → --ivory
01 Sobre     → --white (.alt)
02 Skills    → --ivory
03 Exp.      → --white (.alt)
04 Projetos  → --jet (.dark)
05 Filosofia → --white (.alt)
06 Contato   → --jet (.dark)
Footer       → --jet + border-top 3px --rose
```

**Regra:** nunca duas seções `.dark` consecutivas sem uma `.alt` no meio.

---

## 6. Gráficos — Chart.js

### Configurações Globais

```javascript
Chart.defaults.color = '#B8C0B4';           // --dust-dark
Chart.defaults.font.family = "'DM Mono', monospace";
Chart.defaults.font.size = 10;
```

### Tooltip Padrão

```javascript
const tip = {
  backgroundColor: '#2C363F',     // --jet
  borderColor: '#E75A7C',         // --rose
  borderWidth: 1,
  titleColor: '#E75A7C',
  bodyColor: '#F2F5EA',
  padding: 14,
  cornerRadius: 2,
  titleFont: { family: "'DM Mono',monospace", size: 10 },
  bodyFont: { family: "'DM Sans',sans-serif", size: 12 },
};
```

### Scales Padrão

```javascript
const xScale = {
  grid: { color: 'rgba(214,219,210,0.5)', lineWidth: 0.8 },
  ticks: { color: '#B8C0B4' },
  border: { color: '#D6DBD2' }
};
// yScale idêntico mas com grid color: '#D6DBD2'
```

### Paleta para Datasets

| Uso | Cor |
|---|---|
| Dados primários / projetados | `#E75A7C` (rose) |
| Dados históricos | `rgba(187,199,164,0.55)` (sage transparente) |
| Linha principal | `#2C363F` (jet) |
| Dados secundários | `#8FA07A` (sage-dark) |
| Background fill | `rgba(231,90,124,0.07)` |

### Tipos de Gráfico por Contexto

| Contexto | Tipo | Razão |
|---|---|---|
| Evolução temporal + share | Bar + Line (dual axis) | Volume absoluto + % juntos |
| Custo comparativo | Line com fill | Área entre curvas comunica gap |
| Crescimento YoY | Bar com cor condicional | Rose para anos acima do threshold |
| Forecast | Bar agrupado + Line | Historico vs. projetado imediatamente claro |
| Expertise | Radar | Múltiplas dimensões sem ranking |
| Evolução de skills | Multi-line | Progressão temporal comparativa |

---

## 7. Animações

### Scroll-triggered (Progress Bars)

```javascript
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.querySelectorAll('.bar-fill').forEach((f, i) => {
        setTimeout(() => { f.style.width = f.dataset.w + '%'; }, i * 80);
      });
      obs.unobserve(e.target);
    }
  });
}, { threshold: 0.2 });
```

### Chart Animations

```javascript
animation: { duration: 1400–1800, easing: 'easeInOutQuart' }
```

### Active Nav Tracking

```javascript
window.addEventListener('scroll', () => {
  // Detecta seção atual e aplica .active no link do topbar
});
```

---

## 8. Adaptações para Seção Dark

Dentro de `.section.dark`:

```css
.chart-wrap      → background: rgba(255,255,255,0.03); border-color: rgba(255,255,255,0.09)
.chart-title     → color: var(--ivory)
.chart-subtitle  → color: var(--dust-dark)
.chart-source    → color: rgba(255,255,255,0.28); border-top: rgba(255,255,255,0.08)
grid em gráficos → color: rgba(255,255,255,0.06)
```

---

## 9. Handoff para Agência / Dev

### Para recriar em Webflow:

1. Importar paleta como variáveis globais (tokens acima)
2. Configurar fontes Google: Playfair Display + DM Sans + DM Mono
3. Criar Symbol/Component para: Topbar, Section Header, Chart Wrap, Insight Card, Method Panel
4. Chart.js **não é nativo no Webflow** — usar Embed Code com script externo do CDN
5. Gap de 2px entre cards: usar CSS Grid com `gap: 2px` via Custom CSS

### Para recriar em Figma:

1. Criar Color Styles com todos os tokens nomeados
2. Criar Text Styles para cada nível tipográfico
3. Criar Auto Layout com gap 2px para os grids de cards
4. Gráficos: usar componentes estáticos (screenshots do Chart.js) ou plugin Figma Charts
5. Exportar como design system compartilhado para handoff

### Para recriar em React/Next.js:

```
- CSS Variables → :root no globals.css
- Fontes → next/font com Google Fonts
- Gráficos → react-chartjs-2 (wrapper do Chart.js)
- Layout → CSS Grid nativo (não Tailwind para este design)
- Animações de scroll → Intersection Observer API ou Framer Motion
```

---

## 10. Convenções de Código

```css
/* Comentários de seção em bloco */
/* ══════════════ NOME DA SEÇÃO ══════════════ */

/* Todos os seletores com prefixo de contexto */
.chart-title, .chart-subtitle, .chart-source, .chart-tag

/* BEM-like mas simplificado: bloco-elemento */
.project-card, .project-card-header, .project-title, .project-badge

/* Modificadores com classe adicional, não aninhamento profundo */
.skill-card.accent   (background jet)
.skill-card.rose-accent (background rose)
.section.alt (background white)
.section.dark (background jet)
```

---

## 11. Checklist de QA para Novos Projetos

Antes de adicionar um novo projeto no portfólio, verificar:

- [ ] Badge de status (Publicado / Em desenvolvimento / Breve)
- [ ] Número decorativo no canto (`.project-num-tag`)
- [ ] KPI row com 4 métricas principais
- [ ] Mínimo 2 gráficos Chart.js com dados reais
- [ ] Painel de Bases de Dados (`.method-panel`) com todas as fontes numeradas
- [ ] Painel de Fórmulas com código explícito em `<code>`
- [ ] Tag row com tecnologias utilizadas
- [ ] Source em todos os charts (`.chart-source`)
- [ ] Dados validados em 3+ fontes cruzadas

---

## 12. Próximas Evoluções Recomendadas

| Prioridade | Feature | Esforço |
|---|---|---|
| 🔴 Alta | Responsividade mobile (media queries) | Médio |
| 🔴 Alta | Adicionar Projeto 02 (Capex Dashboard) | Alto |
| 🟡 Média | Dark mode toggle | Médio |
| 🟡 Média | Filtro de projetos por tag | Médio |
| 🟢 Baixa | Animações de entrada (scroll reveal) | Baixo |
| 🟢 Baixa | Print/PDF stylesheet | Baixo |
| 🟢 Baixa | Domínio customizado (jonasleo.com.br) | Baixo |

---

*Design System v1.0 · Jonas Leonardo Portfolio · Fevereiro 2025*
*Criado por: Claude (Anthropic) + Jonas Leonardo*
