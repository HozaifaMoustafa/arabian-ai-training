# Final Review — a1-g06 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g06` — Shahd Khaled, Mariam Mohamed, Omar Mahmoud, Abdelaziz, Fatma Ragab  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `e6c9697` (26/08/2026) — **unchanged since the 04/09 review**

This is the instructor's final review, re-issued after the 07/09 catch-up deadline. Nothing was pushed against it.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Sun 13/09/2026** — the fixes in §3 must be pushed before the final catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

**The 07/09 catch-up deadline passed with no delivery.** I checked every pull request (open, merged and closed), every branch on the remote including forks, and every commit touching your folder on any ref. The last change to `submissions/a1-g06_01-ml-project/` is `e6c9697` from 26/08 — before the QA cutoff. Nothing arrived.

**This is the second and last extension.** After 13/09 the outcome is recorded as it stands.

## 2. What worked

Unchanged from 04/09, and still true:

- Your persona-assignment logic is the best of any group: VIP from `Avg_Monetary.idxmax()`, Dormant from `Avg_Recency.idxmax()`, the remainder inferred. It is immune to K-Means relabelling its clusters — a real failure mode that bit two other groups this round.
- Persona descriptions and recommended actions are properly tabulated.

## 3. What must change

All four items are carried over from 04/09 unchanged.

1. **Your cluster profile, persona assignment and persona summary all save as `<pandas.io.formats.style.Styler>` instead of tables.** Three of your strongest cells display nothing in the committed notebook, so your Point 6 evidence cannot be checked. A `.style` object as a cell's last expression does not survive the save. Drop `.style`, or call `display()` on the plain frame, then re-run. *(a3-g02 hit the same thing this round on one cell — it is not just you.)*
2. **Move the folder.** It is at `submissions/a1-g06_01-ml-project/` — outside `a1-mon-thu/` entirely, which is why your review file and your notebook are in different places. It belongs at `submissions/a1-mon-thu/a1-g06/01-ml-project/`.
3. **Rename** `Copy_of_AI_ENG_Project(2)_G06.ipynb` to `a1-g06_01-ml-project.ipynb`.
4. **Only 2 markdown cells across 21.** Add the six labelled section headings §2 asks for.

## 4. Notes carried forward

Alongside the required fixes above.

- Execution counts were cleared on export. Restart & Run All before you push, so the committed notebook carries its outputs.

## 5. Discussion slot

**S14 — Mon 14/09**, short opening slot before the Project 2 block starts, if you deliver by 13/09.

## 6. A note to the team

**Shahd, Mariam, Omar, Abdelaziz, Fatma** — nothing reached me by Monday, and I would rather ask than assume.

What I wrote on 04/09 was not padding. Your persona-assignment logic is the best in the cohort, and I have been pointing other groups at your approach all week — two groups had their persona names break this round for exactly the reason yours cannot. So this is not a review about work that was not good enough. It is a review about work sitting one `.style` call away from finished, that did not move.

I do not know why, and that is the part I want to fix. If the blocker is technical, it is small: dropping `.style` is a one-line edit per cell, and moving a folder is a `git mv`. If the blocker is git itself, `GIT_PULL_PUSH_EXAMPLES.md` at the repo root covers it and I will walk any of you through it. If it is something inside the group — someone left, one person has the only copy, coursework collided — tell me today and we will work around it. All of those are ordinary, and all of them are fixable.

What I cannot fix is silence. You have until Sunday 13/09, and it is the last extension on Project 1. Please message me before then, even if it is only to say what is in the way.

— Hozaifa
