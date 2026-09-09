# Final Review — a1-g02 — 01-ml-project

**Instructor:** Hozaifa Moustafa  
**Review date:** 09/09/2026 *(round 2 — supersedes the 04/09/2026 review)*  
**Group:** `a1-g02` — Nadeen Adel, Maram Ahmed, Rawan Mustafa, Nour Osama  
**Cohort:** A1 (Mon/Thu)  
**Project:** 01-ml-project — Customer Segmentation  
**Commit reviewed:** `8240e9c` — *Fix file location and update submission* (07/09/2026)

This is the instructor's final review, re-issued after your catch-up push. The 04/09 version returned this submission; that outcome is now replaced by the one below.

## 1. Outcome

- [x] ✅ **Accepted** — graded and closed, no further action
- [ ] 🔁 **Revise** — fixes listed in §3 must be pushed before the catch-up deadline
- [ ] ⛔ **Not submitted** — nothing in the repo

## 2. What worked

**All four required fixes landed.** Taking them in order:

1. The persona collision is gone. Cluster 0 (40 customers, R 8.4 / F 35.0 / M 29,684) is "VIP / Champions"; cluster 1 (260 customers, R 61.8 / F 8.7 / M 2,661) is now **"Standard / Mainstream Customers"** with its own recommendation — targeted engagement and cross-sell, not premium rewards. That is the honest description of a 260-customer majority, and the strategy attached to it is the right one.
2. You did more than rename. `vip_cluster = cluster_means["Monetary"].idxmax()` derives the VIP cluster from the table instead of asserting it, and the `elif FINAL_K == 2:` branch handles the two-cluster case explicitly rather than letting a four-way persona ladder collapse onto two rows. That is the structural fix, not the cosmetic one — you understood what the note was actually asking for.
3. Six labelled markdown sections, one per required point. The notebook reads as an argument now instead of a script.
4. Correct path and correct filename: `submissions/a1-mon-thu/a1-g02/01-ml-project/a1-g02_01-ml-project.ipynb`, with the old `.ipynb.ipynb` deleted rather than left behind.

Everything is executed with outputs saved — 300-row RFM table, both k plots, the PCA scatter, and the final segment summary all render.

## 3. What must change

Nothing. Accepted.

## 4. Notes carried forward

Not blocking. Fix before Project 2 opens.

- **You copied `retail_transactions_segmentation.csv` into your submission folder** so that `pd.read_csv("retail_transactions_segmentation.csv")` would resolve. §1 asks you not to: *do not copy the CSV into your submission folder*. The intended fix is the relative path back to the shared file — `../../../../01-ml-project/retail_transactions_segmentation.csv`. `a1-g10` does exactly this if you want to see it. One dataset, one copy; four groups each carrying their own is how the two silently drift apart.
- Your k evidence is printed (`Best K based on silhouette score: 2`, `0.6789`) but not *written*. Point 3 asks for 2–4 sentences on what in the plots led you there. I told you on 04/09 that your k was properly evidenced and I stand by that, so this does not change the outcome — but on Project 2 write the paragraph. The number is the finding; the sentences are the argument.

## 5. Discussion slot

**S13 — Thu 10/09.** Present the corrected version, framed as *what we changed and why*. Two minutes on why cluster 1 is "Standard" and not "VIP" is the whole story — the room has three other groups who made the same mistake.

## 6. A note to the team

**Nadeen, Maram, Rawan, Nour** — you fixed the right thing.

I want to be specific, because there is a version of this where you rename cluster 1 and move on, and that is not what you did. You went back to the naming *logic* — derived VIP from `idxmax()`, added an explicit branch for k=2 — so the bug cannot come back the next time K-Means shuffles its labels. That is the difference between patching an output and fixing a cause, and it is genuinely the harder instinct to learn. Several groups this round patched the output.

The foundation was solid on 04/09 and I said so then. Now the last mile matches it. Accepted, no conditions. Take the S13 slot and show the room the corrected persona table — you are the clearest worked example of that mistake and its fix that I have.

— Hozaifa
