# Final Review — a1-g04 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g04` — Marwa Waheed, Aya Hussein, Rghdan Nezar, Hoda Elsayed, Mahmoud Shawky  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g04_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- The `CustomerSegmentation` class is the most advanced engineering submitted in either cohort. Encapsulating the whole pipeline and threading `random_state` through the constructor is how this would be written in production. Nobody else attempted it.
- Your personas are correct at k=3 — VIP (7.4 / 35.0 / 29,684), Regular (42.6 / 9.3 / 2,877), At-Risk (257.6 / 2.1 / 326).
- You swept k=2–10, wider than asked for.

## 3. What must change

1. **Zero markdown cells.** Your `# Point 1 —` comments inside the class are good practice, but §2 asks for six labelled *markdown* sections and §3 fails "a wall of unexplained code" on Clarity. Lift those comments out into markdown headings — the content already exists, it is in the wrong cell type.
2. The file sits at `submissions/a1-mon-thu/a1_g04_01_ml_project.ipynb` — outside any group folder, and underscored where the spec is hyphenated. Move it to `submissions/a1-mon-thu/a1-g04/01-ml-project/a1-g04_01-ml-project.ipynb`. §5 returns on wrong folder or filename.

## 4. Notes carried forward

Alongside the required fixes above.

- Your execution counts run to 109, so the saved state is many re-runs deep. Restart & Run All once before you push so the committed sequence is clean.

## 5. Discussion slot

**S13 — Thu 10/09.** Present the class design — it is genuinely worth the room hearing, and the fixes above do not touch it.

## 6. A note to the team

**Marwa, Aya, Rghdan, Hoda, Mahmoud** — you wrote the most advanced code submitted in either cohort. A proper `CustomerSegmentation` class, state held sensibly, `random_state` threaded through the constructor: this is how the pipeline would actually be written on a team, and nobody else went near it. Whoever pushed for that structure, keep pushing for it.

The irony is that engineering that good got returned over markdown cells. Your explanations already exist — they are sitting in `#` comments inside the class. Move them up into markdown headings and you are finished. Do not let a formatting rule make you think the ambition was misplaced; it wasn't. Please present the class design at S13, the room should see it.

— Hozaifa
