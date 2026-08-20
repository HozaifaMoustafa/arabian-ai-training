# Git Pull & Push — Worked Examples

This file shows **real command sequences** students use in this repo. For naming rules and folder layout, see `SUBMISSION_GUIDE.md`.

> **One submitter per group** runs these commands from inside the cloned repo folder (`arabian-ai-training/`).

---

## Example 1 — Pull before you start (every session)

Get the latest project briefs, datasets, and other groups' submissions:

```bash
cd arabian-ai-training
git pull origin main
```

**Expected output (success):**

```
Already up to date.
```

or, if the instructor released something new:

```
Updating abc1234..def5678
Fast-forward
 01-ml-project/retail_transactions_segmentation.csv | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

---

## Example 2 — Work-in-progress commit + push

You saved progress but are not submitting yet. Replace `a1-g07` and the cohort path with your group.

```bash
git add submissions/a1-mon-thu/a1-g07/01-ml-project/
git commit -m "a1-g07: wip RFM features and scatter plot"
git pull origin main
git push origin main
```

**Why pull before push?** Another group may have pushed while you were working. Pulling first keeps your push from being rejected.

---

## Example 3 — Final project submission

```bash
# 1. Stage only your group's folder
git add submissions/a1-mon-thu/a1-g07/01-ml-project/

# 2. Commit with a clear message
git commit -m "a1-g07: submit 01-ml-project"

# 3. Pull, then push
git pull origin main
git push origin main
```

**A3 cohort example** (different folder path, same flow):

```bash
git add submissions/a3-tue-sat/a3-g03/01-ml-project/
git commit -m "a3-g03: submit 01-ml-project"
git pull origin main
git push origin main
```

---

## Example 4 — Push rejected? Pull again, then push

If someone else pushed first, Git may show:

```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'origin'
hint: Updates were rejected because the remote contains work that you do not have locally.
```

**Fix:**

```bash
git pull origin main
git push origin main
```

Because each group only edits its own folder, the pull should merge automatically with **no conflicts**.

---

## Example 5 — Re-submit after mentor says "Needs revision"

```bash
git add submissions/a1-mon-thu/a1-g07/01-ml-project/a1-g07_01-ml-project.ipynb
git commit -m "a1-g07: fix mentor feedback — normalize RFM scores"
git pull origin main
git push origin main
```

---

## Example 6 — A1 written recap (when not in the spotlight)

Add the recap file in the same project folder, then commit with your notebook:

```bash
git add submissions/a1-mon-thu/a1-g07/01-ml-project/a1-g07_recap.md
git add submissions/a1-mon-thu/a1-g07/01-ml-project/a1-g07_01-ml-project.ipynb
git commit -m "a1-g07: submit 01-ml-project + recap"
git pull origin main
git push origin main
```

---

## Quick reference

| Situation | Commands |
|---|---|
| Start of session | `git pull origin main` |
| Save progress | `git add <your-folder>` → `git commit -m "<group-id>: wip ..."` → `git pull` → `git push` |
| Submit project | `git add <your-folder>` → `git commit -m "<group-id>: submit 01-ml-project"` → `git pull` → `git push` |
| Push rejected | `git pull origin main` → `git push origin main` |

---

## Do not do this

- **Do not** `git push --force` — you can overwrite another group's work.
- **Do not** edit files outside your group's folder under `submissions/`.
- **Do not** skip `git pull` right before `git push`.

---

## Check your status anytime

```bash
git status
```

You should see changes only under `submissions/<cohort>/<your-group-id>/` before you commit.
