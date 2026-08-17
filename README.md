# Arabian Academy — AI Engineering Track

This repository is the single source of all course material for the AI Engineering track: project briefs, datasets, group rosters, mentor QA assignments, discussion schedules, and where every group submits their work. New projects are added here as the course progresses — no new links or new repos per project.

**Instructor:** Hozaifa Moustafa · hozaifa.moustafa@alshaya.ai

## Cohorts

This track runs two cohorts out of the same repo:

| Cohort | Sessions | Size | Format |
|---|---|---|---|
| **A1** | Monday & Thursday | ~60 students, groups of 3–5 | Rotating live spotlight discussion (see below) |
| **A3** | Tuesday & Saturday | 18 students, groups of 3–4 | On-site, full-round live discussion |

Work is submitted **per group**, not per individual — see `SUBMISSION_GUIDE.md` for exact rules.

## What's in here

```
arabian-ai-training/
├── 01-ml-project/                    ← Project 1 brief + dataset
├── 02-.../                           ← Project 2, added when released
├── rosters/
│   ├── a1-roster.md                  ← A1 group membership
│   └── a3-roster.md                  ← A3 group membership
├── discussion/
│   ├── a1-discussion-schedule.md     ← A1 rotation rule + tracking table
│   └── a3-discussion-schedule.md     ← A3 full-round schedule
├── qa/
│   ├── a1-mentor-rotation.md         ← which mentor QAs which A1 groups, per project
│   └── a3-mentor-rotation.md         ← which mentor QAs which A3 groups, per project
├── templates/
│   └── QA_REVIEW_TEMPLATE.md         ← mentors copy this into each group's folder
├── submissions/
│   ├── a1-mon-thu/
│   │   ├── a1-g01/
│   │   │   └── 01-ml-project/
│   │   │       ├── a1-g01_01-ml-project.ipynb
│   │   │       └── a1-g01_qa-review.md    ← mentor's QA review
│   │   └── ...
│   └── a3-tue-sat/
│       ├── a3-g01/
│       │   └── 01-ml-project/
│       │       └── a3-g01_01-ml-project.ipynb
│       └── ...
├── README.md
└── SUBMISSION_GUIDE.md
```

## One-time setup (per group)

1. Everyone in the group needs a GitHub account and Git installed. **One student per group** should be the designated "submitter" who runs the git commands, to avoid multiple pushes from the same folder colliding.
2. That student sends the instructor their GitHub username to be added as a collaborator.
3. Clone the repo:
   ```
   git clone https://github.com/HozaifaMoustafa/arabian-ai-training.git
   cd arabian-ai-training
   ```
4. Find your group ID in `rosters/a1-roster.md` or `rosters/a3-roster.md`, and create your folder:
   ```
   mkdir -p submissions/a1-mon-thu/a1-g07/01-ml-project
   ```
   (swap in your actual cohort and group ID)

## Getting new projects (every session)

Pull before you start work each session, so you have any newly released project folders:

```
git pull origin main
```

## Submitting your work

See `SUBMISSION_GUIDE.md` for the full naming convention and git workflow. Short version: work only inside your group's own folder under `submissions/<cohort>/<group-id>/`, commit, pull, then push.

## Discussion sessions

- **A3** (18 students): every group presents live, every project — see `discussion/a3-discussion-schedule.md`.
- **A1** (~60 students): only 3–4 groups present live per session on a rotating queue, so everyone gets a slot roughly once per project cycle; groups not spotlighted post a short written recap instead — see `discussion/a1-discussion-schedule.md` for the exact rotation and the tracking table.

## Mentors & QA

Mentors act as a first-pass QA layer before the instructor's final review. Each project, every group is assigned a mentor (rotating — see `qa/a1-mentor-rotation.md` and `qa/a3-mentor-rotation.md`) who reviews the submission using `templates/QA_REVIEW_TEMPLATE.md` and saves it as `<group-id>_qa-review.md` in the group's project folder.

The flow is: **group submits → assigned mentor reviews and marks Approved or Needs revision → group fixes if needed → instructor does the final review**, focusing mainly on submissions mentors have already approved. This keeps the instructor's review load manageable given the A1 cohort's size.

## Ground rules

- Only add or edit files inside your own group's folder. Don't modify project brief folders, datasets, another group's submission, or the roster/discussion files unless you're the instructor.
- Keep commit messages clear: `<group-id>: submit 0X-project-name` (or `wip` for in-progress commits).
- If `git push` is rejected because someone else pushed first, run `git pull origin main` (this merges cleanly since every group works in a separate folder) and push again.
