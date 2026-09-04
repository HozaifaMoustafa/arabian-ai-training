# Final Review — a1-g09 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g09` — Shams Hassan, Rawan Hany, Aml Elsayed, Rozalenda  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g09_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- Strong across all six points, with the persona step done the robust way — you build `persona_map` from the cluster means instead of hardcoding IDs, so relabelling cannot break it.
- All four names check out against your own table: Occasional (70.6 / 4.2 / 752), VIP (7.4 / 35.0 / 29,684), At-Risk (262.4 / 2.1 / 320), Loyal Active (19.2 / 13.7 / 4,700).
- Twenty-six saved outputs across 25 code cells, each persona given its own markdown section. The notebook reads as a finished document rather than a working file.

## 4. Notes carried forward

Not blocking, but fix these before Project 2 — they cost marks later.

- Two cells left unexecuted — re-run so the sequence is unbroken.
- `../../../../01-ml-project/...` works but is brittle; four levels of `..` breaks the moment the file moves. A small `Path` candidate search is sturdier — a3-g03 has a clean example.

## 5. Discussion slot

**S12 — Mon 07/09.** This is your scheduled slot and you are ready. Be prepared to explain why you built the persona map from the table instead of typing the names in.
