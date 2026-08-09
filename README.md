<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,0,20&height=180&section=header&text=Data%20Profiler&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Data%20Preprocessing%20%26%20Feature%20Engineering&descAlignY=58&descSize=18" width="100%"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=C0111F&center=true&vCenter=true&width=650&lines=Customer+Churn+Data+Profiler+%F0%9F%94%8D;CSV+%2B+JSON+%2B+SQL+%2B+API+%E2%86%92+ML-Ready+Data;Cleaning+%C2%B7+EDA+%C2%B7+Automated+Profiling" alt="Typing SVG" />
</a>

<br/>

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Tensors-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![ydata-profiling](https://img.shields.io/badge/ydata--profiling-Automated%20EDA-6A1B9A?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-2ECC71?style=for-the-badge)
![License](https://img.shields.io/badge/License-Academic%20Project-lightgrey?style=for-the-badge)

</div>

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 📌 Overview

**Data Profiler** is a Data Preprocessing & Feature Engineering project completed as **PR.1** for **Red & White Skill Education**. Working as a Junior Data Analyst for a consumer-insights company, the goal is to take a fragmented, real-world-style **customer purchase behavior** dataset — arriving from **CSV, JSON, a SQL database, and a REST API** — and turn it into a clean, profiled, **ML-ready** dataset for a **customer churn prediction** problem.

> 🎯 **ML Problem Framed:** Predict whether a customer will **churn**, using demographic, purchase, membership, and engagement signals.

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 🗂️ Repository Structure

```text
Data-Profiler-Project/
├── data/
│   ├── customers_demographics.csv         # Source 1 — CSV (demographics)
│   ├── purchase_behavior.json             # Source 2 — JSON (purchase behavior)
│   ├── customers.db                       # Source 3 — SQLite (membership & support)
│   └── engagement_api_response.json       # Source 4 — API-style payload (engagement + churn label)
├── Images/
│   ├── Univariate_Analysis.png            # Age / Income / Total Spend distributions
│   ├── Bivariate_Analysis.png             # Gender vs. Purchases, Income vs. Churn
│   ├── Multivariate_Analysis.png          # Correlation heatmap
│   └── Pair_Plot.png                      # Pair plot by churn class
├── notebooks/
│   └── Data_Profiler_Analysis.ipynb       # Full analysis notebook (Parts A–E, executed)
├── docs/
│   └── Theory_Concepts.pdf                # Theory write-up: data analysis, DS lifecycle, ML framing, tensors
├── reports/
│   └── pandas_profiling_report.html       # Automated data-profiling report (ydata-profiling)
├── requirements.txt
└── README.md
```

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 🧩 Data Sources

| # | Source Type | File | Contents |
|---|---|---|---|
| 1 | CSV | `data/customers_demographics.csv` | `customer_id`, `age`, `gender`, `income`, `region`, `signup_days_ago` |
| 2 | JSON | `data/purchase_behavior.json` | `purchase_frequency`, `total_spent`, `avg_order_value`, `last_purchase_days_ago` |
| 3 | SQL (SQLite) | `data/customers.db` → `customer_membership` table | `membership_years`, `membership_tier`, `support_tickets`, `satisfaction_score` |
| 4 | REST API (payload) | `data/engagement_api_response.json` | `app_sessions_per_month`, `email_open_rate`, `churn` (target) |

All four sources are merged on `customer_id` inside the notebook into a single working table.

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 🛠️ Workflow

### Part A — Fundamentals
- What is Data Analysis
- Planning a Data Science project (CRISP-DM based lifecycle)
- ML problem statement: churn prediction
- Tensors explained in depth, with NumPy examples (scalar → vector → matrix → 3D tensor)

### Part B — Data Acquisition
- Load CSV with Pandas
- Parse JSON
- Connect to SQLite and fetch records
- Parse an API-style JSON response (`{"status", "count", "results": [...]}`)

### Part C — Data Understanding & Cleaning
- `.head()`, `.info()`, `.describe()` exploration
- Missing value & duplicate detection
- Median imputation, dtype correction, duplicate removal

### Part D — Exploratory Data Analysis
- **Univariate:** Age / Income / Total Spend distributions
- **Bivariate:** Gender vs. Purchases, Income vs. Churn
- **Multivariate:** Correlation heatmap, pair plots by churn class

### Part E — Data Profiling
- Automated `ydata-profiling` report — missing values, descriptive stats, correlations, data-quality warnings

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 📊 Exploratory Data Analysis — Visuals

<div align="center">

**Univariate Analysis**
<img src="Images/Univariate_Analysis.png" width="90%"/>

**Bivariate Analysis**
<img src="Images/Bivariate_Analysis.png" width="90%"/>

**Multivariate Analysis — Correlation Heatmap**
<img src="Images/Multivariate_Analysis.png" width="90%"/>

**Pair Plot by Churn Class**
<img src="Images/Pair_Plot.png" width="90%"/>

</div>

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 📈 Key Insights

- `last_purchase_days_ago` and `satisfaction_score` show the clearest separation between churned and retained customers — the strongest behavioral churn signals.
- Total spend is right-skewed; a log transform is recommended before distance-based modeling.
- Income alone is a weak churn predictor — overlap between churned/retained groups is large.
- No severe multicollinearity among numeric features, per the correlation heatmap.

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## ⚙️ Getting Started

```bash
git clone https://github.com/RENSEE-GAJIPARA/data-profiler.git
cd data-profiler
pip install -r requirements.txt
jupyter notebook notebooks/Data_Profiler_Analysis.ipynb
```

<img src="https://capsule-render.vercel.app/api?type=wave&color=gradient&customColorList=2,0,20&height=3&section=header" width="100%"/>

## 📄 Documentation

- 📘 **Theory write-up (PDF):** [`docs/Theory_Concepts.pdf`](docs/Theory_Concepts.pdf)
- 📈 **Automated profiling report (HTML):** [`reports/pandas_profiling_report.html`](reports/pandas_profiling_report.html)

---

<div align="center">

### ✍️ Author

**Rensee Gajipara**
B.Tech — Artificial Intelligence & Data Science, Sarvajanik College of Engineering & Technology (SCET), Surat

[![GitHub](https://img.shields.io/badge/GitHub-RENSEE--GAJIPARA-181717?style=for-the-badge&logo=github)](https://github.com/RENSEE-GAJIPARA)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rensee%20Gajipara-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rensee-gajipara/)

<br/>

*"Quality is our Motto."* — Red & White Skill Education, Shaping "skills" for "scaling" higher...!!!

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,0,20&height=100&section=footer" width="100%"/>

</div>
