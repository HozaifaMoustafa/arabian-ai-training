# Final Review — a1-g03 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g03` — Salma Barakat, Sama Abdo, Farida Ibrahim, Arwa Ismail  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `e6ecbb1` (PR #42, 07/09/2026)

This is the instructor's final review, re-issued after your catch-up push. The 04/09 version returned this submission; that outcome is now replaced by the one below.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

- **The blocking issue is fixed.** All nine code cells are executed and the outputs are committed. The 300-row RFM table, both k-selection plots, the PCA scatter and the cluster-means table all render now. Everything I said looked correct underneath on 04/09 is now verifiable, and it checks out.
- k=2 is properly argued in markdown: *"The silhouette score is highest at k = 2. The elbow plot also shows that the biggest improvement happens early..."* That is Point 3 done the way the criteria ask — the plots and the reasoning in the same place.
- The `idxmax()` persona derivation survived the re-run intact, and you extended it: `at_risk_cluster` is now computed as the remaining index rather than typed. Your names still cannot drift from your numbers.
- Eleven markdown cells, six labelled point sections, Arabic commentary that a beginner could actually learn RFM from.

## 3. What must change

Nothing blocking. Accepted.

## 4. Notes carried forward

Not blocking, but both must be done before Project 2 opens.

- **The filename is still `a1-g03_01-ml-project.ipynb.ipynb`.** You fixed the spaces around the dot, so it is much better than it was — but the suffix is still doubled. It should be `a1-g03_01-ml-project.ipynb`. I am not holding the submission on this: I accepted `a1-g15` on 04/09 with a worse filename, and applying the rule to you and not to them would be arbitrary. So the rule for Project 1 is the one I actually used — a filename alone does not block. From Project 2 it does.
- **"At-Risk" is the wrong name for 260 of your 300 customers.** Their averages are R 60.8 / F 8.7 / M 2,661: two months since the last purchase and nearly nine purchases each. That is your mainstream customer base. Your write-up is careful — you describe them as "the weaker RFM profile," which is true *relative to VIP* — but the label a marketing team reads is "At-Risk," and they would spend win-back budget on 87% of the book. This is the same trap `a1-g02` and `a1-g10` fell into; both moved to k=3 or renamed the cluster. At k=2 you cannot separate a genuinely dormant tail, so either name it "Standard / Regular" or go to k=3, where the dormant group (~20 customers at R ≈ 260) actually appears on its own.

## 5. Discussion slot

**S12 — Mon 07/09. Presented — closed out.** You took the slot early, ahead of the S13 re-present round. No further slot needed.

## 6. A note to the team

**Salma, Sama, Farida, Arwa** — you turned it around in three days, and you did it before your session rather than after it. That is worth naming on its own.

What I wrote on 04/09 still stands: deriving the VIP cluster with `idxmax()` instead of hardcoding it is better engineering than several groups I accepted outright, and you extended that same idea to the second cluster this round rather than leaving it half-done. The only thing between you and an accept was a habit — committing the file before running it — and you changed the habit in one afternoon, exactly as I said you would.

One thing to sit with for Project 2, in §4: "At-Risk" on 260 of 300 customers. Your *analysis* is right; the word is doing something your table does not support. Getting the number right and the name wrong is the most expensive mistake in this whole project, because it is the part a business actually acts on. You are close enough to it now that it is worth the extra ten minutes next time.

Accepted. Good work.

— Hozaifa
