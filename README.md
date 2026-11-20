<h1 align="center">📊 Jonas Leonardo · Data Analytics & BI Portfolio</h1>

<p align="center">
  <b>Agribusiness data, real sources, decision-ready visuals.</b><br>
  A single-file, zero-dependency portfolio built with HTML, CSS and Chart.js. Bilingual (EN / PT-BR), light & dark mode.
</p>

<p align="center">
  <a href="https://jleonardopl1.github.io/jleonardopl.github.io/"><img src="https://img.shields.io/badge/▶_Live_Portfolio-Open-2E7D32?style=for-the-badge" alt="Live portfolio"></a>
  <a href="https://www.linkedin.com/in/jonas-leonardo/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:jleonardopl@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/Chart.js_4.4-FF6384?style=flat-square&logo=chartdotjs&logoColor=white" alt="Chart.js">
  <img src="https://img.shields.io/badge/GitHub_Pages-222222?style=flat-square&logo=githubpages&logoColor=white" alt="GitHub Pages">
  <img src="https://img.shields.io/badge/dependencies-0-success?style=flat-square" alt="zero dependencies">
</p>

---

## 👤 About me

Data & Business Analyst with **9+ years in Brazilian agribusiness**. I run the analytics behind **70+ rebate and sales-incentive campaigns a year** at Agro Amazônia, and before that I spent **7 years at Louis Dreyfus Company** building operational and Capex analytics for grain warehouses.

**Microsoft Certified: Power BI Data Analyst Associate** · Data Science student at Mackenzie · Founder of Yamazing (AI-powered SaaS).

> *"Bad data ruins any analysis. Good data, badly presented, ruins it too."*

---

## 🔬 Case studies

### 01 · Green Revolution 2.0: biologicals vs. chemicals in Brazil
`✅ Published` · `Data Science` · `Forecasting`

**Question:** How fast are biological crop inputs taking share from chemical pesticides in Brazil, and where will the market be by 2028?

**Approach:** I consolidated 12 years of market data (2012–2023) from 6 public and industry sources, computed YoY growth, market share and CAGR, and projected a compound-growth scenario to 2028.

| Metric | Result |
|---|---|
| Biologicals market growth, 2012 → 2023 | **+1,047%** |
| Market share | **1.2% → 11.3%** |
| CAGR | **24.8% p.a.**, about 6× the total market |
| 2028 projection | **≈ US$ 5B** and **~25% share** |

<details>
<summary><b>Formulas and sources</b></summary>

```text
Market Share(t) = Bio_Volume(t) / Total_Volume(t) × 100
CAGR            = (1,720 / 150)^(1/11) − 1 = 24.8%
Forecast(t)     = 1,720 × (1 + 0.248)^(t − 2023)
YoY(t)          = (V(t) − V(t−1)) / V(t−1) × 100
```

**Sources:** ABCBIO · MAPA/SDA · SINDIVEG · CropLife Brasil · CEPEA/ESALQ · Mordor Intelligence

</details>

### 02 · Grain warehouse Capex & operations dashboard
`🛠 In progress` · `Power BI` · `Capex/Opex`

Capital-cost and operational-driver analysis built on 6 years of real warehouse operations data, now being anonymized for public release.

### 03 · Commercial rebate analytics for agribusiness distribution
`🛠 In progress` · `Power BI` · `DAX`

How distributors model supplier rebate and incentive campaigns: earned vs. pending value, forecasting of achievement, and the impact on margins.

---

## 🧰 Skills, backed by evidence

| Area | Tools | Where I've applied it |
|---|---|---|
| **BI & reporting** | Power BI, DAX, Power Query (M), Power Pivot | Executive reporting for 70+ campaigns/yr; PL-300 certified |
| **Spreadsheet modeling** | Excel (advanced), VBA, XlsxWriter | Rebate calculation engines, Capex scenario models |
| **Programming** | Python (pandas, NumPy, Matplotlib), SQL (CTEs, window functions) | Exploratory analysis, forecasting, ERP data extraction |
| **Data viz for web** | Chart.js, HTML/CSS | This portfolio |
| **Domain** | Rebates & channel incentives, commodities, grain logistics | 9+ years in agribusiness |

---

## 💼 Experience

| Period | Company | Role |
|---|---|---|
| Aug 2024 → now | **Agro Amazônia** | Rebate & Incentive Analyst |
| 7 years, to 2024 | **Louis Dreyfus Company** | Storage & Operations Analyst (Capex) |

---

## 🗂 Repository structure

```text
.
├── index.html          # Entire portfolio: single file, no local dependencies
├── DESIGN_SYSTEM.md    # Design tokens, typography, components and chart specs
├── DEPLOY_GUIDE.md     # Step-by-step GitHub Pages deployment
└── README.md
```

## ▶️ Run locally

Nothing to install.

```bash
# Option 1: open index.html in your browser
# Option 2: serve it locally
python -m http.server 8000   # → http://localhost:8000
```

---

<details>
<summary>🇧🇷 Versão em português</summary>

Portfólio de análise de dados e BI focado em agronegócio: dados reais, fontes verificáveis e visualizações que informam decisões. Arquivo único em HTML, CSS e Chart.js, sem dependências, bilíngue e com modo claro/escuro.

Sou Analista de Dados e Negócios com 9+ anos no agronegócio. Hoje cuido da análise de 70+ campanhas de rebate e premiação por ano na Agro Amazônia; antes, passei 7 anos na Louis Dreyfus Company com analytics operacional e de Capex em armazéns de grãos. Certificado Microsoft Power BI Data Analyst Associate e estudante de Ciência de Dados no Mackenzie.

</details>

<p align="center"><sub>Built with HTML · CSS · Chart.js 4.4.1 · Playfair Display + DM Sans + DM Mono · Hosted free on GitHub Pages</sub></p>
