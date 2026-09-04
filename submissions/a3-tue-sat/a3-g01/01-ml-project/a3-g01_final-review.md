# Final Review — a3-g01 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a3-g01` — Ahmed Salama, Mona Mohamed, Shrouq Hatem  
**Cohort:** A3 (Tue/Sat)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a3-g01_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- The most polished notebook submitted in either cohort — full data dictionary, five named data-quality checks, and a documented `log1p` → `StandardScaler` order, which is the correct sequence and one people routinely reverse.
- You swept three metrics rather than the two required, adding Davies–Bouldin on top of elbow and silhouette.
- All four personas verified against your unscaled table; VIP at 18.3% of customers and 67.7% of revenue is a genuinely useful headline.

## 4. Notes carried forward

Not blocking, but fix these before Project 2 — they cost marks later.

- **Your k=4 justification misreports your own numbers, and this is the one thing I want you to fix.** You write that the sharpest elbow is k=3→k=4, but your WCSS drops are 98.3 (k2→3), 57.5 (k3→4) and 47.3 (k4→5) — the sharpest is k2→k3. You call 0.4333 "a high silhouette score" when it is the *lowest* value in your entire sweep, and you mark k=4 optimal on the Davies–Bouldin plot where 0.9153 is the *worst*. k=4 is a perfectly defensible business choice; the problem is the write-up claims the metrics support it when all three point away. Say it honestly instead: *we accept the weakest separation scores in this range because k=2 collapses two distinct high-value groups*. Compare with a3-g03, who hit the identical trade-off and wrote it up straight.
- Cell 20 — the RFM aggregation everything downstream depends on — has outputs but no execution count, so it was edited after its last run. Restart & Run All.
- Your README links `customer_segmentation.ipynb`, which does not exist; the file is `a3-g01-01-ml-project.ipynb.ipynb`. Fix the link and the doubled suffix.
- §1 says do not copy the CSV into your submission folder. Three data files were committed, including the derived `retail_transactions_cleaned.csv`.
- The slide JPG's filename is long enough to break `git checkout` on Windows without `core.longpaths` set. Shorten it — it will bite a classmate, not you.

## 5. Discussion slot

**S13 — Tue 08/09.** Short slot: present the corrected k-justification only. I am pairing it with a3-g03 deliberately — the two of you reached the same decision and wrote it up differently, and that contrast is the most useful thing in this project.

## 6. A note to the team

**Ahmed, Mona, Shrouq** — this is the most polished notebook submitted in either cohort. The data dictionary, the five named quality checks, `log1p` before scaling in the correct order, a third evaluation metric nobody asked for — three people produced more finished work than most teams of five. That is not in question.

I have been direct in §4 about the k write-up, and I want to explain why. You reached a defensible answer and then described the evidence as agreeing with you when it did not. Reviewers notice that faster than a wrong number, and it costs more, because it puts everything *else* you wrote under suspicion. The fix is one honest paragraph — and the fact that your analysis was sound the whole time is what makes it worth fixing rather than worth worrying about. Present the corrected version at S13; that correction will teach the room more than the original would have.

— Hozaifa
