# Capstone Projects — built live in session

These are the projects **the instructor builds with you, live, during the session** — not group assignments. There is no `SUBMISSION_CRITERIA.md` here, nothing to push into `submissions/`, and no mentor QA round. They exist so that by the end of the track this repo holds a full set of portfolio projects: the ones you built and were reviewed on, plus complete worked ones built end to end with you.

## How each one works

1. **Before the session** — the client brief and the dataset are already in the project folder. Read the brief beforehand so the session isn't the first time you see the problem.
2. **During the session** — we build it together on screen. Follow the reasoning, not the keystrokes. You don't need to type along or screenshot anything.
3. **After the session** — the finished notebook is pushed into the same folder. Run `git pull origin main` to get it.

```
git pull origin main
```

Because the notebook lands *after* the session, a folder here with no `.ipynb` in it simply means we haven't built it yet, or it hasn't been pushed yet. Watch the repo (see the root `README.md`) so you get the announcement when it does.

## Projects

| # | Project | Domain | Dataset | Built live | Notebook |
|---|---|---|---|---|---|
| 01 | [Churn Prediction — Wasla Telecom](01-churn-prediction/) | Supervised classification | `wasla_customer_records.csv` — 7,043 customers, 21 fields | Session 8 — A3 Sat 22/08/2026, A1 Mon 24/08/2026 | Pending — pushed after the live session |

More are added as the track progresses.

## 01 — Churn Prediction for Wasla Telecom

Wasla Telecom lost roughly 27% of its subscriber base to churn over the past year. The task set by their VP of Customer Retention: identify which customers are at risk of leaving *before* they leave, and explain why, so the retention team can act early.

**Brief:** `01-churn-prediction/Wasla_Telecom_Churn_Project_Brief.pdf` (also as `.docx`)
**Dataset:** `01-churn-prediction/wasla_customer_records.csv` — real customer records, provided as-is from the billing system, quirks included.

> **Read the brief for the problem, not for a deadline.** It's written in the standard client-brief format, so it carries "Your Task", "Deliverables" and "Due Date" headings. Those don't apply here — this one is covered end to end in Session 8 and there is nothing to hand in. The brief is there so you see the problem the way a client would state it.

What we cover building it:

- **EDA** — who churns, and how it tracks with contract type, tenure, billing and add-on services. One column hides a data-type bug that only shows up if you check carefully.
- **Cleaning & preprocessing** — fixing that data-type issue, consistent categorical encoding, scaling where it's needed.
- **Three models** — Logistic Regression, Random Forest and XGBoost, compared fairly with cross-validation.
- **Picking a metric that matters** — only about 1 in 4 customers churn, so accuracy alone is misleading.
- **The evaluation report** — turning the model into retention actions someone non-technical can act on, e.g. *"month-to-month customers with no tech support churn far more — prioritise outreach there."*

The last point is the real deliverable of the project. A slightly less accurate model with a clear, actionable report beats a marginally better model with no business takeaway.

## Using these in your portfolio

These are yours to keep and show. If you put one on your own GitHub, write your own README for it explaining the problem and what the results mean — a bare notebook with no framing doesn't read as portfolio work to anyone reviewing it.

Questions about anything we built go in an issue using the **❓ Question** template, same as everything else.
