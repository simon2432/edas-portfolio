# Telco Customer Churn — EDA

**Goal:** Identify the main drivers of customer churn and define a high-risk segment for targeted retention.

---

## Dataset

| | |
|---|---|
| **Source** | [IBM Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) |
| **Size** | 7,043 customers × 33 columns |
| **Geography** | California, USA |
| **Target** | `Churn Label` (Yes / No) — baseline churn rate: **26.5%** |

The dataset includes demographics, account info, contracted services (internet, phone, streaming), billing details, and churn outcome.

---

## Key Questions

1. Which variables are most associated with churn?
2. Is early tenure a risk indicator?
3. Does contract type explain a large part of the churn gap?
4. Is there a high-risk segment we can define and target?
5. Does Tech Support appear to have a protective effect for high-risk customers?

---

## Main Findings

- **Contract type is the strongest single driver.** Month-to-month (M2M) customers churn at dramatically higher rates than one- or two-year contract holders.
- **Early tenure is critical.** Churn is highest in the first 12 months and drops steadily after that. The retention window is front-loaded.
- **High charges amplify the risk.** High monthly charges combined with M2M contracts produce the worst outcomes.
- **High-risk segment** (Tenure ≤ 6 months + M2M + Monthly Charges > $70): a small portion of customers responsible for a disproportionate share of total churn.
- **Tech Support shows a protective pattern** within the Fiber + M2M segment, even after controlling for price — but this is observational. An A/B test is needed to confirm.

---

## Recommendation

Run a controlled experiment offering free Tech Support for the first 3 months to Fiber + M2M customers. Track 6-month churn, retention curve, and cost per retained customer.

---

## Structure

```
telco-churn/
├── eda_telco_churn.ipynb   ← main analysis
└── data/
    ├── Telco_customer_churn.xlsx             ← main merged file (used by notebook)
    ├── Telco_customer_churn_demographics.xlsx
    ├── Telco_customer_churn_location.xlsx
    ├── Telco_customer_churn_population.xlsx
    ├── Telco_customer_churn_services.xlsx
    └── Telco_customer_churn_status.xlsx
```

---

## Tools

`pandas` · `numpy` · `matplotlib` · `seaborn`
