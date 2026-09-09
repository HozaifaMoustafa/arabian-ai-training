# Final Review — a3-g02 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a3-g02` — Ahmed Hesham, Mohamed Bashar, Kareem Amr, Omar Abdul Aziz  
**Cohort:** A3 (Tue/Sat)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `a2f17f0` — *a3-g02: submit 01-ml-project* (05/09/2026)

This is the instructor's final review, re-issued after your catch-up delivery. The 04/09 version recorded this project as not submitted; that outcome is now replaced by the one below.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

You delivered two days after the review and well inside the deadline, and what arrived is a complete, correct submission. Taking the six points in order:

- **Point 1.** 3,663 transactions to a 300-row customer table, reference date stated in the output (`max(transaction_date) + 1 day`), Monetary as total spend. Both choices §4 asks you to declare are declared.
- **Point 2.** `StandardScaler` on all three columns, clustering on the scaled values — and a dedicated *"Why Scaling is Essential"* subsection rather than the one-line hand-wave the criteria would have accepted.
- **Point 3.** k swept 2–10, both curves plotted side by side with your chosen k marked, and a written justification that quotes its own numbers: inertia 394.2 at k=2 falling to 183.0 at k=3 then flattening, silhouette 0.678 at k=3 against 0.679 at k=2 and 0.570 at k=4. You then say why the near-tie with k=2 resolves toward three: a third segment that is genuinely distinct and actionable. That is Point 3 done properly.
- **Point 4.** `KMeans(n_clusters=3, random_state=42, n_init=10)`, labels attached back onto the RFM table.
- **Point 5.** PCA to two components, scatter coloured by cluster, titled and labelled.
- **Point 6.** The means table renamed by persona so the evidence and the names are in a single frame — VIP / Champions (40 customers, R 8.4 / F 35.0 / M 29,684), Core / Regular (238, R 43.6 / F 9.3 / M 2,877), Dormant / At-risk (22, R 258.6 / F 2.1 / M 326). Each persona then gets its own subsection with counts, share of base, and a differentiated action.

Correct filename, correct folder, correct relative path to the shared CSV with a fallback if it is missing. Eight markdown cells, all nine code cells executed with outputs saved.

**One thing worth singling out:** naming the majority cluster **"Core / Regular Customers"** rather than reaching for a dramatic label. 238 customers at R 43.6 with nine purchases each are the ordinary backbone of the business. Four groups across the two cohorts put "At-Risk," "Dormant" or "VIP" on a cluster of exactly this shape, and every one of them was returned for it. You got the least glamorous naming decision in the project right.

## 3. What must change

Nothing. Accepted.

## 4. Notes carried forward

Not blocking. Both before Project 2 opens.

- **Your k-comparison table saves as `<pandas.io.formats.style.Styler at 0x7bd573cd2350>` instead of a table.** The highlighted-row styling on `k_comparison` does not survive the notebook save, so that cell shows an object reference to a reader. Your evidence survives anyway — the plots and the written justification carry it — which is the only reason this is a note and not a §3 item. Drop `.style` or wrap it in `display()`. `a1-g06` lost three cells this way.
- **`persona_names = {0: ..., 1: ..., 2: ...}` is hardcoded.** It is *correct* — I checked each row against its label — but it is correct by luck of the label ordering. K-Means numbers its clusters by initialisation, so a different `random_state` reshuffles them and your names would silently follow the wrong rows. Derive them instead: `vip = cluster_summary["Monetary"].idxmax()`, dormant by highest Recency, remainder inferred. `a1-g10` has the strongest version of this if you want to read one.

## 5. Discussion slot

**S14 — Sat 12/09**, short opening slot before the Project 2 block. Present the k=2 versus k=3 argument — you had a 0.001 gap in silhouette to resolve and you resolved it on business grounds rather than on the decimal. That is the discussion the A3 room most needs to have.

## 6. A note to the team

**Ahmed, Mohamed, Kareem, Omar** — on 04/09 I wrote that when three of five teams miss a deadline I assume the problem is mine before I assume it is yours, and I asked you to tell me what got in the way. You answered by shipping, two days later, and shipping something that would have been accepted without revision had it arrived on time.

Two things stood out to me, and neither is the clustering.

The first is that you wrote *"Why Scaling is Essential"* as its own section. The criteria ask for a single sentence there. You wrote a section — which means you were explaining the method to a reader rather than satisfying a checklist, and that difference shows up everywhere else in the notebook.

The second is your persona naming. Your biggest cluster is 238 of 300 customers, 79% of the base, moderately recent and moderately frequent — and you called them "Core / Regular Customers." That sounds like the obvious choice. It was not: four groups across both cohorts looked at a cluster of exactly that shape and reached for "VIP," "At-Risk" or "Dormant," and all four were returned for it. Naming the unremarkable majority accurately, instead of making it sound more interesting than it is, is the single most commercially useful instinct in this project. You had it on your first submission.

Accepted, with two small notes in §4 that cost you nothing this time. Take the S14 slot and walk the room through k=2 versus k=3 — your margin was one thousandth of a silhouette point, and how you broke that tie is worth hearing.

Good to have you back in it.

— Hozaifa
