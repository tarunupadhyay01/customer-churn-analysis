# Customer Churn Analysis & Exploration

**CodeNova AI/ML Internship – Batch 02 | Task 1**

Exploratory data analysis of the public **Telco Customer Churn** dataset (IBM sample data, 7,043 customers, 21 columns) to find what drives customers to leave and what a retention team could do about it.

## Key insights
| Driver | Evidence |
|---|---|
| Overall churn | 26.5% (1,869 of 7,043 customers) |
| Contract type | Month-to-month 42.7% vs one-year 11.3% vs two-year 2.8% |
| Tenure | 47.4% churn in months 0-12, falling to 9.5% after 48 months; median tenure 10 (churned) vs 38 (retained) |
| Monthly charges | Median $79.65 (churned) vs $64.43 (retained) |
| Internet service | Fiber optic 41.9% vs DSL 19.0% |
| Payment method | Electronic check 45.3% vs 15-19% for others |
| Support services | No tech support 41.6% vs 15.2% with it |
| Senior citizens | 41.7% vs 23.6% |

**Recommendations:** move new customers to longer contracts, improve first-year onboarding, bundle tech support/security, promote automatic payments, and investigate fiber-optic pricing and quality. These are associations, not proven causes.

## Data characteristics
- 7,043 rows, no duplicate customer IDs.
- `TotalCharges` had 11 blank values, all with `tenure = 0` (new customers), so they were set to 0.
- Classes are imbalanced (~73% stayed / ~27% churned).

## Visualizations (`images/`, 300 dpi)
1. `01_churn_distribution.png`
2. `02_churn_by_contract.png`
3. `03_tenure_monthly_charges.png`
4. `04_churn_by_tenure_group.png`
5. `05_other_drivers.png`
6. `06_correlation_heatmap.png`

## Tech stack
Python 3, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook. No paid tools or APIs.

## Setup
```bash
git clone <your-repo-url>
cd <repo-folder>
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Customer_Churn_Analysis.ipynb
```
The dataset is included at `data/Telco-Customer-Churn.csv`.

## Project structure
```
├── Customer_Churn_Analysis.ipynb   # executed notebook with commentary
├── data/Telco-Customer-Churn.csv
├── images/                         # exported charts
└── README.md
```

## Dataset source
IBM Telco Customer Churn sample dataset (also on Kaggle as "Telco Customer Churn").
