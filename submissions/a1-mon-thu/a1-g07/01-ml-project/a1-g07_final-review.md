# Final Review — a1-g07 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g07` — Sara Mohamed, Rewan Ibrahim, Menna Hussien, Malak Yasser, Omar Assem  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g07_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- **The cleanest submission in A1.** Thirteen markdown cells against ten code cells, executed in order, outputs saved, nothing off-spec. There is nothing for me to return.
- Personas correct at k=3 and stated plainly: VIP (8.4 / 35.0 / 29,684), Regular (43.6 / 9.3 / 2,877), At-Risk (258.6 / 2.1 / 326).
- You guarded the data path with `os.path.exists` before falling back, so the notebook runs from more than one working directory. Small thing, and exactly the kind of care that makes a notebook someone else can actually run.
- The narrative-to-code balance means a reader can follow your reasoning without executing anything.

## 5. Discussion slot

**S12 — Mon 07/09.** You presented at S11 and are approved. One thing worth raising if you speak again: your 43.6-day "Regular" group is 79% of customers and the biggest revenue lever in the dataset — a sentence on what would move them toward VIP would sharpen it.
