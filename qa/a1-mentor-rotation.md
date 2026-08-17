# A1 Mentor Rotation — QA Assignments

Mentor-to-group assignments rotate every project, so each mentor sees different groups over the course rather than owning the same batch permanently.

## Group batches (fixed groupings, only the mentor assigned to each rotates)

| Batch | Groups |
|---|---|
| Batch 1 | a1-g01, a1-g02, a1-g03, a1-g04 |
| Batch 2 | a1-g05, a1-g06, a1-g07, a1-g08 |
| Batch 3 | a1-g09, a1-g10, a1-g11, a1-g12 |
| Batch 4 | a1-g13, a1-g14, a1-g15 |

## Rotation table (cyclic shift each project — M1→2→3→4→1...)

| Project | Batch 1 | Batch 2 | Batch 3 | Batch 4 |
|---|---|---|---|---|
| 01-ml-project | M1 | M2 | M3 | M4 |
| 02-... | M4 | M1 | M2 | M3 |
| 03-... | M3 | M4 | M1 | M2 |
| 04-... | M2 | M3 | M4 | M1 |

Add a row per new project, continuing the shift pattern (each mentor moves to the batch of the mentor before them in the row above).

## Workflow

1. Group submits (pushes notebook) before the project deadline.
2. The mentor assigned to that group's batch this project reviews it using `templates/QA_REVIEW_TEMPLATE.md`, saved as `<group-id>_qa-review.md` in the group's project folder.
3. If "Needs revision," the group fixes and re-pushes; mentor re-checks.
4. Once "Approved," the instructor does the final review — only approved submissions need a full instructor pass, which is the point of this step.
