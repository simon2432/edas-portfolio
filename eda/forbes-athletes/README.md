# Forbes Highest-Paid Athletes — EDA

**Goal:** Understand how the Forbes top-10 highest-paid athletes list has evolved over three decades — earnings growth, sport dominance, and earnings concentration.

---

## Dataset

| | |
|---|---|
| **Source** | [Forbes Richest Athletes (Kaggle)](https://www.kaggle.com/datasets/parulpandey/forbes-highest-paid-athletes-19902019/data) |
| **Size** | 301 rows (top 10 per year, 1990–2020) |
| **Columns** | Rank, athlete name, nationality, sport, total earnings |

---

## Key Questions

1. How have total top-10 earnings grown over 30 years?
2. Which sports consistently dominate the list, and has that changed?
3. Are earnings becoming more concentrated in fewer athletes — or less?
4. How global is the list? How has the non-US share evolved?

---

## Main Findings

- **Total earnings grew ~5–6× in nominal terms** between 1990 and 2020, with notable jumps in certain years (e.g. 2015, 2018).
- **Sport dominance shifted:** boxing and tennis were strongest in the early 1990s; basketball dominated the middle period; soccer has led in the last decade.
- **Concentration did not increase.** The share of total top-10 earnings going to the #1, top 3, and top 5 athletes was *lower* in 2006–2020 than in 1990–2005. Within this slice, earnings became slightly *less* concentrated over time, not more.
- **Linear trends** for concentration metrics (Top1%, Top3%, Top5%) are slightly negative across the full period — consistent with the two-period comparison.
- **Geography:** the majority of appearances are from the USA. UK, Germany, Switzerland, Portugal, and Brazil account for most non-US entries.

---

## Data setup

Download `forbes_richest_athletes.csv` from [Kaggle](https://www.kaggle.com/datasets/parulpandey/forbes-highest-paid-athletes-19902019/data) and place it in the `data/` folder.

> All files in `data/` are gitignored.

## Structure

```
forbes-athletes/
├── eda_forbes_athletes.ipynb
└── data/
    └── .gitkeep
```

---

## Tools

`pandas` · `matplotlib` · `scipy`
