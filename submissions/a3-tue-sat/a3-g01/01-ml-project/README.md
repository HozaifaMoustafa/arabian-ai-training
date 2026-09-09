# 🛍️ Customer Segmentation ML Project — Cohort A3 Group 01

**Course**: AI Engineering Track (Machine Learning Module)  
**Instructor**: Hozaifa Moustafa (Arabian Academy)  
**Group**: `a3-g01` (Cohort A3 — Tue/Sat)  
**Notebook**: [`customer_segmentation.ipynb`](customer_segmentation.ipynb)

---

## 📌 Project Overview

This project transforms 1 year of raw retail transaction logs (`3,663` transactions across `300` unique customers from Jan 1 to Dec 30, 2024) into actionable customer segments using unsupervised machine learning.

### Pipeline Highlights
1. **Data Quality & EDA**: Complete validation (0 nulls, date/amount sanity, multi-purchase analysis, category balance).
2. **RFM Feature Engineering**: Customer-level aggregation of Recency ($R$), Frequency ($F$), and Monetary ($M$) using baseline date `2024-12-31`.
3. **Skewness & Scaling**: Right-skewness reduction via `np.log1p` and feature standardization via `StandardScaler`.
4. **Optimal $k$ Evaluation**: Multi-metric sweep $k \in [2, 8]$ using Elbow Method (WCSS), Silhouette Score, and Davies-Bouldin Index justifying optimal **$k=4$**.
5. **K-Means & PCA 2D Reduction**: Model fitting with `KMeans(k=4, random_state=42)` and PCA projection retaining **99.53% explained variance** with annotated centroids.
6. **Personas & Business Strategy**: 4 named customer personas grounded in unscaled RFM profile metrics with targeted strategic recommendations.

---

## 📂 Project Structure

```
01-ml-project/
├── customer_segmentation.ipynb        # Master Jupyter Notebook (complete 7-section pipeline & outputs)
├── retail_transactions_segmentation.csv # Raw transaction dataset (3,663 rows, 300 customers)
├── retail_transactions_cleaned.csv     # Cleaned transaction dataset
├── SUBMISSION_CRITERIA.md              # Project submission checklist & requirements
└── README.md                           # Project guide and overview
```

---

## 👥 Customer Personas & Revenue Impact

| Persona Name | Cluster | Customer Count (%) | Total Spend ($) | Revenue Share (%) | Mean Recency | Mean Freq | Mean Spend | Recommended Action |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| 🌟 **VIP Champions** | `Cluster 0` | 55 (18.3%) | $1,272,704.38 | **67.7%** | 7.0 days | 29.9 tx | $23,140.08 | Exclusive VIP loyalty, dedicated concierge, early product access. |
| 💎 **Core Loyal Spenders** | `Cluster 3` | 111 (37.0%) | $514,053.39 | **27.3%** | 22.6 days | 13.4 tx | $4,631.11 | Cross-sell product bundles, tier-upgrade incentives. |
| ⚠️ **At-Risk Occasional** | `Cluster 1` | 69 (23.0%) | $67,687.09 | **3.6%** | 56.6 days | 5.5 tx | $980.97 | "We Miss You" win-back coupons, feedback surveys. |
| 💤 **Dormant / Churned** | `Cluster 2` | 65 (21.7%) | $24,778.08 | **1.3%** | 147.7 days | 2.3 tx | $381.20 | Minimize ad spend, send mass clearance emails only. |

---

## 🚀 How to Run

1. **Environment Requirements**:
   - Python 3.10+
   - Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

2. **Execution**:
   Open Jupyter Notebook or JupyterLab and execute all cells in [`customer_segmentation.ipynb`](customer_segmentation.ipynb) from top to bottom:
   ```bash
   jupyter notebook customer_segmentation.ipynb
   ```
