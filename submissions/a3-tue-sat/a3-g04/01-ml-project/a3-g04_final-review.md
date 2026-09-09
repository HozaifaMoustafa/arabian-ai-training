# Final Review — a3-g04 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a3-g04` — Ramy Magdy, Saad Khaled, Haitham Shabah, Ahmed Mohamed  
**Cohort:** A3 (Tue/Sat)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `35aa8ac` — *a3-g04: submit 01-ml-project* (PR #41, 07/09/2026)

This is the instructor's final review, re-issued after your catch-up delivery. The 04/09 version recorded this project as not submitted; you delivered on the deadline, so that outcome is replaced — but the delivery is not yet a submission under `SUBMISSION_CRITERIA.md`.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Sun 13/09/2026** — the fixes in §3 must be pushed before the final catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

**This is the last extension.** After 13/09 the outcome is recorded as it stands.

## 2. What worked

You delivered by the deadline, and the 42 lines you wrote are correct as far as they go. That is not nothing, so let me be specific about what is right in them:

- Your RFM aggregation is textbook: `ref_date = max(transaction_date) + 1 day`, then a single `groupby("customer_id").agg(...)` producing Recency, Frequency and Monetary in one pass. The `+ 1 day` is a deliberate touch — it stops your most recent buyer landing on a Recency of zero. Several groups missed that.
- You scale before you cluster. `StandardScaler` on the three RFM columns, and `fit_predict` runs on the scaled frame, not the raw one. §2 Point 2 calls unscaled clustering "the most common mistake in this project" — you did not make it.
- `random_state=42, n_init=10` on K-Means. Reproducible, and `n_init` set explicitly rather than left to the default.
- The PCA scatter has a title and a `hue` mapping, and your cluster summary is a `groupby().mean()` on the unscaled table — which is the right frame to profile from, since scaled means are not interpretable.

The method is not the problem. Every structural decision in that file is correct.

## 3. What must change

**The file at `submissions/a3-tue-sat/a3-g04/01-ml-project/g04_01-ml-project.ipynb` is not a notebook.** It is a Python script — 42 lines of plain source — saved with an `.ipynb` extension. It has no JSON structure, so Jupyter and Colab cannot open it and GitHub will not render it. Everything below follows from that.

1. **Rebuild it as an actual notebook.** Open Colab or Jupyter, paste your code into cells, run it, and save via **File → Download .ipynb**. Do not rename a `.py` file. Your existing code is fine — this is a container problem, not a code problem.
2. **No outputs at all.** §3 requires Restart & Run All to complete with the outputs saved in the committed file. Nothing in your delivery has ever been executed and saved.
3. **No markdown cells.** §2 requires the six points as labelled markdown sections; §3 fails a wall of unexplained code on Clarity. Six headings plus a couple of sentences each.
4. **Point 3 is missing entirely — this is the largest gap.** You set `n_clusters=3` with no elbow plot, no silhouette sweep and no written reasoning. §5 returns on *"k chosen with no elbow or silhouette evidence,"* and §6 ranks justified k second only to correct method. Sweep k=2..10, collect `kmeans.inertia_` and `silhouette_score`, plot both, and write 2–4 sentences on what the plots told you. This is the single biggest piece of work outstanding, and it is maybe thirty lines.
5. **Point 6 is missing.** You print the per-cluster RFM means, which is the *evidence* — but no cluster is named and no persona is described. Give each a business name derived from its own row (`cluster_means["Monetary"].idxmax()` gives you VIP without hardcoding), then 2–3 sentences each on who they are and what the business should do differently for them. §5 returns on personas left as "Cluster 0/1/2."
6. **Fix the dataset path.** `pd.read_csv('retail_transactions_segmentation.csv')` will not resolve from your folder, and §1 asks you not to copy the CSV in. Use `../../../../01-ml-project/retail_transactions_segmentation.csv`.
7. **Rename** `g04_01-ml-project.ipynb` to `a3-g04_01-ml-project.ipynb`. The cohort prefix is missing.
8. **Label the PCA axes.** You have a title and colour mapping; §2 Point 5 also wants axis labels. `plt.xlabel("PC1")` / `plt.ylabel("PC2")`.

A working reference for all of this is `submissions/a3-tue-sat/a3-g02/01-ml-project/a3-g02_01-ml-project.ipynb` — same cohort, same deadline, accepted this round. Read it before you start.

## 4. Notes carried forward

- `rfm_scaled_df` is built with the original column names, so `rfm[['Recency','Frequency','Monetary']]` and its scaled twin are easy to confuse further down. Suffix the scaled frame's columns, or keep it as a plain array.

## 5. Discussion slot

**S15 — Tue 15/09**, after the 13/09 deadline. Present the k evidence you are about to build: the two plots, and why you landed where you landed.

## 6. A note to the team

**Ramy, Saad, Haitham, Ahmed** — you delivered on the deadline after missing the first one. I asked you to tell me what got in the way or push what you had, and you pushed. I would rather have this conversation than the one we were heading for.

And I want you to be clear about where you actually stand, because a §3 list of eight items looks worse than your position is. Every method decision in those 42 lines is correct. You scaled before clustering — the criteria call that "the most common mistake in this project," and a third of the cohort made it. You added `+ 1 day` to your reference date so your most recent buyer would not sit at zero. You set `n_init` explicitly. You profiled the clusters on the *unscaled* table, which is the only frame where the numbers mean anything. That is four judgement calls in a row, all right, and none of them accidental.

What you sent is the skeleton of a good submission that stopped about 60% of the way in. Two things are genuinely missing — the evidence for k, and the personas — and one thing is a packaging accident: you saved a `.py` file with an `.ipynb` name, so nothing will even open it. That last one is not a knowledge gap, it is thirty seconds in the wrong menu.

Here is what I would do, in order, and it is one evening between four people: paste your code into a Colab notebook and run it. Add the k sweep and the two plots. Add six markdown headings. Name three clusters from their own rows and write two sentences each. Download as `.ipynb`. Push.

Open `a3-g02`'s notebook first — they were in your position on 04/09, delivered two days later, and were accepted this round with nothing outstanding. It is the clearest map of the distance you have left, and the distance is shorter than this review looks.

Sunday 13/09. Message me if anything stalls.

— Hozaifa
