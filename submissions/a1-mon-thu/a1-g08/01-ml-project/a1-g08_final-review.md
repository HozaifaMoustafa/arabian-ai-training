# Final Review — a1-g08 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g08` — Mahmoud Attia, Mohamed Adel, Amr Essam, Youmna Elsayed, Mariam Hesham  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g08_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- You went past the brief with quartile R/F/M scoring layered on top of K-Means — and you used `rank(method="first")` to break Frequency ties in `pd.qcut`, which is a subtle and correct detail most people get wrong on their first attempt.
- Fourteen markdown cells; the structure is all there.

## 3. What must change

1. **All 24 code cells are unexecuted and the notebook has zero outputs.** §5: *a notebook committed with its outputs stripped out*. This is the only thing standing between you and an accept — the work underneath is among the most ambitious submitted. Restart & Run All and re-commit.
2. Rename `a1-g08_RFM_KMeans_full.ipynb` to `a1-g08_01-ml-project.ipynb`.

## 4. Notes carried forward

Alongside the required fixes above.

- `SUBMISSION_GUIDE.md` was copied into your group folder on the first attempt. It has since been removed on `staging` — please do not re-add it. Only your notebook belongs in that folder.

## 5. Discussion slot

**S13 — Thu 10/09.** Present the quartile scoring; it is the most interesting extension anyone attempted.
