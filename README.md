# Data Portfolio

A collection of data analysis and machine learning projects. Each project includes a focused problem statement, exploratory analysis, and actionable findings.

---

## EDA Projects

| Project | Dataset | Key Topics | Tools |
|---|---|---|---|
| [Telco Customer Churn](./eda/telco-churn/) | 7K telecom customers (California) | Churn drivers, high-risk segmentation, A/B test design | pandas, seaborn, matplotlib |
| [Forbes Highest-Paid Athletes](./eda/forbes-athletes/) | Top 10 athletes per year, 1990–2020 | Earnings trends, sport dominance, concentration analysis | pandas, scipy, matplotlib |
| [Olist E-Commerce (Brazil)](./eda/olist-ecommerce/) | ~100K orders, multiple tables | Delivery delays, geographic analysis, seller risk, review impact | pandas, seaborn, matplotlib |
| [UK Online Retail](./eda/uk-retail/) | ~500K transactions, ~13 months | Revenue trends, Pareto concentration, cohort retention, top products | pandas, matplotlib, seaborn |

---

## ML Projects

| Project | Dataset | Type | Status |
|---|---|---|---|
| *(coming soon)* | | | |

---

## Repository Structure

```
data-portfolio/
│
├── eda/
│   ├── telco-churn/
│   ├── forbes-athletes/
│   ├── olist-ecommerce/
│   └── uk-retail/
│
└── ml-projects/
```

Each project folder contains:
- A Jupyter notebook with the full analysis
- A `README.md` with problem statement, findings, and data source
- A `data/` folder (large files are gitignored — see each project's README for download instructions)

---

## Setup

```bash
# Clone the repo
git clone https://github.com/<your-username>/data-portfolio.git
cd data-portfolio

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy openpyxl
```

Notebooks were developed with Python 3.10+. No additional configuration needed — just download any large data files listed in the project READMEs and place them in the corresponding `data/` folder.
