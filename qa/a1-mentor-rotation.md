# A1 Mentor Rotation — QA Assignments

Mentor-to-group assignments rotate every project, so each mentor sees different groups over the course rather than owning the same batch permanently.

Mentors: **Ahmed Salama**, **Ammar Gomaa**, **Adham Ahmed**, **Youssef Anwar** (see `rosters/mentors.md`).

## Group batches (fixed groupings, only the mentor assigned to each rotates)

| Batch | Groups | Group count |
|---|---|---|
| Batch 1 | a1-g01, a1-g02, a1-g03, a1-g04 | 4 |
| Batch 2 | a1-g05, a1-g06, a1-g07, a1-g08 | 4 |
| Batch 3 | a1-g09, a1-g10, a1-g11, a1-g12 | 4 |
| Batch 4 | a1-g13, a1-g14, a1-g15 | 3 |

## Rotation table

| Project | Batch 1 | Batch 2 | Batch 3 | Batch 4 |
|---|---|---|---|---|
| 01-ml-project | Youssef Anwar | Ammar Gomaa | Adham Ahmed | Ahmed Salama |
| 02-... | Adham Ahmed | Youssef Anwar | Ahmed Salama | Ammar Gomaa |
| 03-... | Ammar Gomaa | Ahmed Salama | Youssef Anwar | Adham Ahmed |
| 04-... | Youssef Anwar | Adham Ahmed | Ammar Gomaa | Ahmed Salama |

**Conflict of interest:** Youssef Anwar is a student in `a1-g14`, which is in **Batch 4** — so Youssef never appears in the Batch 4 column. That is why this is not a plain cyclic shift. Ammar and Adham each cover all four batches exactly once; Ahmed covers Batch 4 twice (projects 1 and 4) to absorb Youssef's exclusion; Youssef covers Batch 1 twice (projects 1 and 4). No mentor gets the same batch two projects in a row.

Review load over the four projects: Youssef 16 groups, Ammar 15, Adham 15, Ahmed 14 — Youssef's exemption costs him nothing, since Batch 4 is the smallest batch.

**Adding project 5 and beyond:** don't just continue a shift pattern — it will eventually land Youssef on Batch 4. Copy the project 1–4 block again as-is (project 5 = project 1's row, and so on). If the roster changes such that `a1-g14` moves to a different batch, rebuild this table around the new exclusion.

## Workflow

1. Group pushes their working notebook by the **QA cutoff** — Project 1: **Fri 28/08/2026**.
2. The mentor assigned to that group's batch reviews it using `templates/QA_REVIEW_TEMPLATE.md`, saved as `<group-id>_qa-review.md` in the group's project folder. **Post all reviews by the review deadline** — Project 1: **Sun 30/08/2026**. Review whatever is in the repo at the cutoff; if a group pushed nothing, mark it and move on.
3. If "Needs revision," the group fixes and re-pushes before the **final deadline** (Project 1: Mon 31/08/2026); mentor re-checks.
4. The instructor then reviews **every** group using `templates/FINAL_REVIEW_TEMPLATE.md`, committed as `<group-id>_final-review.md` next to the notebook — including groups still marked "Needs revision" and groups that submitted nothing, since that file is also how those groups are notified. Outcome is ✅ Accepted, 🔁 Revise by \<date\>, or ⛔ Not submitted.

All four mentors work the same window (~4 groups each), regardless of when their batch is spotlighted — see `discussion/a1-discussion-schedule.md`.

Capstone projects under `capstone-projects/` are built live by the instructor and are **not** reviewed here — there is nothing submitted for them.
