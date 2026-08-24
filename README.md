# Power BI Version Control with Git (PBIP/TMDL)

**This is a course exercise, not a standalone portfolio project.** It follows
the Udemy course "Power BI CI/CD: GitHub, Version Control, Pipelines" by
A Siva Theja, covering the offline Git workflow only — Power BI Service /
Microsoft Fabric deployment pipelines are out of scope.

## What this demonstrates

- Saving a Power BI report as a **Power BI Project (PBIP)** instead of a
  binary `.pbix` file, so the semantic model and report are stored as
  readable text (TMDL / JSON)
- Tracking changes to Power Query (M), DAX measures, and report visuals
  through Git
- Branching, merging, and resolving a merge conflict on the semantic model
- Rolling back an accidental change (deleted visual) using Git history

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

*(dashboard)*

*(git diff on a DAX measure in TMDL)*

## Course credit

Built following the Udemy course "Power BI CI/CD: GitHub, Version Control,
Pipelines" by A Siva Theja.
