# Final Review — a1-g04 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g04` — Marwa Waheed, Aya Hussein, Rghdan Nezar, Hoda Elsayed, Mahmoud Shawky  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `a437512` (PR #37, 06/09/2026)

This is the instructor's final review, re-issued after your catch-up push. The 04/09 version returned this submission; that outcome is unchanged, with a new deadline below.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Sun 13/09/2026** — the fixes in §3 must be pushed before the final catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

**This is the second and last extension.** After 13/09 the outcome is recorded as it stands.

## 2. What worked

- The `CustomerSegmentation` class is still the most advanced engineering submitted in either cohort, and it survived the rewrite intact — state held on the instance, `random_state` threaded through the constructor, a k sweep of 2–10 wider than asked for. Nobody else attempted it.
- Your k=3 result is correct and your cluster profile is clean: VIP (R 7.4 / F 35.0 / M 29,684, 40 customers), Regular (R 42.6 / F 9.3 / M 2,877, 238), At-Risk / Dormant (R 257.6 / F 2.1 / M 326, 22). The names follow from the rows.
- Every cell is executed with outputs saved, and you now load the dataset from inside the cloned repo rather than a Drive path.

## 3. What must change

Both items below are carried over from 04/09 unchanged. Neither was addressed in this push.

1. **Still zero markdown cells.** All eighteen cells are code. §2 requires the six points as labelled **markdown** sections and §3 fails "a wall of unexplained code" on the Clarity check. Your `# Point 1 — RFM Analysis` banner comments inside the class are exactly the right content — they are just in the wrong cell type. Cut each one out, insert a markdown cell above the code, paste it in with a `##` heading. Twenty minutes, and no code changes at all. **This is the item that is holding the submission.**
2. **Still outside your group folder — and now there are two copies.** Your 06/09 push added `submissions/a1-mon-thu/a1-g04_01-ml-project/a1_g04_01_ml_project.ipynb` without removing the original at `submissions/a1-mon-thu/a1_g04_01_ml_project.ipynb`. Both are byte-identical (blob `55b2c11`), neither is in your group folder, and `submissions/a1-mon-thu/a1-g04/01-ml-project/` currently contains nothing but this review file. Delete **both** and put one copy at:

   ```
   submissions/a1-mon-thu/a1-g04/01-ml-project/a1-g04_01-ml-project.ipynb
   ```

   Hyphens, not underscores, and `a1-g04/01-ml-project/` as two folder levels. Then delete the `a1-g04_01-ml-project/` folder entirely, so only one copy of your notebook exists anywhere in the repo. A `git mv` moves a file; copying and pushing leaves the original behind, which is what happened here.

3. **Add the persona write-ups.** Point 6 asks for 2–3 sentences per persona: who they are and what the business should do *differently* for them. You have the names in `persona_names` and the means table beneath, which is the evidence — but the prose is missing entirely. Three short paragraphs in the markdown cells you are adding for item 1.

## 4. Notes carried forward

Alongside the required fixes above.

- Remove `Customer_Segmentation_Project_Walkthrough (1).docx` from the folder. §1: the notebook is the whole submission.
- Your execution counts now run to 111 — the saved state is deeper into re-runs than it was on 04/09, when I asked you to clean it. Restart & Run All once before you push, so the committed sequence starts at 1.
- Cell 1 saves the output `fatal: destination path 'arabian-ai-training' already exists and is not an empty directory.` It is not a Python error and nothing downstream breaks, but `!git clone` inside a submitted notebook only works on a fresh Colab runtime. Once the file is in the right folder, the relative path `../../../../01-ml-project/retail_transactions_segmentation.csv` reaches the dataset with no clone at all.

## 5. Discussion slot

**Mon 14/09**, short opening slot. Present the class design; it is worth the room hearing and none of the fixes above touch it.

## 6. A note to the team

**Marwa, Aya, Rghdan, Hoda, Mahmoud** — I need to be straight with you, because I do not think you are being served by me being gentle about this.

Everything I wrote on 04/09 still holds. Your `CustomerSegmentation` class is the most advanced code submitted in either cohort. Your k=3 clustering is correct. Your personas match their numbers. On the *analysis*, you are near the top of the class.

And the submission is being returned a second time for the same two things: no markdown cells, and the file is not in your group's folder. Neither is a knowledge gap. Neither takes an hour. You pushed a new version on the 6th, which means you were working on this — but the work went into the notebook's content instead of the two items I listed, and the content was never the problem.

So let me make the priority unambiguous, in order:

1. Delete both stray copies and put one at `submissions/a1-mon-thu/a1-g04/01-ml-project/a1-g04_01-ml-project.ipynb`.
2. Turn your `# Point N —` comments into markdown cells above the code they describe.
3. Write three short paragraphs, one per persona.

Do those three and you are accepted. Do not touch the class — it is not what is wrong. It would be a genuinely bad outcome for the strongest engineering in the cohort to be recorded as incomplete over formatting, and that is now the only thing on the table. Deadline Sunday 13/09, and it is the last one.

Bring the class design on Monday 14/09 regardless. The room should see it.

— Hozaifa
