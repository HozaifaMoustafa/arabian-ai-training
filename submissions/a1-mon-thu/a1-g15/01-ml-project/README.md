# Customer Segmentation — RFM + K-Means

**Project 1 · AI Engineering Track**

RFM analysis + K-Means clustering on one year of retail transactions, segmenting 300 customers into three actionable personas.

---

## 📁 Contents

| File | Description |
|---|---|
| `<group-id>_01-ml-project.ipynb` | Full notebook: cleaning, RFM, scaling, elbow/silhouette, K-Means, PCA, personas |
| `RFM_clustered.csv` | Final customer-level table with Recency, Frequency, Monetary, Cluster, and Persona |
| `README.md` | This file — project summary |

---

## 1. Objective

Segment 300 retail customers into distinct, actionable groups based on purchasing behavior, using the RFM framework (Recency, Frequency, Monetary) combined with K-Means clustering, and translate the resulting clusters into business personas with concrete recommendations.

**Dataset:** `retail_transactions_segmentation.csv` — 3,663 transactions, 300 unique customers, Jan 1 – Dec 30, 2024. Columns: `customer_id`, `transaction_date`, `amount`, `product_category`.

---

## 2. Data Cleaning & Preparation

| Check | Result |
|---|---|
| Missing values | None |
| Fully duplicated rows | None |
| Duplicates on (customer_id, date, amount) | None |
| Transactions with amount ≤ 0 | None |
| Date parsing errors | None |
| Whitespace-only / padded string values | None |
| Product categories | 6 valid categories, no inconsistencies |

The dataset required no row removal — cleaning steps (drop-duplicates, positive-amount filter, whitespace strip) were applied as safeguards but changed nothing, since the raw data was already clean. `transaction_date` was converted to `datetime` for the Recency calculation.

---

## 3. RFM Feature Engineering

Aggregated from transaction-level to customer-level:

- **Recency** — days since the customer's last purchase (relative to Jan 1, 2025, one day after the latest transaction date)
- **Frequency** — total number of transactions
- **Monetary** — total amount spent

| Metric | Mean | Std | Min | Max |
|---|---|---|---|---|
| Recency (days) | 54.7 | 68.3 | 1 | 337 |
| Frequency (# transactions) | 12.2 | 10.6 | 1 | 45 |
| Monetary ($) | 6,264.1 | 9,659.8 | 71.9 | 39,424.1 |

---

## 4. Scaling

RFM features were standardized with `StandardScaler` (mean 0, std 1) before clustering, since K-Means relies on Euclidean distance and Monetary's raw scale would otherwise dominate Recency/Frequency.

---

## 5. Choosing k

**Elbow Method:** inertia drops sharply from k=1 to k=3, then flattens from k=4 onward — elbow around k=3.

**Silhouette Score:**

| k | Score |
|---|---|
| 2 | 0.6789 |
| **3** | **0.6782** |
| 4 | 0.5702 |
| 5 | 0.5232 |
| 6 | 0.5194 |
| 7 | 0.4626 |
| 8 | 0.4815 |
| 9 | 0.4822 |
| 10 | 0.4765 |

**Decision: k = 3.** k=2 scored marginally higher (0.6789 vs. 0.6782), but the gap is negligible. k=3 was chosen because it yields more business-actionable segments without meaningful loss in cluster quality, and scores drop sharply from k=4 onward — both elbow and silhouette independently support k=3.

---

## 6. Clustering Results

K-Means fit with k=3 (`random_state=42`, `n_init=10`):

| Cluster | Customers | Recency (days) | Frequency | Monetary ($) |
|---|---|---|---|---|
| 0 | 40 | 8.40 | 35.00 | 29,683.61 |
| 1 | 238 | 43.59 | 9.32 | 2,876.90 |
| 2 | 22 | 258.59 | 2.09 | 326.14 |

### RFM Matrix

| Cluster | Recency | Frequency | Monetary |
|---|---|---|---|
| 0 | High | High | High |
| 1 | Medium | Medium | Medium |
| 2 | Low | Low | Low |

All three RFM dimensions agree consistently within each cluster — a clean, non-contradictory pattern.

### PCA Visualization

- PC1 explained variance: 75.03%
- PC2 explained variance: 23.72%
- **Total variance captured: 98.75%**

Three visually well-separated clusters with minimal overlap — confirms the clusters reflect genuinely distinct behavior, not an arbitrary split.

---

## 7. Personas & Business Recommendations

### 🟦 VIP / High-Value Customers — 40 customers (13.3%)
`Recency 8.4d · Frequency 35 · Monetary $29,683.61`

Purchase frequently, spend by far the most, and bought most recently. Core of the business's revenue despite being a small share of the base.
**Action:** prioritize retention — loyalty rewards, early access, premium support. Avoid generic discounts on customers who already buy without them.

### 🟨 Regular Customers — 238 customers (79.3%)
`Recency 43.6d · Frequency 9.3 · Monetary $2,876.90`

The largest group, purchasing roughly every six weeks with moderate spend. Engaged but with significant untapped growth potential.
**Action:** cross-sell/upsell campaigns, personalized recommendations, engagement nudges to push more of this group toward VIP status.

### 🟥 Dormant / At-Risk Customers — 22 customers (7.3%)
`Recency 258.6d · Frequency 2.1 · Monetary $326.14`

Haven't purchased in over 8 months on average, minimal historical spend. High risk of full churn.
**Action:** low-cost win-back campaigns only. Avoid heavy marketing spend here — ROI on aggressive re-engagement is typically low for this segment.

---

## 8. Summary

| Segment | Share | Priority |
|---|---|---|
| VIP | 13.3% | Retain — highest priority |
| Regular | 79.3% | Grow — biggest opportunity |
| Dormant | 7.3% | Low-cost reactivation only |

Segmentation is clean and well-separated (PCA captures 98.75% of variance in 2D) and directly actionable: retention effort on VIPs, growth investment on the Regular majority, minimal spend on the Dormant tail.

---

## Methodology Notes (for Q&A)

- **Why StandardScaler before K-Means?** K-Means uses Euclidean distance; without scaling, Monetary (thousands) would dominate Recency (tens/hundreds of days) purely due to raw magnitude.
- **Why k=3 and not the argmax silhouette pick (k=2)?** The two scores are statistically tied (0.6789 vs 0.6782); k=3 gives finer, more business-actionable segmentation without meaningfully sacrificing cluster quality.
- **Why persona names assigned after printing cluster profiles, not before?** K-Means cluster indices (0, 1, 2) are arbitrary — they carry no inherent order. Names must be mapped to the printed R/F/M values, not assumed in advance.
- **Why PCA on `scaled_rfm`, not raw RFM?** The visualization must reflect the same distances K-Means actually used; PCA on unscaled data would show a different (misleading) geometry.
