# Cafo — Design System
> Inferido a partir da landing page `cafo-lp.vercel.app` · v1.0

---

## 1. Fundação

### Identidade Visual

O design do Cafo é **dark-first, editorial e técnico**. Combina a densidade de um painel SaaS com a atmosfera acolhedora de uma cafeteria especializada. A linguagem visual é limpa, com contrastes fortes, tipografia expressiva e UI components que simulam interfaces reais do produto.

**Referências estéticas:**
- Painéis SaaS modernos (Linear, Vercel, Raycast)
- Editorial de café especialidade
- Interface de PDV touchscreen

---

## 2. Paleta de Cores

### Cores Base (Tema Escuro)

| Token | Valor (inferido) | Uso |
|---|---|---|
| `--bg-primary` | `#0A0A0A` | Fundo principal da página |
| `--bg-surface` | `#111111` | Cards, seções elevadas |
| `--bg-elevated` | `#1A1A1A` | Inputs, UI components internos |
| `--bg-border` | `#2A2A2A` | Bordas sutis, divisores |
| `--text-primary` | `#FAFAFA` | Títulos, texto principal |
| `--text-secondary` | `#A0A0A0` | Subtítulos, metadados, labels |
| `--text-muted` | `#606060` | Placeholders, textos terciários |

### Cor de Marca (Accent)

| Token | Valor (inferido) | Uso |
|---|---|---|
| `--accent` | `#C8963E` | CTAs primários, highlights, destaques em títulos |
| `--accent-hover` | `#D9A84F` | Estado hover do accent |
| `--accent-subtle` | `#C8963E1A` | Backgrounds de badges, tags sutis |
| `--accent-text` | `#C8963E` | Texto em itálico destacado nos headings |

> **Nota:** O accent é um âmbar/dourado — evoca café, calor, especialidade. Usado com parcimônia para máximo impacto.

### Cores Semânticas

| Token | Valor (inferido) | Uso |
|---|---|---|
| `--success` | `#4ADE80` | Métricas positivas (`+8% vs ontem`, `↑ 3 novos`) |
| `--warning` | `#FACC15` | Alertas, avisos no CRM |
| `--danger` | `#F87171` | Inativos, atenção |
| `--info` | `#60A5FA` | Tags informativas |

### Gradientes

```css
/* Hero background — noise + dark radial */
background: radial-gradient(ellipse at 50% 0%, #1A1208 0%, #0A0A0A 60%);

/* Accent glow — usado atrás de UI mockups */
background: radial-gradient(ellipse at center, #C8963E18 0%, transparent 70%);

/* Surface cards */
background: linear-gradient(135deg, #161616 0%, #111111 100%);
```

---

## 3. Tipografia

### Famílias

| Papel | Família | Estilo |
|---|---|---|
| **Display / Hero** | Serifada (inferido: `Playfair Display` ou `DM Serif Display`) | Títulos grandes com itálico expressivo |
| **Body / UI** | Sans-serif (inferido: `Inter` ou `DM Sans`) | Textos corridos, labels, botões |
| **Mono / Dados** | Monospace (inferido: `JetBrains Mono` ou `IBM Plex Mono`) | Valores numéricos no dashboard, métricas |

> **Padrão distintivo:** Os títulos `<h1>` e `<h2>` misturam regular + *itálico* na mesma linha para criar ritmo visual — ex: *"do barista ao dono"*, *"CRM"*, *"café"*.

### Escala Tipográfica

| Token | Tamanho | Line-height | Uso |
|---|---|---|---|
| `--text-xs` | `11px` | `1.4` | Labels, badges, metadados |
| `--text-sm` | `13px` | `1.5` | Texto secundário, listas |
| `--text-base` | `15–16px` | `1.6` | Corpo de texto |
| `--text-lg` | `18–20px` | `1.5` | Subtítulos, intro paragraphs |
| `--text-xl` | `24–28px` | `1.3` | H3, títulos de seção menores |
| `--text-2xl` | `36–42px` | `1.2` | H2 principais |
| `--text-hero` | `56–72px` | `1.05` | H1 hero |

### Padrões de Uso

```css
/* Padrão hero — mixing serif + italic */
h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(42px, 6vw, 72px);
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.02em;
}

h1 em {
  font-style: italic;
  color: var(--accent); /* dourado */
}

/* H2 sections */
h2 {
  font-size: clamp(28px, 4vw, 42px);
  font-weight: 700;
  line-height: 1.15;
  letter-spacing: -0.015em;
}

/* Label de seção — ex: "Plataforma para cafeterias" */
.section-label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent);
}
```

---

## 4. Espaçamento

Baseado em escala de 4px.

