# Olist E-Commerce (Brazil) — EDA

**Goal:** Identify the main drivers of delivery delays and quantify their impact on customer satisfaction (review scores).

---

## Dataset

| | |
|---|---|
| **Source** | [Brazilian E-Commerce Public Dataset by Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) |
| **Size** | ~100K orders, multiple relational tables |
| **Period** | January 2017 – August 2018 |
| **Scope** | Delivered orders with valid delivery dates |

> **Note:** Large data files are not tracked in this repo. Download the dataset from the Kaggle link above and place the CSV files in the `data/` folder before running the notebook.

---

## Key Questions

1. What share of orders arrive late, and how late are they?
2. Do late delivery rates vary by region (customer state, seller state)?
3. Which sellers have the worst combination of volume and late rate?
4. How strongly does late delivery affect review scores?

---

## Main Findings

- **~7% of delivered orders arrive after the estimated date.** Most late deliveries are in the 1–7 day range; a smaller tail extends beyond 30 days.
- **Geographic variation is significant.** States like AL, MA, SE, PI, and CE (as destinations) show the highest late rates. Sellers in AM and MA also show elevated rates at the origin.
- **87 high-risk sellers** are in the top quartile for both order volume and late delivery rate — a small group responsible for a disproportionate share of delays.
- **Late delivery has a clear, monotonic impact on reviews:**
  - On-time: ~9% low ratings (1–2 stars), avg score ~4.3
  - Late 1–7 days: ~50% low ratings
  - Very late 8–30 days: ~81% low ratings, avg score ~1.65
- High-risk sellers also receive significantly worse average review scores than the rest.

---

## Recommendations

1. **Focus on the 87 high-risk sellers** — tighter SLAs, preferred carrier requirements, dedicated support.
2. **Target high-late-rate destination states** — improve carrier coverage or adjust estimated delivery dates by corridor.
3. **Track the same metrics post-intervention:** late delivery rate, % low-star reviews, seller compliance.

---

## Structure

```
olist-ecommerce/
├── eda_olist_ecommerce.ipynb   ← main analysis
└── data/
    ├── olist_sellers_dataset.csv                  ← included (small)
    ├── product_category_name_translation.csv      ← included (small)
    ├── olist_orders_dataset.csv                   ← download from Kaggle
    ├── olist_order_items_dataset.csv              ← download from Kaggle
    ├── olist_order_reviews_dataset.csv            ← download from Kaggle
    ├── olist_customers_dataset.csv                ← download from Kaggle
    ├── olist_order_payments_dataset.csv           ← download from Kaggle
    ├── olist_products_dataset.csv                 ← download from Kaggle
    └── olist_geolocation_dataset.csv              ← download from Kaggle
```

---

## Tools

`pandas` · `numpy` · `matplotlib` · `seaborn`
