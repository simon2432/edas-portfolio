# EDA Portfolio

A collection of exploratory data analysis projects. Each project includes a focused problem statement, exploratory analysis, and actionable findings.

---

## Projects

| Project                                                | Dataset                             | Key Topics                                                           | Tools                       |
| ------------------------------------------------------ | ----------------------------------- | -------------------------------------------------------------------- | --------------------------- |
| [Telco Customer Churn](./eda/telco-churn/)             | 7K telecom customers (California)   | Churn drivers, high-risk segmentation, A/B test design               | pandas, seaborn, matplotlib |
| [Forbes Highest-Paid Athletes](./eda/forbes-athletes/) | Top 10 athletes per year, 1990–2020 | Earnings trends, sport dominance, concentration analysis             | pandas, scipy, matplotlib   |
| [Olist E-Commerce (Brazil)](./eda/olist-ecommerce/)    | ~100K orders, multiple tables       | Delivery delays, geographic analysis, seller risk, review impact     | pandas, seaborn, matplotlib |
| [UK Online Retail](./eda/uk-retail/)                   | ~500K transactions, ~13 months      | Revenue trends, Pareto concentration, cohort retention, top products | pandas, matplotlib, seaborn |

---

## Setup — Conda environment

All projects share the same environment. Follow these steps to set it up:

**1. Clone the repository**

```bash
git clone https://github.com/simon2432/data-portfolio.git
cd data-portfolio
```

**2. Create the conda environment**

```bash
conda create -n data-portfolio python=3.10
conda activate data-portfolio
```

**3. Install dependencies**

```bash
pip install -r eda/requirements.txt
```

**4. Register the environment as a Jupyter kernel**

```bash
python -m ipykernel install --user --name data-portfolio --display-name "Python (data-portfolio)"
```

**5. Launch Jupyter**

```bash
jupyter notebook
```

Then select the `Python (data-portfolio)` kernel when opening any notebook.

**6. Download the data**

Each project's `data/` folder is gitignored. See the individual project READMEs for the Kaggle download link and the files you need to place in `data/`.

---

## Repository Structure

```
data-portfolio/
│
├── README.md
├── .gitignore
│
└── eda/
    ├── requirements.txt         ← shared dependencies for all projects
    ├── telco-churn/
    ├── forbes-athletes/
    ├── olist-ecommerce/
    └── uk-retail/
```

Each project folder contains:

- A Jupyter notebook with the full analysis (`eda_<project>.ipynb`)
- A `README.md` with problem, findings, and data download instructions
- A `data/` folder with a `.gitkeep` (populate locally after downloading from Kaggle)
