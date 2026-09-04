# Final Review — a1-g02 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g02` — Nadeen Adel, Maram Ahmed, Rawan Mustafa, Nour Osama  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g02_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [ ] ✅ **Accepted** — graded and closed, no further action
- [x] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- k=2 is properly evidenced. You printed the silhouette peak (0.6789) and read the elbow alongside it, and the criteria explicitly accept a well-argued k=2 over an unexplained k=4. The choice is not the problem.
- The RFM table itself is correct — 300 customers, clean `groupby`, dates parsed properly.

## 3. What must change

1. **Both of your clusters are named "VIP / Champions"** and carry the same recommendation ("High total spending, high order frequency, and very recent purchases"). Cluster 1 is 260 customers at R 61.8 / F 8.7 / M 2,661 — that is your ordinary majority, not a VIP tier, and the recommendation is wrong for them. This is the one failure §5 names outright: *persona names that contradict the cluster's own RFM averages*.
2. Appending the cluster ID "to ensure 100% uniqueness across segments" makes the two names *look* different without making them *mean* different things. Delete that line and derive each name from its own row of the means table — `cluster_means["Monetary"].idxmax()` gives you the VIP cluster in one line, and it cannot drift.
3. **The entire project is one code cell** with a single markdown cell. §2 asks for each of the six points as its own labelled markdown section. Split it up — this is also what makes the persona bug hard to see.
4. Move the notebook to `submissions/a1-mon-thu/a1-g02/01-ml-project/a1-g02_01-ml-project.ipynb`. It is currently one folder too high and named `.ipynb.ipynb`.

## 4. Notes carried forward

Alongside the required fixes above.

- You load the CSV from a GitHub raw URL. It runs, which is the important part, but §1 asks for the repo-relative path so the notebook keeps working if the repo moves.

## 5. Discussion slot

**S13 — Thu 10/09.** Present after your fixes land. Be ready to say what the second cluster actually is, in one sentence.

## 6. A note to the team

**Nadeen, Maram, Rawan, Nour** — I want to be clear about something, because a "revise" can land harder than it should: your *analysis* is not the problem. You chose k=2, you backed it with a real silhouette score, and you read the elbow alongside it. That is a defensible, evidence-led decision, and plenty of groups who landed on a prettier number did less thinking than you did. Your RFM table is clean and correct.

What went wrong is the last mile — two clusters ended up with the same name, and the fix was a label rather than a rethink. That is a very common trap and an easy one to climb out of. Split the notebook into sections, name each cluster from its own row, and you will see the problem disappear in about twenty minutes. The foundation is already solid. Come to S13 and show us the corrected version.

— Hozaifa
