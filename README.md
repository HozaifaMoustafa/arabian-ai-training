# Arabian Academy — AI Engineering Track

This repository is the single source of all course material for the AI Engineering track: project briefs, datasets, group rosters, mentor QA assignments, discussion schedules, capstone projects built live in session, and where every group submits their work. New projects are added here as the course progresses — no new links or new repos per project.

By the end of the track this repo holds every portfolio project you need: the ones **you** build and submit as a group, and the ones **we build together in session** under `capstone-projects/`.

**Instructor:** Hozaifa Moustafa · hozaifa.dev@gmail.com

## Cohorts

This track runs two cohorts out of the same repo:

| Cohort | Sessions | Size | Format |
|---|---|---|---|
| **A1** | Monday & Thursday | ~60 students, groups of 3–5 | Rotating live spotlight discussion (see below) |
| **A3** | Tuesday & Saturday | 18 students, groups of 3–4 | On-site, full-round live discussion |

Work is submitted **per group**, not per individual — see `SUBMISSION_GUIDE.md` for exact rules, and each project's own `SUBMISSION_CRITERIA.md` for what that project must contain.

## What's in here

```
arabian-ai-training/
├── .github/ISSUE_TEMPLATE/           ← announcement + question templates
├── 01-ml-project/
│   ├── Customer_Segmentation_Project_Brief.docx
│   ├── retail_transactions_segmentation.csv
│   └── SUBMISSION_CRITERIA.md         ← what a complete submission for THIS project must contain
├── 02-.../                           ← Project 2, added when released (with its own SUBMISSION_CRITERIA.md)
├── capstone-projects/                ← built live in session by the instructor — see below
│   ├── README.md
│   └── 01-churn-prediction/
│       ├── Wasla_Telecom_Churn_Project_Brief.pdf
│       ├── wasla_customer_records.csv
│       └── <notebook>.ipynb           ← posted here after the live session
├── rosters/
│   ├── a1-roster.md                  ← A1 group membership
│   ├── a3-roster.md                  ← A3 group membership
│   └── mentors.md                    ← mentor names + conflict-of-interest rule
├── discussion/
│   ├── a1-discussion-schedule.md     ← A1 rotation rule + tracking table
│   └── a3-discussion-schedule.md     ← A3 full-round schedule
├── qa/
│   ├── a1-mentor-rotation.md         ← which mentor QAs which A1 groups, per project
│   └── a3-mentor-rotation.md         ← which mentor QAs which A3 groups, per project
├── templates/
│   ├── QA_REVIEW_TEMPLATE.md         ← mentors copy this into each group's folder
│   └── SUBMISSION_CRITERIA_TEMPLATE.md  ← instructor copies this into each new project folder
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

## Two kinds of project in this repo

They live in different folders and work differently — don't mix them up.

| | **Group projects** (`01-ml-project/`, `02-...`) | **Capstone projects** (`capstone-projects/`) |
|---|---|---|
| Who builds it | You, in your group, on your own time | The instructor, live with you in the session |
| Has `SUBMISSION_CRITERIA.md` | Yes | No |
| You submit it | Yes — into `submissions/<cohort>/<group-id>/` | No |
| Mentor QA review | Yes | No |
| What you get | Feedback and a review cycle on your own work | A complete, worked reference project for your portfolio |

**Capstone projects** are the ones we build together on screen during the session. Each folder holds the client brief and the dataset up front, and the **notebook is pushed here after the live session** — so you can follow along live without racing to copy code, then pull the finished notebook afterwards and re-read it at your own pace.

The point is that by the end of the track this repo contains a full set of portfolio projects: the ones you built yourselves and were reviewed on, plus the ones built with you end to end. Both are yours to show. See `capstone-projects/README.md` for the current list.

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

## Turn on notifications — everyone, once

**Do this on day one.** It is how you find out that a new project was released, a deadline moved, or submission criteria changed — without having to keep checking the repo manually.

1. Open the repo on GitHub: https://github.com/HozaifaMoustafa/arabian-ai-training
2. Click **Watch** (top right, next to Star).
3. Choose **All Activity**, then Apply.

GitHub will now email you whenever the instructor posts a course announcement. Make sure the email on your GitHub account is one you actually read, and check your spam folder for the first one — mark it "not spam" so the rest arrive.

Every announcement is an issue in this repo labelled **`announcement`**, so you can also read the full history any time at [Issues → label:announcement](https://github.com/HozaifaMoustafa/arabian-ai-training/issues?q=label%3Aannouncement). Nothing important is announced only in class.

> **Note for the instructor:** push the change to `main` first, then open the announcement issue (**Issues → New issue → 📣 Course announcement**). Opening that issue is what triggers the emails, so it should point at work that is already live. Bare `git push` alone does **not** email anyone.

## Asking questions

Open an issue using the **❓ Question** template — questions about a brief, the submission criteria, or the git workflow get answered once, publicly, where the whole cohort benefits. Check your project's `SUBMISSION_CRITERIA.md` first; §4 and §5 answer most of them.

Anything specific to your group's own submission goes to your assigned mentor instead — see `qa/a1-mentor-rotation.md` or `qa/a3-mentor-rotation.md`.

## Getting new projects (every session)

Even with notifications on, pull before you start work each session so you have any newly released project folders:

```
git pull origin main
```

Pull **after** a session too — that's when the notebook for a capstone project we built together gets pushed.

## Submitting your work

Two files govern every submission, and they answer different questions:

| File | Question it answers |
|---|---|
| `SUBMISSION_GUIDE.md` (repo root) | **How** to submit — folder layout, file naming, the git workflow. Same for every project. |
| `<project-folder>/SUBMISSION_CRITERIA.md` | **What** to submit for that specific project — required sections point by point, what you may decide yourselves, what gets returned as "Needs revision", and the final self-check. |

**Every project released in this repo ships with its own `SUBMISSION_CRITERIA.md` inside its project folder.** Read it before you start working — it is the exact checklist your assigned mentor reviews you against, so there should be no surprises about what "done" means. For Project 1 that file is `01-ml-project/SUBMISSION_CRITERIA.md`.

Short version of the workflow: work only inside your group's own folder under `submissions/<cohort>/<group-id>/`, commit, pull, then push.

## Discussion sessions

- **A3** (18 students): every group presents live, every project — see `discussion/a3-discussion-schedule.md`.
- **A1** (~60 students): all 15 groups present live, split across a two-session block per project so the discussion closes while the work is fresh — see `discussion/a1-discussion-schedule.md` for the split and the tracking table.

## Mentors & QA

The four mentors are **Ahmed Salama, Ammar Gomaa, Adham Ahmed and Youssef Anwar** — see `rosters/mentors.md`.

Mentors act as a first-pass QA layer before the instructor's final review. Each project, every group is assigned a mentor (rotating — see `qa/a1-mentor-rotation.md` and `qa/a3-mentor-rotation.md`) who reviews the submission using `templates/QA_REVIEW_TEMPLATE.md` and saves it as `<group-id>_qa-review.md` in the group's project folder.

Two of the mentors are also students in the track (Ahmed in `a3-g01`, Youssef in `a1-g14`). **Neither reviews their own group** — the rotation tables are built so those pairings never come up, so just follow the table.

The flow is: **group pushes by the QA cutoff → assigned mentor reviews and marks Approved or Needs revision → group fixes before the final deadline → instructor does the final review**, focusing mainly on submissions mentors have already approved. This keeps the instructor's review load manageable given the A1 cohort's size.

That is why every project has **two** dates and not one — a QA cutoff three days early so the review can actually reach you, and the real deadline. See `SUBMISSION_GUIDE.md` §3. For Project 1: A3 pushes by **Wed 26/08**, A1 by **Fri 28/08**.

## Ground rules

- Only add or edit files inside your own group's folder. Don't modify project brief folders, datasets, another group's submission, or the roster/discussion files unless you're the instructor.
- Keep commit messages clear: `<group-id>: submit 0X-project-name` (or `wip` for in-progress commits).
- If `git push` is rejected because someone else pushed first, run `git pull origin main` (this merges cleanly since every group works in a separate folder) and push again.
