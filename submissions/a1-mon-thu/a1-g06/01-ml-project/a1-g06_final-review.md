# Final Review — a1-g06 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g06` — Shahd Khaled, Mariam Mohamed, Omar Mahmoud, Abdelaziz, Fatma Ragab  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g06_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- Your persona-assignment logic is the best of any group: VIP from `Avg_Monetary.idxmax()`, Dormant from `Avg_Recency.idxmax()`, remainder inferred. It is immune to K-Means relabelling the clusters, which is a real failure mode that seven other groups are exposed to.
- Persona descriptions and recommended actions are properly tabulated.

## 3. What must change

1. **Your cluster profile, persona assignment and persona summary all saved as `<pandas.io.formats.style.Styler>` rather than tables.** Three of your strongest cells display nothing in the committed notebook, which means your Point 6 evidence is unverifiable. `.style` as a cell's last expression does not survive the save. Drop `.style`, or call `display()` on the plain frame, then re-run.
2. Your folder is `submissions/a1-g06_01-ml-project/` — outside `a1-mon-thu/` entirely. Move it to `submissions/a1-mon-thu/a1-g06/01-ml-project/`.
3. Rename `Copy_of_AI_ENG_Project(2)_G06.ipynb` to `a1-g06_01-ml-project.ipynb`.
4. Only 2 markdown cells across 21. Add the six section headings §2 asks for.

## 4. Notes carried forward

Alongside the required fixes above.

- Execution counts were cleared on export. Restart & Run All before you push.

## 5. Discussion slot

**S13 — Thu 10/09.** Your persona logic is what I want the room to see — it is the fix I am recommending to half the cohort.
