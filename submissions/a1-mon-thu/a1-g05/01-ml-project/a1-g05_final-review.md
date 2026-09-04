# Final Review — a1-g05 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g05` — Hassan Mohamed, Omar Wael, Samah Maged, Luji Alhedodi, Sandy Kandil  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g05_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- **Your justification for k is the best in either cohort.** You state openly that silhouette favours k=2 (0.66) and k=3 (0.655), then argue the business case anyway: k=3 leaves one over-generalised 238-customer bucket, and k=4 splits it into 128 and 111 without much loss of separation. That is exactly what §6 means by *the reasoning matters more than the number*, and it is the model answer for this project.
- Every persona carries a specific action rather than a generic one.

## 4. Notes carried forward

Not blocking, but fix these before Project 2 — they cost marks later.

- **Cluster 3 is labelled "At-risk" but you describe it as "Solid, steady customers"** — R 19 days, F 13.7, M ~4,700. Your description is right and your label is wrong. Rename it "Loyal" or "Core". I am accepting this because the evidence and reasoning underneath are correct and the fix is one word, but read strictly it trips the §5 persona-mismatch line — do not rely on that leniency next project.
- One cell left unexecuted, and the filename has a trailing space: `a1-g05_01-ml-project .ipynb`.

## 5. Discussion slot

**S12 — Mon 07/09.** You presented at S11 and are approved. If you are willing, read your k-justification paragraph out — I want the other groups to hear how you framed the trade-off.

## 6. A note to the team

**Hassan, Omar, Samah, Luji, Sandy** — you wrote the best paragraph anyone submitted for this project. You had a result that did not flatter your choice, you said so out loud, and then you argued your case on the business merits anyway. That is intellectual honesty, and it is rarer and worth more than a high silhouette score. I am going to read your justification to the cohort, because it is the standard I want everyone aiming at.

Rename that one cluster from "At-risk" to "Loyal" — your own description already says what it really is — and this is close to exemplary. Genuinely well done.

— Hozaifa
