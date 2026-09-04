# Submission Criteria — 01-ml-project (Customer Segmentation)

Read this **before you start working**, not the night before the deadline. It tells you exactly what a complete submission looks like for this project, what you are free to decide yourselves, and what will get your work sent back as "Needs revision."

Every project folder in this repo has its own `SUBMISSION_CRITERIA.md`. The general git and naming rules live in `SUBMISSION_GUIDE.md` — this file is only about *this* project's content.

**Submitted per group**, not per person. There are three dates — see `SUBMISSION_GUIDE.md` §3 for why:

| | A3 (Tue/Sat) | A1 (Mon/Thu) |
|---|---|---|
| **QA cutoff** — push your best working version for mentor review | **Wed 26/08/2026** | **Fri 28/08/2026** |
| **Mentor review posted** | Fri 28/08/2026 | Sun 30/08/2026 |
| **Final deadline** — fixes pushed; this is what gets graded | **Sat 29/08/2026** (Session 10) | **Mon 31/08/2026** (Session 10) |

Session 10 is also when the discussion round for this project starts. A3 groups all present that session; A1 groups present across S10–S13 — check `discussion/a1-discussion-schedule.md` for your slot.

---

## 1. What you submit

Exactly these files, inside your own group's folder:

```
submissions/<cohort>/<group-id>/01-ml-project/
├── <group-id>_01-ml-project.ipynb      ← required, one notebook
└── <group-id>_recap.md                 ← A1 groups only, and only if you are NOT spotlighted this session
```

Example for A1 group 7: `submissions/a1-mon-thu/a1-g07/01-ml-project/a1-g07_01-ml-project.ipynb`

- One notebook per group. Not one per student, not three notebooks split by task.
- The persona summary is **the last section of that same notebook**, clearly separated by a markdown heading. A separate PDF or Word file is not required and does not replace the notebook section.
- Load the dataset from the repo path `01-ml-project/retail_transactions_segmentation.csv` (a relative path is fine). Do not copy the CSV into your submission folder, and do not load it from your own Desktop or Drive path — your mentor has to be able to run your notebook.

---

## 2. Delivery criteria, point by point

Your notebook must contain all six points below, each as a **labelled markdown section**. This is the checklist your mentor works through — anything missing is an automatic "Needs revision."

### Point 1 — RFM feature table built from the raw transactions

- Start from the transaction-level CSV (3,663 rows) and produce a **customer-level** table (300 rows, one per `customer_id`).
- **Recency** = days since that customer's most recent purchase, measured from a **fixed reference date you state explicitly** (e.g. the dataset's max `transaction_date`, or 2024-12-31). Say which one you used.
- **Frequency** = number of transactions for that customer.
- **Monetary** = total *or* average spend per customer — your choice, but state which one you picked.
- Show the resulting table (`.head()` and `.shape`) so it is visible that you actually built it.

*Not accepted:* feeding raw transaction rows or the `amount` column straight into clustering without building the RFM table.

### Point 2 — Features scaled before clustering

- Standardize the three RFM columns (e.g. `StandardScaler`) and cluster on the scaled values.
- One sentence on *why* scaling is needed here — days, transaction counts and money are on completely different scales.

*Not accepted:* fitting K-Means on unscaled RFM. This is the most common mistake in this project.

### Point 3 — Choice of k justified with evidence

- Run **both** the elbow method (inertia vs. k) and the silhouette score across a range of k (e.g. 2–10).
- Plot both.
- Write 2–4 sentences stating which k you chose and *what in those plots led you there*.

*Not accepted:* "we chose k=4" with no plots, or plots with no written reasoning. A well-reasoned k=3 scores higher than an unexplained k=5.

### Point 4 — K-Means fitted with your chosen k

- Fit K-Means on the scaled features using the k you justified in Point 3.
- Set `random_state` so your results are reproducible.
- Attach the cluster label back onto each customer in the RFM table.

### Point 5 — PCA visualization of the clusters

- Reduce the scaled features to 2 components with PCA and produce a scatter plot coloured by cluster label.
- The plot must be readable: axis labels, a legend or colour key, and a title.

