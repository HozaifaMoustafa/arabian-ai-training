# Final Review — a1-g13 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g13` — Mohamed Ali, Karim Ahmed, Shady, Ahmed Adel, Omar Rafaat  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `172504a` (PR #39, 07/09/2026)

This is the instructor's final review, re-issued after your catch-up delivery. The 04/09 version recorded this project as not submitted; that outcome is now replaced by the one below.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

You delivered on the catch-up deadline, and what arrived is one of the two or three best-argued notebooks in either cohort.

- **Your k justification is the most honest in the class.** You state plainly that silhouette is *highest* at k=2 (0.679) and effectively tied at k=3 (0.678), that k=4 scores lower at 0.570, and that you chose k=4 anyway — then you say why: the elbow flattens after k=4, 0.57 is still solid structure, and k=2–3 gives you no segment for recently-active moderate spenders. You end with *"The deciding factor... is business interpretability, not the single highest silhouette digit."* That sentence is the whole lesson of Point 3. Two other groups reached k=4; you are the only one who did not quietly imply the metrics agreed with you.
- **You tested the claim rather than asserting it.** You printed the full `results` table across k=2..10, then drew the vertical marker at k=4 on both plots, then profiled the four clusters and checked they were actually distinct before committing. The reasoning is auditable end to end.
- Your four personas match their rows exactly, and the actions are differentiated by *value*, not just by segment: VIP gets dedicated outreach, Dormant explicitly gets **the least budget per customer** because their spend was low even when active. Deciding where *not* to spend is the part most groups skip.
- The sanity checks are real ones — 300 unique customers in, 300 rows out; recency 1 to 337 days; the note that Frequency and Monetary both have long right tails "which is exactly the kind of structure clustering should pick up on." You are checking your work as you go, not at the end.
- Twelve markdown cells, all thirteen code cells executed with outputs saved, PCA reporting 98.7% variance captured with centroids overlaid on the scatter.

## 3. What must change

Nothing blocking. Accepted.

## 4. Notes carried forward

Not blocking, but all three before Project 2 opens.

1. **`pd.read_csv('retail_transactions_segmentation.csv')` will not resolve from your folder.** There is no CSV at `submissions/a1-mon-thu/a1-g13/01-ml-project/`, and §1 asks you not to put one there. It ran for you because the file sat beside the notebook locally, but a mentor cloning the repo gets `FileNotFoundError` on cell 1. Use the relative path to the shared copy: `../../../../01-ml-project/retail_transactions_segmentation.csv`. Your saved outputs are what saved this from being a §3 "runs top to bottom" failure — do not rely on that twice.
2. **Delete `a1-g13_01-ml-project - Copy.ipynb`.** Both PRs carry a byte-identical duplicate of your notebook. §1 asks for one notebook in the folder.
3. **Your group-size labels are swapped.** Loyal / Regular is 128 customers (43%) and New / Occasional is 111 (37%), but you call New/Occasional "the largest group" and Loyal "the second-largest." The numbers in the same paragraph contradict the words. Small, but this is a persona write-up a business would read.

**Housekeeping on my side:** you have three open pull requests for the same work — #34, #38 and #39. I am taking #39 and closing the other two. Next project, one branch and one PR per group.

## 5. Discussion slot

**S13 — Thu 10/09.** Present the k justification specifically — the k=2 vs k=3 vs k=4 argument and why you overrode the silhouette peak. Five minutes on that, and skip the rest. Three groups this round wrote k reasoning that described the evidence as agreeing with them when it did not; yours is the version I want them to hear.

## 6. A note to the team

**Mohamed, Karim, Shady, Ahmed, Omar** — on 04/09 I wrote that I had nothing from you and would like to be able to say something next time. You gave me a lot to say.

Here is the part I did not expect. Every group in this project had to choose a k, and almost all of them wrote the justification the same way: pick a number, then describe the evidence as though it endorsed the pick. You did the opposite. You wrote down that silhouette preferred k=2, that k=3 was tied with it, that your choice of k=4 scored *lower* than both — and then you argued for it anyway, on grounds you could defend. "The deciding factor is business interpretability, not the single highest silhouette digit."

That is a harder thing to write than a correct answer. It means being comfortable saying the numbers do not fully agree with me and here is why I am choosing anyway — which is precisely what you will be doing in front of stakeholders for the rest of your careers. A group that missed the first deadline entirely produced the most intellectually honest section in twenty submissions.

Three small things in §4 — a data path, a duplicate file, two swapped words. None of them touch the thinking. Fix them before Project 2 and bring the k argument to S13; the room needs to hear it from you rather than from me.

Welcome back.

— Hozaifa
