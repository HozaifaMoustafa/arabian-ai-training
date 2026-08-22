# Submission Guide

Both cohorts share this repository. Submissions are **per group**, organized by cohort. Follow this exactly so pulls and pushes stay conflict-free across ~20 groups.

> ### First, read your project's criteria file
>
> This guide covers **how** to submit — naming, folders, git. It is the same for every project.
>
> **What** to submit is defined per project, in a `SUBMISSION_CRITERIA.md` file inside that project's own folder — for Project 1, `01-ml-project/SUBMISSION_CRITERIA.md`. Every project released in this repo comes with one. It lists the required sections point by point, what you are free to decide yourselves, what gets a submission returned as "Needs revision", and a final self-check list.
>
> That file is exactly what your assigned mentor reviews you against. Read it **before you start working**, and run its §7 self-check before you push.

## 1. Folder and file naming

```
submissions/
├── a1-mon-thu/
│   └── <group-id>/                 e.g. a1-g07
│       ├── 01-ml-project/
│       │   ├── <group-id>_01-ml-project.ipynb
│       │   └── <group-id>_recap.md     ← only if not spotlighted that session (A1 only)
│       └── 02-.../
└── a3-tue-sat/
    └── <group-id>/                 e.g. a3-g03
        └── 01-ml-project/
            └── <group-id>_01-ml-project.ipynb
```

- Your group ID comes from `rosters/a1-roster.md` or `rosters/a3-roster.md` — always use it exactly (lowercase, e.g. `a1-g07`, `a3-g03`).
- One subfolder per project, matching the project folder name at the repo root (e.g. `01-ml-project`).
- One notebook per project per group: `<group-id>_<project-folder-name>.ipynb`.
- A1 groups only: if your group isn't in the live spotlight for a given discussion session, add `<group-id>_recap.md` in that project's folder (see `discussion/a1-discussion-schedule.md`).

## 2. Workflow, step by step

The designated submitter for the group runs these:

**Before starting work:**
```
git pull origin main
```

**While working:** commit as often as you like inside your group's folder (`wip: RFM features done`).

**When ready to submit:**
```
git add submissions/<cohort>/<group-id>
git commit -m "<group-id>: submit 01-ml-project"
git pull origin main
git push origin main
```

The `git pull` right before pushing matters — if another group pushed in the meantime, this brings your local repo up to date first. Since every group works in a separate folder, the merge should always be automatic, with no conflicts, as long as you only touch your own folder.

**If Git reports a conflict anyway:** stop, don't force-push. It almost always means a file outside your own group's folder was touched by mistake — check `git status`, undo anything outside your folder, and try again.

## 3. Deadlines — there are two

Every project has a **QA cutoff** and a **final deadline**. They exist so mentor feedback reaches you *before* you present, not after.

| | When | What it means |
|---|---|---|
| **QA cutoff** | 3 days before the project's first discussion session | Push your best working version. This is the version your mentor reviews. It does not have to be perfect. |
| **Mentor review posted** | 1 day before the discussion session | Your mentor commits `<group-id>_qa-review.md` next to your notebook, marked Approved or Needs revision. |
| **Final deadline** | the discussion session itself | Fix anything the review flagged, push again. This version is what the instructor grades and what you present. |

**Missing the QA cutoff doesn't fail you — it just costs you the review.** Your mentor reviews what is in the repo at the cutoff; if nothing is there, you go into the discussion with no feedback and the instructor sees your work cold. Push something.

Submitting means: your group's notebook is committed and pushed to `submissions/<cohort>/<group-id>/<project-folder>/` before the relevant date. Each project's `SUBMISSION_CRITERIA.md` states its own three dates.

## 4. Discussion sessions

- **A3 groups:** every group presents live each project cycle — no recap needed. See `discussion/a3-discussion-schedule.md`.
- **A1 groups:** check `discussion/a1-discussion-schedule.md` to see if your group is in the spotlight for the upcoming session. If not, submit a short written recap (`<group-id>_recap.md`, 4–6 sentences: what you built, key decision/result, one open question) alongside your notebook.

## 5. Mentor QA review (before instructor review)

After the **QA cutoff** (§3), a mentor reviews whatever you have pushed — before the instructor sees it, and before you present. See `qa/a1-mentor-rotation.md` or `qa/a3-mentor-rotation.md` for who's assigned to your group this project. The mentor fills out `templates/QA_REVIEW_TEMPLATE.md` and commits it as `<group-id>_qa-review.md` in your project folder.

- **Approved:** your submission moves to the instructor's final review as-is.
- **Needs revision:** the mentor's notes will say exactly what to fix. Update your notebook, commit, pull, push again, and the mentor re-checks. Don't wait for the instructor to catch issues the mentor already flagged — treat mentor feedback as required, not optional.

## 6. Checklist before you push

This is the generic, every-project checklist. Your project's `SUBMISSION_CRITERIA.md` has a longer, project-specific one in its §7 — run that one too.

- [ ] Every required point in the project's `SUBMISSION_CRITERIA.md` §2 is present as a labelled section
- [ ] Notebook is in `submissions/<cohort>/<group-id>/<project-folder-name>/`, correctly named
- [ ] Notebook runs top-to-bottom without errors (Restart & Run All)
- [ ] All deliverables the brief asks for are present
- [ ] Recap file added if your group isn't spotlighted this round (A1 only)
- [ ] You pulled latest `main` before pushing
- [ ] Commit message identifies your group and the project

If your mentor marked "Needs revision," re-check this list again before re-pushing.
