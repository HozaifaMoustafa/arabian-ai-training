# Final Review — a1-g01 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 04/09/2026  
**Group:** `a1-g01` — Omnia Hamed, Mona Amasha, Rawan Ali, Amal Mohamed  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `dad096e`

This is the instructor's final review. Your mentor's `a1-g01_qa-review.md` was the gate check against `SUBMISSION_CRITERIA.md`; this file is the record of the work itself and is where any remaining action sits. Questions on it come to me, not to your mentor.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise by Mon 07/09/2026** — the fixes in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo; deliver by Mon 07/09/2026 or Project 1 is recorded as missed

## 2. What worked

- All six points present, labelled, and executed in order (1→10) with outputs saved.
- Your persona map is correct on all four clusters, and I checked each one against your own table: VIP (R 8.4 / F 35.0 / M 29,684), Loyal (20.7 / 14.0 / 4,849), Occasional (68.8 / 4.3 / 765), Lost (263.4 / 2.1 / 320). Nothing is mislabelled.
- You inverse-transformed the centroids back to real units with `scaler.inverse_transform` and `np.expm1`. Almost nobody did this, and it is what makes the cluster centres readable as money rather than z-scores.
- You were the only group to file a recap, unprompted.

## 4. Notes carried forward

Not blocking, but fix these before Project 2 — they cost marks later.

- Your final persona table ends on `.style.background_gradient(...)`, so what got committed is `<pandas.io.formats.style.Styler>` instead of the table. The prettiest cell in your notebook shows nothing. Drop `.style` or wrap it in `display()` — worth knowing before it costs you on a graded point.
- You label Monetary as EGP; the dataset carries no currency. State the assumption rather than implying it.

## 5. Discussion slot

**S12 — Mon 07/09.** You already presented at S10 and you are approved, so no second slot is required. Come anyway if you want to speak to the centroid inverse-transform; it is worth two minutes of everyone's time.

## 6. A note to the team

**Omnia, Mona, Rawan, Amal** — this was a genuinely careful piece of work, and the care shows in a place most people never reach. Transforming the centroids back into real money with `inverse_transform` and `expm1` is not in the brief; you did it because you wanted the numbers to *mean* something to a reader, and that instinct is exactly what separates an analyst from someone who runs models. You were also the only group in fifteen who wrote a recap when nobody made you.

Fix the `.style` line so your final table actually shows, and this is a submission you could put in front of a client. Keep that standard.

— Hozaifa
