# Final Review — a1-g06 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 10/09/2026 *(follow-up — supersedes the 09/09/2026 review)*  
**Group:** `a1-g06` — Shahd Khaled, Mariam Mohamed, Omar Mahmoud, Abdelaziz, Fatma Ragab  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `902d24a` (PR #46, 10/09/2026)

This is the instructor's review of your 10/09 push, ahead of the 13/09 deadline set on 09/09. Real progress — two of the four required fixes landed — but the outcome does not change yet, because the other two are still outstanding.

A second copy of this same push also arrived as PR #47 on the `a1-g06_01-ml-project` branch. That branch was forked from a commit before the round-2 review batch merged, so its notebook is byte-for-byte identical to the one reviewed here, but merging the branch itself would have reverted roughly fifty unrelated files across the repo (every other group's review, the announcement PDFs, the discussion schedules). I closed PR #47 as superseded rather than merge it — nothing in it was lost, it's the same file already reviewed below.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Sun 13/09/2026** — the fixes in §3 must be pushed before the final catch-up deadline (unchanged — this is still the last extension)
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

- **Item 1 from 09/09 is fixed.** `cluster_profile`, the persona-assignment table and `persona_summary` all now end their cell in `display(<plain DataFrame>)` instead of `.style` — every one of them renders in the committed notebook. Numbers check out: VIP/Champions (Avg Monetary 29,683.61, 40 customers), Active/Regular (238), Dormant/At-Risk (Avg Recency 258.59, 22) — same persona logic praised on 04/09 and 09/09, now actually visible.
- **Item 4 is fixed, well past the minimum.** You went from 2 markdown cells to 17, and all six required sections (§2 of the criteria) are present as labelled headings: RFM Feature Table, Features Scaled, Choice of K, K-Means Fitting, Personas & Business Interpretation, Visualizations.
- The carried-forward note about execution counts is also resolved — all 19 code cells are executed and every substantive cell (all but the import cell and one trailing empty cell) carries output.
- Your persona-assignment logic (`Avg_Monetary.idxmax()` for VIP, `Avg_Recency.idxmax()` for Dormant, the remainder inferred) remains the best in the cohort at surviving K-Means relabelling its own clusters, and the persona descriptions are still properly tabulated.

## 3. What must change

Two items carried over from 09/09 — unchanged, and the only things standing between this and an accept.

1. **Move the folder.** Your notebook is at `submissions/a1-mon-thu/a1-g06-01-ml-project/a1-g06_01-ml-project.ipynb.ipynb` — a folder named with a hyphen (`a1-g06-01-ml-project`) instead of the required two nested folders, and a filename with the `.ipynb` extension doubled. Meanwhile this review lives at `submissions/a1-mon-thu/a1-g06/01-ml-project/`, which is why they still aren't next to each other. `git mv` the notebook into the same folder as this file.
2. **Rename** it to `a1-g06_01-ml-project.ipynb` (single extension) once it's in the right place.

Both are pure file operations — no notebook content changes required.

## 4. Notes carried forward

None outstanding beyond §3.

## 5. Discussion slot

**Mon 14/09**, short opening slot, if you deliver by 13/09.

## 6. A note to the team

**Shahd, Mariam, Omar, Abdelaziz, Fatma** — this is real, visible progress. The `.style` fix and the markdown sections are exactly what I asked for, and the persona logic still stands out — I'm still pointing other groups at it.

What's left is not analysis, it's two `git mv`-shaped operations: move the notebook file into `submissions/a1-mon-thu/a1-g06/01-ml-project/`, next to this review, and drop the doubled `.ipynb.ipynb` down to one. Nothing about the work itself needs to change. If git is the obstacle rather than time, `GIT_PULL_PUSH_EXAMPLES.md` at the repo root walks through exactly this operation, and I'll walk any of you through it directly if that's faster.

Sunday 13/09 is still the last extension on Project 1. You are one small push away from an accept — please get it in.

— Hozaifa
