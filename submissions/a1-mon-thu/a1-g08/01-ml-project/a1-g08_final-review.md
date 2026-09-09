# Final Review — a1-g08 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g08` — Mahmoud Attia, Mohamed Adel, Amr Essam, Youmna Elsayed, Mariam Hesham  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `e74ef49` (03/09/2026) — **unchanged since the 04/09 review**

This is the instructor's final review, re-issued after the 07/09 catch-up deadline. Nothing was pushed against it.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Sun 13/09/2026** — the fixes in §3 must be pushed before the final catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

**The 07/09 catch-up deadline passed with no delivery.** I checked every pull request (open, merged and closed), every branch on the remote including forks, and every commit touching your folder on any ref. Your branch `a1-g08_01-ml-project` still ends at `e74ef49`, and PR #10 was merged before the review was written. Nothing arrived.

**This is the second and last extension.** After 13/09 the outcome is recorded as it stands.

## 2. What worked

Unchanged from 04/09, and still true:

- You went past the brief with quartile R/F/M scoring layered on top of K-Means — and you used `rank(method="first")` to break Frequency ties in `pd.qcut`, which is a subtle and correct detail most people get wrong on their first attempt.
- Fourteen markdown cells; the structure is all there.

## 3. What must change

Both items are carried over from 04/09 unchanged.

1. **All 24 code cells are unexecuted and the notebook has zero outputs.** §5: *a notebook committed with its outputs stripped out*. This is the only substantive thing between you and an accept — the work underneath is among the most ambitious submitted, and none of it is currently visible. Restart & Run All, then commit the notebook **with** its outputs. `a1-g03` had exactly this problem on 04/09, fixed it in three days, and is accepted this round.
2. **Rename** `a1-g08_RFM_KMeans_full.ipynb` to `a1-g08_01-ml-project.ipynb`.

## 4. Notes carried forward

Alongside the required fixes above.

- Your folder still contains `SUBMISSION_GUIDE.md`, `SUBMISSION_CRITERIA.md`, `Customer_Segmentation_Project_Brief.docx`, `retail_transactions_segmentation.csv` and a `.jpg`. §1: only your notebook belongs there, and it asks specifically that you not copy the CSV in. Delete all five in the same push.

## 5. Discussion slot

**S14 — Mon 14/09**, short opening slot before the Project 2 block starts, if you deliver by 13/09.

## 6. A note to the team

**Mahmoud, Mohamed, Amr, Youmna, Mariam** — nothing reached me by Monday, and I want to be clear about what is at stake, because I do not think you know.

Your notebook contains the most ambitious extension anyone attempted in this project. Nobody asked for quartile R/F/M scoring on top of the clustering, and using `rank(method="first")` to break the Frequency ties in `qcut` is a detail that catches out people with years of pandas behind them. Somebody on this team read the documentation properly and thought it through.

None of it renders. Every cell is committed unrun, so a reader opening your notebook sees code and blank space. The best work in the batch is currently invisible, and the fix is **Restart & Run All, save, push** — one menu item, and the file is done. `a1-g03` was in exactly this position on 04/09 and is accepted this round. The gap between you is one afternoon, not one skill.

If something is stopping that — the notebook errors partway when you actually run it, Colab times out, the CSV path breaks, nobody has push access — send me the error and I will unblock it today. That is a fifteen-minute conversation, and I would much rather have it than record this as incomplete.

Sunday 13/09, and it is the last extension on Project 1. Please do not let this one go by.

— Hozaifa
