# Final Review — a1-g10 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g10` — Yasmin Khaled, Hader Mohsen, Radwa Alaa, Omar Mohamed, Al Hassan  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g10_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- k=2 is chosen against the actual silhouette maximum (0.6789) and — importantly — you *printed* the reasoning rather than leaving it implied.
- Your VIP persona is accurate and its recommended action is specific and sensible.

## 3. What must change

1. **Cluster 1 is 260 of your 300 customers, at R 61.8 / F 8.7 / M 2,661 — and you named it "Dormant / Lost" and described it as "churned or inactive."** Nearly nine purchases each, two months since the last one, is your mainstream customer base, not a lapsed one. §5 returns on *persona names that contradict the cluster's own RFM averages*. Either rename it ("Regular / Developing") or move to k=3 so a genuinely dormant tail actually separates out. I would try k=3 — your instinct that there is a dormant group is right, k=2 just cannot isolate it.
2. **The entire project is one code cell with no markdown at all.** §2 wants the six points as labelled markdown sections; §3 fails a wall of unexplained code on Clarity.
3. Rename `customer_segmentation.ipynb` to `a1-g10_01-ml-project.ipynb`, and remove the stray `README.txt`.

## 4. Notes carried forward

Alongside the required fixes above.

- Drop the "ALL SUBMISSION REQUIREMENTS & VALIDATION CHECKS PASSED!" banner. A notebook printing its own pass mark is not evidence, and in this case it was not accurate — which is exactly why it is worth removing.

## 5. Discussion slot

**S13 — Thu 10/09.** If you re-run at k=3, show the room both cluster profiles side by side and say which one you would take to a marketing team.

## 6. A note to the team

**Yasmin, Hader, Radwa, Omar, Al Hassan** — the instinct that got you into trouble is actually a good one, so let me name it clearly. You looked at your data and thought "there is a dormant group in here." You are right — there is. The problem is that k=2 cannot isolate it, so that label landed on 260 ordinary customers instead. Your reasoning was sound; the tool you gave it was too blunt.

You also did something several accepted groups did not: you *printed* your reasoning for k instead of leaving it implied. That is the right habit. Re-run at k=3, split the notebook into sections, and I think you will see the segment you were looking for appear on its own. Bring both profiles to S13 — that is a genuinely interesting thing to show.

— Hozaifa
