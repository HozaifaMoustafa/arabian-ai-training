# Final Review — a1-g10 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g10` — Yasmin Khaled, Hader Mohsen, Radwa Alaa, Omar Mohamed, Al Hassan  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `a2ca04c` (PR #35, merged 04/09/2026)

This is the instructor's final review, re-issued after your catch-up push. The 04/09 version returned this submission; that outcome is now replaced by the one below.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

**All three required fixes landed, plus both carried-forward notes.** This is the most complete turnaround in the cohort.

1. **You went to k=3, and the segment you were looking for appeared.** Your profile is now VIP / Champions (40 customers, R 8.4 / F 35.0 / M 29,684), Recent / Occasional Buyers (238, R 43.6 / F 9.3 / M 2,877), Dormant / Lost (22, R 258.6 / F 2.1 / M 326). Twenty-two customers who have not bought in eight and a half months — *that* is a dormant group, and it is the one your instinct told you was in the data on 04/09. At k=2 the label landed on 260 ordinary customers; at k=3 it lands on the 22 it belongs to. The instinct was right the whole time.
2. Six labelled markdown sections, one per point. The wall of code is gone.
3. Renamed to `a1-g10_01-ml-project.ipynb`, stray `README.txt` removed.

Two more things you were not asked for but did anyway:

- **Your persona assignment is now rank-based across all three dimensions** — VIP by the combined rank of low recency, high frequency and high monetary; Dormant by the inverse; the remainder inferred. That is stronger than `Monetary.idxmax()` alone, because it will not misfire on a cluster that spends heavily but has gone quiet. Of the twenty submissions this is the most robust naming logic anyone wrote.
- The "ALL SUBMISSION REQUIREMENTS & VALIDATION CHECKS PASSED!" banner is gone, and you load the dataset from `../../../../01-ml-project/retail_transactions_segmentation.csv` — the shared file, by relative path, exactly as §1 asks. Only two groups in twenty got that right.

## 3. What must change

Nothing. Accepted.

## 4. Notes carried forward

None outstanding. Both 04/09 notes were addressed.

## 5. Discussion slot

**Thu 10/09.** Show the room the k=2 profile beside the k=3 profile and say, in one sentence, what changed about the business recommendation. You are the clearest example in either cohort of *why* the choice of k is a business decision and not just a plot-reading exercise — that is a five-minute talk that will land.

## 6. A note to the team

**Yasmin, Hader, Radwa, Omar, Al Hassan** — I told you on 04/09 that your instinct was sound and the tool was too blunt. You proved the first half yourselves.

Going to k=3 and finding twenty-two genuinely dormant customers sitting exactly where you thought they were is the most satisfying outcome of this whole review round. You did not just apply a fix I handed you; you had a hypothesis about your data, the first attempt could not test it, and the second one did. That is the actual loop of the job.

And you went further than the notes asked. Nobody told you to rewrite the persona assignment to rank across all three RFM dimensions — you did it because `idxmax()` on Monetary alone would misname a high-spending cluster that has gone quiet, and you saw that before it bit you. That is now the most robust naming logic in either cohort, and I will be pointing other groups at it.

From returned to the strongest turnaround in the class in five days. Accepted, with nothing carried forward. Bring both k profiles to Thursday.

— Hozaifa
