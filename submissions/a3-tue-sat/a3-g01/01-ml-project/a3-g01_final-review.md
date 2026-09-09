# Final Review — a3-g01 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a3-g01` — Ahmed Salama, Mona Mohamed, Shrouq Hatem  
**Cohort:** A3 (Tue/Sat)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `3637ed4` — *Revise justification for choosing k=4 in clustering* (PR #36, 05/09/2026)

The outcome is unchanged from 04/09. This round records that the k-justification note is now addressed, and raises one new item about how the revision is stored.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

Unchanged from 04/09:

- The most polished notebook submitted in either cohort — full data dictionary, five named data-quality checks, and a documented `log1p` → `StandardScaler` order, which is the correct sequence and one people routinely reverse.
- Three evaluation metrics swept rather than the two required, adding Davies–Bouldin on top of elbow and silhouette.
- All four personas verified against your unscaled table; VIP at 18.3% of customers and 67.7% of revenue is a genuinely useful headline.

New this round — **the k=4 justification is rewritten, and it is now honest.** You went further than I asked. The old text claimed the sharpest elbow was k=3→k=4; the new text says the reduction is *"most noticeable up to k=4"* with *"diminishing returns"* beyond, which is what your WCSS column actually shows. And you now write, in your own words:

> *"The Silhouette Score does not identify k=4 as the mathematically optimal solution; k=2 achieves a higher score."*

followed by:

> *"Overall, k=4 was not selected because it achieved the best score across all evaluation metrics. Rather, it was chosen because it offered a reasonable clustering structure while producing a more granular and actionable customer segmentation."*

That is the paragraph. You did not soften it, you did not bury it in the middle, and you closed the section on it. A reader now knows exactly what you traded and why — and the four personas that follow read as a decision rather than a result. The analysis was always sound; now the write-up matches it.

## 3. What must change

Nothing blocking. Accepted.

## 4. Notes carried forward

The k-justification note from 04/09 is **closed**. One new item, then the four that remain open.

1. **The revised markdown cell does not render — fix this before you present.** The new text went into the notebook's JSON as separate `source` strings with no `\n` at the end of each, so Jupyter concatenates them into one run-on line. The heading fuses to the first bullet:

   > `### Justification for Choosing $k=4$* **Elbow Point (WCSS):** The most noticeable reduction...`

   All three bullets and the closing paragraph then run together as a single block. The *content* is right — it is only the line terminators. Open the cell in Jupyter or Colab, retype it as normal markdown with real line breaks, and re-save from the editor rather than hand-editing the `.ipynb`. It matters more than usual here because this exact cell is what you are presenting at S14.

Still open from 04/09:

- Cell 20 — the RFM aggregation everything downstream depends on — has outputs but no execution count, so it was edited after its last run. Restart & Run All.
- Your README links `customer_segmentation.ipynb`, which does not exist; the file is `a3-g01-01-ml-project.ipynb.ipynb`. Fix the link, and the doubled suffix — it should be `a3-g01_01-ml-project.ipynb`, with an underscore.
- §1 says do not copy the CSV into your submission folder. Three data files are committed, including the derived `retail_transactions_cleaned.csv`.
- The slide JPG's filename is long enough to break `git checkout` on Windows without `core.longpaths` set. Shorten it — it will bite a classmate, not you.

## 5. Discussion slot

**S14 — Sat 12/09.** Moved from S13, which did not run. Short slot: the corrected k-justification only. Read the closing sentence out loud — *"k=4 was not selected because it achieved the best score across all evaluation metrics"* — and then say what you would tell a stakeholder who asked why not k=2. I am still pairing this with a3-g03, and now also with a3-g02, who hit a 0.001 silhouette gap between k=2 and k=3 and broke the tie the same way you did.

## 6. A note to the team

**Ahmed, Mona, Shrouq** — you did the harder version of the fix.

I asked for one honest paragraph. What you wrote was a four-part argument that names the elbow evidence, concedes the silhouette evidence outright, makes the business case separately, and then closes by stating plainly that k=4 did not win on the metrics. You could have edited two adjectives and satisfied the note. Instead you rewrote the section so that a reader who disagrees with you can see exactly where to disagree — which is the whole point, and considerably more uncomfortable to write.

That last sentence is the one I will be quoting to the room: *"k=4 was not selected because it achieved the best score across all evaluation metrics. Rather, it was chosen because it offered a reasonable clustering structure while producing a more granular and actionable customer segmentation."* Every group in both cohorts had to make a trade-off like that. You are one of three who wrote it down instead of implying it away.

One irritating thing, in §4: the cell does not render. The line breaks were lost when the JSON was edited by hand, so your best paragraph currently displays as a single run-on blob with the heading glued to the front of it. Retype it inside Jupyter — content unchanged, five minutes — and please do it before Saturday, because this is the cell you are presenting.

Accepted, note closed. The correction taught the room more than the original would have, exactly as I hoped.

— Hozaifa
