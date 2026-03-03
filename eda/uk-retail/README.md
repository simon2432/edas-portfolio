# UK Online Retail — EDA

**Goal:** Understand revenue patterns, customer concentration, cohort retention, and product performance for a UK-based online retailer.

---

## Dataset

| | |
|---|---|
| **Source** | [E-Commerce Data (Kaggle)](https://www.kaggle.com/datasets/carrie1/ecommerce-data) |
| **Size** | ~500K transactions before cleaning |
| **Period** | ~13 months of transaction data |
| **Geography** | Primarily UK, with international orders |

---

## Key Questions

1. What is the revenue trend over time, and is there seasonality?
2. How concentrated is revenue across customers (Pareto distribution)?
3. Who are the top 20% of customers — and what do they look like?
4. What does cohort retention look like month over month?
5. Which products drive the most revenue?

---

## Main Findings

- **Seasonality is clear:** December is the peak month (holiday demand). February and April show dips; the rest of the year is relatively stable.
- **Revenue is highly concentrated:** the top 20% of customers account for ~75% of total revenue — a near-Pareto distribution.
- **Customer revenue is heavy-tailed:** a small number of very high-spenders pull the distribution significantly, visible on a log scale.
- **Cohort retention is moderate:** sharp drop-off in months 1–2 is typical for this category. Customers who stay past month 2 tend to show better long-term retention.
- **UK dominates:** the vast majority of revenue and customers are from the United Kingdom.
- **Top products:** REGENCY CAKESTAND 3 TIER, PAPER CRAFT items, and seasonal decorations are consistently strong revenue drivers.

---

## Recommendations

1. **Protect the top 20%** — these customers are disproportionately valuable; a VIP or loyalty program is worth the investment.
2. **Reduce early drop-off** — focus retention efforts in months 1–2 (drip campaigns, post-purchase follow-up, early incentives).
3. **Diversify geography** — Netherlands, Ireland, and Germany already show traction; worth testing more targeted marketing there.
4. **Lean into Q4 seasonality** — start pre-holiday campaigns in October–November, plan inventory ahead of the December peak.

---

## Data setup

Download `ecom_data.csv` (~43 MB) from [Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data) and place it in the `data/` folder.

> All files in `data/` are gitignored.

## Structure

```
uk-retail/
├── eda_uk_retail.ipynb
└── data/
    └── .gitkeep
```

---

## Tools

`pandas` · `numpy` · `matplotlib` · `seaborn`
