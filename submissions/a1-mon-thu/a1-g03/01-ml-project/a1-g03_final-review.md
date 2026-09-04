# Final Review — a1-g03 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g03` — Salma Barakat, Sama Abdo, Farida Ibrahim, Arwa Ismail  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g03_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- Your persona assignment is done the right way — `vip_cluster = cluster_means["Monetary"].idxmax()`, then the remainder inferred. The names are derived from the numbers, so they can never drift out of sync. Several approved groups hardcoded this and are more fragile than you are.
- Eleven markdown cells with clear step-by-step commentary. The narrative requirement is comfortably met.
- You fall back to a raw URL if the relative path is missing — a thoughtful touch.

## 3. What must change

1. **Every cell is unexecuted and all outputs are empty.** §5: *a notebook committed with its outputs stripped out*. As it stands I cannot verify a single one of the six points, even though the code underneath looks correct. Restart & Run All, then commit the notebook **with** its outputs.
2. Rename to `a1-g03_01-ml-project.ipynb`. The current name — `a1-g03_01-ml-project . ipynb.ipynb` — has spaces around the dot and a doubled suffix.

## 4. Notes carried forward

Alongside the required fixes above.

- At k=2 you only get "VIP" and "At-Risk". Once your outputs are visible, look at whether two segments are really actionable — k=3 may serve your persona step better. Not required, but worth ten minutes.

## 5. Discussion slot

**S13 — Thu 10/09.** This is the closest of the six to being done; it is a re-run, not a rewrite.