| Token | Valor | Uso típico |
|---|---|---|
| `--space-1` | `4px` | Micro gaps, icon padding |
| `--space-2` | `8px` | Gaps internos de componentes |
| `--space-3` | `12px` | Padding de badges, tags |
| `--space-4` | `16px` | Padding interno de cards pequenos |
| `--space-6` | `24px` | Gap entre elementos em grid |
| `--space-8` | `32px` | Padding de cards grandes |
| `--space-12` | `48px` | Espaço entre subseções |
| `--space-16` | `64px` | Padding de seções (mobile) |
| `--space-24` | `96px` | Padding de seções (desktop) |
| `--space-32` | `128px` | Gap entre seções maiores |

---

## 5. Bordas & Raios

| Token | Valor | Uso |
|---|---|---|
| `--radius-sm` | `6px` | Badges, tags, inputs pequenos |
| `--radius-md` | `10px` | Botões, cards compactos |
| `--radius-lg` | `16px` | Cards principais |
| `--radius-xl` | `20–24px` | Cards de UI mockup, pricing |
| `--radius-full` | `9999px` | Avatares, pills |

### Bordas

```css
/* Borda padrão de cards */
border: 1px solid #2A2A2A;

/* Borda com glow sutil (cards em destaque) */
border: 1px solid #C8963E30;
box-shadow: 0 0 0 1px #C8963E15;

/* Sem borda (superfícies internas) */
border: none;
```

---

## 6. Sombras & Elevação

```css
/* Elevação baixa — cards padrão */
box-shadow: 0 1px 3px rgba(0,0,0,0.4), 0 1px 2px rgba(0,0,0,0.3);

/* Elevação média — UI mockups, pricing highlight */
box-shadow: 0 8px 32px rgba(0,0,0,0.6), 0 2px 8px rgba(0,0,0,0.4);

/* Elevação alta — modais, popovers */
box-shadow: 0 24px 64px rgba(0,0,0,0.8);

/* Glow accent — CTA primário */
box-shadow: 0 0 24px rgba(200,150,62,0.3);
```

---

## 7. Componentes

### Botões

#### Primário (CTA principal)
```css
.btn-primary {
  background: #C8963E;
  color: #0A0A0A;
  font-weight: 700;
  font-size: 14px;
  padding: 12px 24px;
  border-radius: 10px;
  border: none;
  letter-spacing: -0.01em;
  transition: all 0.15s ease;
}
.btn-primary:hover {
  background: #D9A84F;
  box-shadow: 0 0 20px rgba(200,150,62,0.4);
  transform: translateY(-1px);
}
```

#### Secundário (outline)
```css
.btn-secondary {
  background: transparent;
  color: #FAFAFA;
  font-weight: 500;
  font-size: 14px;
  padding: 12px 24px;
  border-radius: 10px;
  border: 1px solid #2A2A2A;
  transition: all 0.15s ease;
}
.btn-secondary:hover {
  border-color: #404040;
  background: #1A1A1A;
}
```

#### Ghost / Link
```css
.btn-ghost {
  background: transparent;
  color: #A0A0A0;
  font-size: 14px;
  padding: 8px 16px;
  border: none;
  border-radius: 8px;
}
.btn-ghost:hover {
  color: #FAFAFA;
  background: #1A1A1A;
}
```

---

### Cards

#### Card Padrão
```css
.card {
  background: #111111;
  border: 1px solid #2A2A2A;
  border-radius: 16px;
  padding: 24px;
}
```

#### Card de Produto / UI Mockup
```css
.card-product {
  background: #0F0F0F;
  border: 1px solid #222222;
  border-radius: 20px;
  padding: 0; /* overflow hidden para clips */
  overflow: hidden;
  box-shadow: 0 8px 32px rgba(0,0,0,0.6);
}
```

#### Card de Pricing Destacado
```css
.card-pricing-featured {
  background: linear-gradient(135deg, #1A1208, #111111);
  border: 1px solid #C8963E40;
  border-radius: 20px;
  padding: 32px;
  position: relative;
}
/* Badge "Recomendado" */
.card-pricing-featured::before {
  content: 'Recomendado';
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
  background: #C8963E;
  color: #0A0A0A;
  font-size: 11px;
  font-weight: 700;
  padding: 4px 12px;
  border-radius: 9999px;
  letter-spacing: 0.05em;
}
```

---

### Badge / Label de Seção

```css
.section-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  background: #C8963E15;
  border: 1px solid #C8963E30;
  color: #C8963E;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 5px 12px;
  border-radius: 9999px;
}
```

---

### Avatares de Testimonial

```css
.avatar {
  width: 36px;
  height: 36px;
  border-radius: 9999px;
  background: #C8963E20;
  color: #C8963E;
  font-size: 12px;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  letter-spacing: 0.05em;
}
```

---

### Stars (Rating)

```css
.stars {
  color: #C8963E;
  font-size: 12px;
  letter-spacing: 1px;
}
```

---

### Métricas / Dashboard UI