*Not accepted:* an unlabelled plot, or one where the clusters are indistinguishable because no colour mapping was applied.

### Point 6 — Named personas grounded in the numbers

- Show the **mean Recency / Frequency / Monetary per cluster** as a small table — this is your evidence.
- Give every cluster a real business name (e.g. "VIP", "At-risk", "New/Occasional", "Dormant"). Not "Cluster 0".
- Write **2–3 sentences per persona**: who they are, and what the business should do *differently* for this group.

*Not accepted:* persona names that contradict the cluster's own RFM averages — for example calling a high-recency, low-frequency, low-spend cluster "VIP". Your names have to follow from your table.

---

## 3. Also required

- **Runs top to bottom.** Restart & Run All must complete with no errors, and the outputs must be saved in the notebook you commit. A notebook your mentor cannot execute is not a submission.
- **Narrative, not just code.** Markdown cells explaining what each section does and why. A wall of unexplained code fails the Clarity check in the QA review.
- **A1 groups not in this session's spotlight:** add `<group-id>_recap.md` — 4–6 sentences covering what you built, your key decision or result, and one open question. Check `discussion/a1-discussion-schedule.md` to see whether you are spotlighted. A3 groups all present live, so no recap is needed.

---

## 4. What you are free to decide

These are genuinely your call. You will not lose marks for the choice itself — only for not stating it.

- Monetary as total spend or average spend.
- The reference date used for Recency.
- The value of k, as long as Point 3's evidence supports it.
- The range of k you sweep.
- Plot styling and library (matplotlib, seaborn, plotly — anything that renders in the committed notebook).
- Extra work beyond the brief: outlier handling, log-transforming Monetary, comparing K-Means against another clustering algorithm, breaking down `product_category` per persona. This is bonus, not required — keep it clearly separated from the six required points so nothing looks missing.

---

## 5. What gets your submission returned

- Any of the six points missing or unlabelled.
- Clustering on unscaled features.
- k chosen with no elbow or silhouette evidence.
- Personas left as "Cluster 0/1/2", or persona names that don't match their RFM averages.
- Errors on Restart & Run All, or a notebook committed with its outputs stripped out.
- Wrong filename or wrong folder — see `SUBMISSION_GUIDE.md` §1.
- Files added or edited **outside your own group's folder**.
- Work copied from another group. Groups reaching a similar k is expected; identical notebooks are not.

---

## 6. How it's judged

Your mentor reviews against this file using `templates/QA_REVIEW_TEMPLATE.md`, marks **Approved** or **Needs revision**, and commits the review as `<group-id>_qa-review.md` next to your notebook. Approved submissions move on to the instructor's final review. "Needs revision" means: fix what the notes say, commit, pull, push again — treat it as required, not optional.

What earns a strong review, in priority order:

1. **Correct method** — RFM built properly, features scaled, K-Means fitted on the scaled data.
2. **Justified k** — the reasoning matters more than the number.
3. **Personas that make business sense** — grounded in the cluster averages, and actionable.
4. **A notebook someone else can read and run.**

---

## 7. Final self-check before you push

- [ ] Notebook at `submissions/<cohort>/<group-id>/01-ml-project/<group-id>_01-ml-project.ipynb`
- [ ] All six points present as labelled markdown sections
- [ ] RFM table is customer-level (300 rows) and visible in the output
- [ ] Reference date for Recency stated; total-vs-average Monetary stated
- [ ] Features scaled before K-Means
- [ ] Elbow **and** silhouette plotted, with written reasoning for your k
- [ ] `random_state` set on K-Means
- [ ] PCA scatter plot labelled and coloured by cluster
- [ ] Per-cluster RFM mean table shown
- [ ] Every cluster has a business name plus 2–3 sentences
- [ ] Restart & Run All passes, outputs saved
- [ ] Dataset loaded from the repo path, not a local machine path
- [ ] Recap file added if your A1 group isn't spotlighted this session
- [ ] Nothing changed outside your group's folder — run `git status` to confirm
- [ ] `git pull origin main` done before pushing
