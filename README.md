# 📊 Telco Customer Churn Analysis


📌 Project Overview

This project performs a comprehensive Exploratory Data Analysis (EDA) on the Telco Customer Churn Dataset — a widely used, real-world telecom industry dataset that captures detailed service, contract, and billing information for over 7,000 customers. The goal is to uncover meaningful patterns and insights about customer churn behaviour, high-risk customer segments, the impact of contract types and billing methods, and the financial cost of customer loss.

By analysing the dataset across multiple dimensions — tenure, monthly charges, service subscriptions, and demographic attributes — this project produces a clean, enriched analytical view that enables multi-dimensional exploration of why customers leave, who is most at risk, and how much revenue the business stands to lose or recover through smarter retention strategies.

## 🎯 Business Problem

A telecommunications company is experiencing significant customer churn — customers cancelling their subscriptions every month. The business needs to understand:

- **Who** is most likely to churn
- **Why** they churn (key drivers)
- **How much** revenue is at risk ($)
- **What** interventions will have the highest ROI

> **Churn rate: 26.5%** — 1 in 4 customers leaves every period.

---

## 📁 Project Structure

```
telco-churn-analysis/
│
├── data/
│   └── Telco-Customer-Churn.csv          # Raw dataset (7,043 rows × 21 cols)
│
├── notebooks/
│   └── Telco_Churn_EDA_Annotated.ipynb   # Full EDA with inline comments
│
├── outputs/
│   ├── distributions1.png                 # Tenure / Charges distribution plots
│   ├── distributions2.png                 # Contract / Internet / Payment charts
│   ├── Patterns and Relationships.png     # Churn by contract, internet, tenure
│   ├── Correlation.png                    # Correlation heatmap
│   ├── Summarize & Communicate Results.png# Top churn risk factors bar chart
│   └── Business case.png                  # Retention ROI chart
│
├── report/
│   └── Telco_Churn_Project_Report.html   # Full project report
│
├── presentation/
│   └── Telco_Churn_Portfolio.pptx        # 9-slide stakeholder presentation
│
└── README.md
```

---

## 🔍 Dataset Overview

| Property | Value |
|----------|-------|
| Source | IBM Sample Telco Dataset |
| Rows | 7,043 customers |
| Features | 21 columns |
| Target | `Churn` (Yes/No) |
| Class balance | 73.5% No / 26.5% Yes |

**Feature categories:** Demographics · Services · Account Info · Financials

---

## 🛠️ Workflow

```
1. Import Data         → pd.read_csv, data.head(), data.shape
2. Explore Structure   → dtypes, value_counts, group comparisons
3. Clean Data          → pd.to_numeric, dropna, IQR outlier check
4. Descriptive Stats   → describe(), groupby mean comparison
5. Distributions       → Overlapping histograms (churned vs retained)
6. Patterns            → Churn rate by contract, internet, tenure cohort
7. Correlations        → Pearson matrix, heatmap
8. Business Insights   → Segment churn rates, horizontal bar chart
9. ROI Model           → Retention scenario analysis, unit economics
```

---

## 📈 Key Findings

### Churn Rate by Segment

| Segment | Churn Rate | Risk |
|---------|-----------|------|
| Tenure < 12 months | **47.7%** | 🔴 High |
| Electronic check payment | **45.3%** | 🔴 High |
| Month-to-month contract | **42.7%** | 🔴 High |
| Fiber optic internet | **41.9%** | 🔴 High |
| Senior citizen | **41.7%** | 🔴 High |
| One-year contract | 11.3% | 🟡 Medium |
| Two-year contract | **2.8%** | 🟢 Low |

### Numeric Correlations with Churn

| Feature | r | Direction |
|---------|---|-----------|
| Tenure | **-0.354** | Longer tenure → much lower churn |
| TotalCharges | -0.199 | Higher lifetime spend → lower churn |
| MonthlyCharges | +0.193 | Higher monthly bill → slight churn signal |

### Churned vs Retained — Average Metrics

| Metric | Churned | Retained |
|--------|---------|----------|
| Avg Tenure | 18.0 months | 37.7 months |
| Avg Monthly Charges | $74.4 | $61.3 |
| Avg Total Charges | $1,532 | $2,556 |

---

## 💰 Business Case — Retention ROI

| Retention Rate | Customers Saved | Net Annual Value |
|---------------|----------------|-----------------|
| 5% | 93 | **$101,169** |
| 10% | 187 | **$202,339** |
| 15% | 280 | **$303,508** |
| 20% | 374 | **$404,678** |
| 25% | 467 | **$505,847** |

**Unit economics:**
- Cost to **acquire** 1 customer: ~**$324** (5× avg monthly charge)
- Cost to **retain** 1 customer: ~**$32** (0.5× avg monthly charge)
- **10× cheaper** to retain than acquire

---

## ✅ Recommendations

| # | Action | Target Segment | Expected Impact |
|---|--------|---------------|-----------------|
| 01 | Contract upgrade incentive (10–15% discount) | Month-to-month, tenure 12–24 mo | Churn: 42.7% → ~25% |
| 02 | Loyalty programme at 3 & 6 month marks | New customers (<12 mo) | Reduce 47.7% cohort drop-off |
| 03 | Dedicated support + value communication | Fiber optic customers | Close value-price perception gap |
| 04 | Auto-pay migration ($5/mo discount) | Electronic check users | Remove friction, reduce 45.3% churn |

---

## 🚀 How to Run


# Clone the repo
git clone https://github.com/Birender8265/telco-churn-analysis.git

cd telco-churn-analysis



---

## 📦 Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
jupyter>=1.0
```

---

## 📬 Contact

Built as part of an industry-standard end-to-end data analytics portfolio project.  
Feel free to fork, star ⭐, or raise an issue!
