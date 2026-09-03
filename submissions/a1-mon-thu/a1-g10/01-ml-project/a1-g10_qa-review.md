# QA Review a1-g10 <group-id> 01-ml-project <project-folder-name>

Mentors: copy this file into the group's project folder as `<group-id>_qa-review.md`, fill it in, and commit it alongside your review. This sits between the group's submission and the instructor's final review, so keep it honest and specific — the instructor relies on this instead of re-checking everything from scratch.

**Mentor:** Youssef Hassan
**Review date:** 9/2/2026
**Group:** g10
**Project:** Customer Segmentation Project
**Submission commit checked:** latest as of push (paste the commit hash or note "latest as of push")

## 1. Deliverable checklist

Work through the numbered points in that project's `SUBMISSION_CRITERIA.md` §2 (e.g. `01-ml-project/SUBMISSION_CRITERIA.md`) — that file is the agreed definition of "complete," and the group was told to build against it. Copy its points here and check each one off:

- [X] Point 1 — RFM feature table built from the raw transactions
- [X] Point 2 — Features scaled before clustering
- [X] Point 3 — Choice of k justified with evidence
- [X] Point 4 — K-Means fitted with your chosen k
- [X] Point 5 — PCA visualization of the clusters
- [X] Point 6 — Named personas grounded in the numbers

Also check the "Not accepted" notes under each point — those are the specific failure modes to look for.

## 2. Runs cleanly?

Restart & Run All (or equivalent) — does it execute top to bottom without errors?

**Result:** No
**Notes:** error (there are no such file or directory 'retail_transactions_segmentation.csv')

## 3. Correctness

Does the methodology match what the brief asked for, and do the results make sense (e.g. numbers aren't obviously wrong, conclusions follow from the data)?

**Notes:** the methodology match what the brief asked for but the Opti K need to reconsider.

## 4. Clarity

Is the notebook/report readable — labeled sections, explained reasoning, not just code with no narrative?

**Notes:**  yes everything is label Cleary and explained Cleary too

## 5. Overall status

- [ ] ✅ **Approved** — ready for instructor's final review
- [X] 🔁 **Needs revision** — see notes below, group should fix and re-push before instructor review

## 6. Revision notes to the group (if applicable)

_
first file name is wrong the right name is a1-10_01-ml-project
second when i run the code it doesn't work say there are no such file or directory so, pleases review this error.
third to be more readable split each point in speared cell (this doesn't mean that you are wrong).
_
