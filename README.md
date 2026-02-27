[README.md](https://github.com/user-attachments/files/25602729/README.md)
# Jonas Leonardo · Data Analyst & BI Portfolio

[![Portfolio](https://img.shields.io/badge/Portfolio-Live-E75A7C?style=flat-square&logoColor=white)](https://jleonardopl.github.io/portfolio)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jonas_Leonardo-2C363F?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/jonas-leonardo/)
[![Email](https://img.shields.io/badge/Email-jleonardopl@gmail.com-BBC7A4?style=flat-square&logo=gmail)](mailto:jleonardopl@gmail.com)

---

## Sobre este repositório

Portfólio profissional de análise de dados, Business Intelligence e Data Science —
construído com HTML, CSS e Chart.js puro. Sem frameworks. Sem dependências ocultas.
Apenas dados reais, fontes verificáveis e visualizações que informam decisões.

> **"Não existe análise boa com dado ruim. E não existe dado bom mal apresentado."**

---

## Stack Técnico

| Ferramenta | Nível | Aplicação |
|---|---|---|
| Microsoft Excel / DAX | ⬛⬛⬛⬛⬛ Avançado | Modelagem, Power Query, Power Pivot |
| Power BI | ⬛⬛⬛⬛⬜ Avançado | Dashboards executivos, DAX complexo |
| Python (pandas, matplotlib) | ⬛⬛⬛⬜⬜ Intermediário+ | Análise exploratória, automação, forecast |
| SQL | ⬛⬛⬛⬜⬜ Intermediário | Consultas, JOINs, integração ERP |
| Chart.js / DataViz | ⬛⬛⬛⬛⬜ Avançado | Visualizações interativas para web |

---

## Projetos no Portfólio

### 01 · Revolução Verde 2.0 — Biológicos vs. Químicos no Brasil
**Status:** ✅ Publicado · Fevereiro 2025

Estudo de ciência de dados sobre a transição estrutural do mercado de defensivos agrícolas
no Brasil. 12 anos de dados reais (2012–2023) + forecast até 2028.

**Principais achados:**
- Mercado de biológicos cresceu **+1.047%** entre 2012 e 2023
- Market share: **1,2% → 11,3%** em 11 anos
- CAGR de **24,8% a.a.** — 6× superior ao mercado total
- Projeção: **US$ 5 bilhões** e **25% de market share** até 2028

**Fontes:** ABCBIO · MAPA/SDA · SINDIVEG · CropLife Brasil · CEPEA/ESALQ · Mordor Intelligence

**Fórmulas principais:**
```
Market Share(t) = Volume_Bio(t) / Volume_Total(t) × 100
CAGR = (1.720 / 150)^(1/11) - 1 = 24,8%
Forecast(t) = 1.720 × (1 + 0,248)^(t - 2023)
YoY(t) = (V(t) - V(t-1)) / V(t-1) × 100
```

---

### 02 · Dashboard Capex — Armazéns de Grãos *(em desenvolvimento)*
Análise de custos de capital e variáveis operacionais baseada em 6 anos de dados reais
da operação Louis Dreyfus Company. Em fase de documentação e anonimização.

---

### 03 · Análise de Rebates Comerciais — Agro *(em breve)*
Modelagem de campanhas de rebates e premiação de distribuidores com Power BI e DAX avançado.

---

## Experiência Profissional

```
2022 – 2025  │  Agro Amazônia          │  Analista de Rebates e Prêmios
2016 – 2022  │  Louis Dreyfus Company  │  Analista Operacional & Capex
```

---

## Estrutura do Repositório

```
portfolio/
├── index.html          ← Portfólio completo (single-file, sem dependências locais)
├── README.md           ← Este arquivo
├── DESIGN_SYSTEM.md    ← Especificação técnica completa de design e código
└── DEPLOY_GUIDE.md     ← Passo a passo para publicar no GitHub Pages
```

---

## Como rodar localmente

Não precisa instalar nada. Apenas abra o arquivo:

```bash
# Opção 1 — abrir direto no navegador
double click em index.html

# Opção 2 — servidor local (opcional)
python -m http.server 8000
# acesse: http://localhost:8000
```

---

## Contato

**Jonas Leonardo de Paula Leite da Silva**
Data Analyst · Business Intelligence · Python
📍 Cuiabá, MT · Brasil

- 📧 [jleonardopl@gmail.com](mailto:jleonardopl@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/jonas-leonardo/)

---

*Portfólio construído com HTML · CSS · Chart.js 4.4.1 · Google Fonts (Playfair Display + DM Sans + DM Mono)*
*Hospedado via GitHub Pages · Sem custo · Sem backend · 100% estático*
