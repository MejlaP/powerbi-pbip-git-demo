# Power BI Version Control with Git (PBIP/TMDL)

**This is a course exercise, not a standalone portfolio project.** It is based
on the Udemy course "Power BI CI/CD: GitHub, Version Control, Pipelines" by
A Siva Theja, adapted to run without SQL Server and without a Power BI Service
tenant — see *How this differs from the course* below.

## What this demonstrates

- Saving a Power BI report as a **Power BI Project (PBIP)** instead of a
  binary `.pbix` file, so the semantic model and report are stored as
  readable text (TMDL / JSON)
- Tracking changes to Power Query (M), DAX measures, and report visuals
  through Git
- Branching, merging, and resolving a merge conflict on the semantic model
- Rolling back an accidental change (deleted visual) using Git history

## How this differs from the course

| Course setup | This repo | Why |
|---|---|---|
| SQL Server with three databases (`Finance_Dev/_Test/_Prod`) | A single CSV file (Microsoft Financial Sample) | The three databases exist to feed three Fabric workspaces in the deployment-pipeline part of the course, which is out of scope here. For Git version control the data source is irrelevant. |
| Two developers on separate machines | One developer, two branches | The merge conflict is produced deliberately by changing the same measure on two branches and merging both into `dev` — same mechanics, no second account needed. |
| Power BI Service / Fabric deployment pipelines | Not covered | Requires a work or school account; this repo is the local Git workflow only. |

## Why this matters

Publishing a report to Power BI Service solves distribution, not version
control — it shows what's live right now, not what changed, who changed it,
or why. This is a small, hands-on demo of the alternative: a Power BI report
whose history lives in Git, with real diffs instead of a stack of
`report_final_v3.pbix` files.

## Data

The report is built on a small sample financials dataset (~700 rows) that
comes with the course. The data file itself is not included here — a PBIP
project stores only the model and report definitions, not the data.

## Screenshots

**The report**

<img width="1240" height="661" alt="dashboard" src="https://github.com/user-attachments/assets/2315fce8-93bb-4a94-af9c-65c509bb8e1c" />


**A DAX measure change as a text diff**

<img width="587" height="233" alt="final_diff_readme" src="https://github.com/user-attachments/assets/b5a56f71-a553-4da4-9d83-3fe0121eec5a" />


Because the semantic model is stored as TMDL, a change to a measure shows up
as two lines of readable text rather than a binary file that "just changed".

## Course credit

The Git workflow in this repo follows the Udemy course "Power BI CI/CD:
GitHub, Version Control, Pipelines" by A Siva Theja. The data source, the
single-developer merge-conflict setup, and leaving out the Fabric
deployment-pipeline part are my own adaptations — see *How this differs
from the course* above.
