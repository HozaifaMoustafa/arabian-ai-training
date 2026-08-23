# Submission Criteria — <project-folder-name> (<Project Title>)

> **Instructor note:** copy this file into every new project folder as `SUBMISSION_CRITERIA.md` and fill it in when the project is released, so each project states its own delivery criteria in one predictable place. See `01-ml-project/SUBMISSION_CRITERIA.md` for a completed example. Delete this note in the filled-in copy.

Read this **before you start working**, not the night before the deadline. It tells you exactly what a complete submission looks like for this project, what you are free to decide yourselves, and what will get your work sent back as "Needs revision."

Every project folder in this repo has its own `SUBMISSION_CRITERIA.md`. The general git and naming rules live in `SUBMISSION_GUIDE.md` — this file is only about *this* project's content.

**Due:** _ **Submitted per group**, not per person.

---

## 1. What you submit

```
submissions/<cohort>/<group-id>/<project-folder-name>/
├── <group-id>_<project-folder-name>.ipynb      ← required, one notebook
└── <group-id>_recap.md                         ← A1 groups only, and only if NOT spotlighted this session
```

- One notebook per group.
- Any additional required artefact for this project: _
- Load the dataset from its repo path, not from a local machine path.

---

## 2. Delivery criteria, point by point

One numbered point per required step from the brief. Each must be a **labelled markdown section** in the notebook.

### Point 1 — _
- _
- _

*Not accepted:* _

### Point 2 — _
- _

*Not accepted:* _

### Point 3 — _
- _

*Not accepted:* _

*(add or remove points to match this project's brief)*

---

## 3. Also required

- **Runs top to bottom.** Restart & Run All completes with no errors, outputs saved in the committed notebook.
- **Narrative, not just code.** Markdown cells explaining what each section does and why.
- **A1 groups not spotlighted this session:** `<group-id>_recap.md`, 4–6 sentences — what you built, key decision or result, one open question.

---

## 4. What you are free to decide

- _
- _

---

## 5. What gets your submission returned

- Any required point missing or unlabelled.
- _
- Errors on Restart & Run All, or outputs stripped out.
- Wrong filename or wrong folder — see `SUBMISSION_GUIDE.md` §1.
- Files added or edited outside your own group's folder.
- Work copied from another group.

---

## 6. How it's judged

Your mentor reviews against this file using `templates/QA_REVIEW_TEMPLATE.md`, marks **Approved** or **Needs revision**, and commits it as `<group-id>_qa-review.md` next to your notebook.

Priority order for this project:

1. _
2. _
3. _

---

## 7. Final self-check before you push

- [ ] Notebook in the right folder with the right name
- [ ] Every point in §2 present as a labelled section
- [ ] _
- [ ] Restart & Run All passes, outputs saved
- [ ] Recap file added if your A1 group isn't spotlighted this session
- [ ] Nothing changed outside your group's folder — run `git status` to confirm
- [ ] `git pull origin main` done before pushing
