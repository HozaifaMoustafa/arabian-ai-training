# Final Review — a3-g03 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a3-g03` — Shahd Waleed, Amina Abdelaziz, Rokaya Abdelgany, Sama Alaaeldin  
**Cohort:** A3 (Tue/Sat)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a3-g03_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- **This is the reference submission for Project 1**, and I intend to show it to the next cohort.
- You are the only group that states both choices §2 Point 1 asks for *and* explains them: reference date `2024-12-31`, "one day after the dataset's last transaction so Recency is always ≥ 1 instead of one customer sitting at exactly 0"; and Monetary as total, "because it reflects overall customer value, which is what the persona step is built around." That is precisely the standard.
- You are honest about k: you print that silhouette favours k=2, then select k=4 for actionability and say why. Compare a3-g01, who reached the same k and wrote it up as though the metrics agreed.
- `FINAL_K` defined once and reused, and the persona map derived from `cluster_means.index` so relabelling cannot break it.
- The CSV is found via a candidate-path search, so it runs from any working directory. Executes 1→14 in order.

## 4. Notes carried forward

Not blocking, but fix these before Project 2 — they cost marks later.

- Nothing outstanding. For your own awareness: two versions of your notebook existed in the repo — one reached `main` via PR #14, a later and better one via `staging`. The `staging` version is the one kept, which is the one with `FINAL_K`, the written k-justification and the derived persona map.

## 5. Discussion slot

**No further slot needed** — you presented at S10 and are closed out. If you are willing to sit in on S13 to compare notes with a3-g01 on the k write-up, it would be worth the room's time.