```css
/* Valor positivo */
.metric-positive {
  color: #4ADE80;
  font-size: 11px;
  font-weight: 600;
}

/* Valor negativo / atenção */
.metric-negative {
  color: #F87171;
  font-size: 11px;
  font-weight: 600;
}

/* Label de métrica */
.metric-label {
  color: #606060;
  font-size: 10px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

/* Valor principal */
.metric-value {
  font-family: 'JetBrains Mono', monospace;
  font-size: 24px;
  font-weight: 700;
  color: #FAFAFA;
  letter-spacing: -0.02em;
}
```

---

### Numeração de Steps

```css
.step-number {
  font-size: 11px;
  font-weight: 700;
  color: #C8963E;
  letter-spacing: 0.05em;
  font-family: monospace;
  /* ex: "01", "02", "03" */
}
```

---

## 8. Layout & Grid

### Container

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
}

@media (min-width: 768px) {
  .container { padding: 0 48px; }
}

@media (min-width: 1280px) {
  .container { padding: 0 80px; }
}
```

### Grid Principal

```css
/* 2 colunas — features, pricing */
.grid-2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}

/* 3 colunas — testimonials */
.grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

/* Split — texto + UI mockup */
.grid-split {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: center;
}
```

---

## 9. Estrutura de Seções

| Seção | Tipo | Background | Padding vertical |
|---|---|---|---|
| Navbar | Sticky + blur | `rgba(10,10,10,0.8)` + backdrop-filter | `16px` |
| Hero | Full-width | Radial gradient escuro | `96–128px` |
| Features (steps) | Alternado | `#0A0A0A` | `96px` |
| Social proof / comunidade | Dark elevated | `#0F0F0F` | `96px` |
| Testimonials | Grid 3 cols | `#0A0A0A` | `80px` |
| Problema / dor | Texto centrado | `#0A0A0A` | `96px` |
| UI Showcase (PDV + IA) | Split layout | `#080808` | `80px` |
| Pricing | Grid 2 cols | `#0A0A0A` | `96px` |
| CTA final | Centrado | `#0F0B06` (leve quente) | `96px` |
| Footer | Dark | `#080808` | `32px` |

---

## 10. Navbar

```
[Logo "Cafo"] ←————————————————→ [Começar grátis]
```

- Logo: wordmark em branco, sem ícone
- Sem links de navegação visíveis (landing page one-scroll)
- CTA único no canto direito — botão primário amber
- Sticky com `backdrop-filter: blur(12px)` e leve borda bottom

---

## 11. Micro-interações & Motion

| Elemento | Comportamento |
|---|---|
| Botões primários | `translateY(-1px)` + glow no hover |
| Cards | `border-color` suaviza no hover |
| UI Mockups | Estáticos, sem animação (imagens reais do produto) |
| Seção Hero | Provável fade-in + stagger nos elementos |
| Métricas no dashboard | Podem ter counter animation no scroll |

```css
/* Transição padrão */
transition: all 0.15s ease;

/* Transição suave para hover em cards */
transition: border-color 0.2s ease, box-shadow 0.2s ease;
```

---

## 12. Copywriting Patterns

| Padrão | Exemplo |
|---|---|
| **Headline dupla** — setup + payoff | "Você acorda cedo, trabalha até fechar. *A segunda-feira fraca só aparece na conta do mês.*" |
| **Itálico como ênfase emocional** | *barista*, *dono*, *CRM*, *café* |
| **Bullets de benefício** | "Sem cartão de crédito · Setup em 10 minutos" |
| **Duplo CTA** | Primário (ação) + Secundário (descoberta) |
| **Prova social em 1 linha** | Nome, cargo, cidade, ★★★★★, quote |
| **Labels de seção em caps** | "DO PEDIDO AO RELACIONAMENTO" |
| **Headline simplificada de pricing** | "Simples como o café *que você faz.*" |

---

## 13. Assets

| Asset | URL |
|---|---|
| Screenshot PDV + Perfil de cliente | `https://cafo-lp.vercel.app/cafo-product-1.png` |
| Screenshot CRM | `https://cafo-lp.vercel.app/cafo-product-2.png` |

---

## 14. Checklist de Consistência

Ao criar novas páginas dentro do ecossistema Cafo (ex: Cafo Frame), verificar:

- [ ] Fundo dark `#0A0A0A` como base
- [ ] Accent âmbar `#C8963E` — apenas em CTAs, itálicos de heading e labels
- [ ] Tipografia serifada nos headings com itálico expressivo
- [ ] Labels de seção em uppercase, tracking largo, cor accent
- [ ] Cards com `border: 1px solid #2A2A2A`
- [ ] Métricas em monospace com verde/vermelho semântico
- [ ] Dois CTAs por seção principal (primário + secundário)
- [ ] Sem background branco em nenhuma seção
- [ ] Numeração de steps em formato `01`, `02`, `03`
- [ ] Testimonials com avatar de iniciais (não foto)

---

*Design System inferido a partir de `cafo-lp.vercel.app` · Cafo Studio © 2026*