# Final Review — a1-g08 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 10/09/2026 *(follow-up — supersedes the 09/09/2026 review)*  
**Group:** `a1-g08` — Mahmoud Attia, Mohamed Adel, Amr Essam, Youmna Elsayed, Mariam Hesham  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `0860fb8` (PR #48, 10/09/2026)

This is the instructor's review of your 10/09 push, ahead of the 13/09 deadline set on 09/09. Both required fixes landed, and the notebook was rewritten rather than patched.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

- **Both blocking issues are fixed.** The notebook is renamed to `a1-g08_01-ml-project.ipynb`, and all 16 code cells are executed with their outputs committed — the RFM table, both k-selection plots (elbow + silhouette), the PCA scatter and every cluster/persona table now render.
- You rewrote the pipeline rather than just re-running the old one, and the new version is tighter: `assert`-backed sanity checks straight after building the RFM table (300 unique customers, no missing values), a documented `reference_date`, and a `Final Validation Checklist` markdown cell at the end that walks back through every requirement and ties it to a cell above.
- K chosen at 3 via elbow + silhouette together (silhouette peaks at k=2 but flattens by k=3 while inertia keeps dropping sharply — a defensible call, and you show both curves so it can be checked). Cluster profile is clean: VIP (R 8.4 / F 35.0 / M 29,683.6, 40 customers), Regular (R 43.6 / F 9.3 / M 2,876.9, 238), Dormant/At-Risk (R 258.6 / F 2.1 / M ~326, 22).
- Persona write-ups are proper prose, not just labels: each of the three markdown cells states the profile and a distinct business action (reactivation campaigns for Dormant, cross-sell/bundles for Regular, retention perks for VIP).

## 3. What must change

Nothing — accepted as delivered.

## 4. Notes carried forward

Not blocking, but clean this up before the next project:

- Your folder still contains `SUBMISSION_GUIDE.md`, `SUBMISSION_CRITERIA.md`, `Customer_Segmentation_Project_Brief.docx`, `retail_transactions_segmentation.csv` and a `.jpg` (`rfm_analysis_matrix_...slide01.jpg`) alongside the notebook. §1 of the submission criteria asks that only the notebook live in your group folder, and specifically asks that you not copy the CSV in. This was already noted on 09/09 and wasn't part of this push — delete all five next time you touch this folder.
- The quartile R/F/M scoring on top of K-Means (`pd.qcut` with `rank(method="first")` to break Frequency ties) that the 09/09 review praised is gone from this rewrite. Not a problem for acceptance — the K-Means segmentation on its own satisfies the brief — but if that extension still exists in your history somewhere, it was genuinely one of the better pieces of work in the cohort and worth keeping around for your own portfolio.

## 5. Discussion slot

**Mon 14/09.**

## 6. A note to the team

**Mahmoud, Mohamed, Amr, Youmna, Mariam** — this is accepted. The rewrite is clean, the checklist at the end is a good habit worth carrying into the next project (it is the kind of thing that makes a submission easy to grade and easy for you to double-check yourselves before you push), and the persona write-ups actually argue for specific business actions instead of just naming a cluster. Good work getting this in ahead of the deadline.

— Hozaifa
