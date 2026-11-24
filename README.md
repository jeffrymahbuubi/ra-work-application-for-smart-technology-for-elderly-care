# Application of Smart Technology in Older Adult Care

This Tuesday class project explores how home care workers and supervisors in Taiwan could share incident reports, hand over cases, and track follow-up when several workers or agencies support the same older adult.

Today, details can be scattered across calls, messages, and service records. A worker may report the same incident several times, and the next person on the case may have to piece together what happened and what still needs to be done.

## Proposed workflow

1. A care worker records an incident in a shared log for the older adult. The proposal considers text entry and one-tap voice recording.
2. The log shows recent incidents and a traffic-light indicator. Green means relatively stable, yellow means keep monitoring, and red means review promptly. The first version can use simple rules students can explain. A later version could explore AI-based classification.
3. A supervisor reviews the report and the reason for the indicator, then decides what follow-up is needed and whether to adjust assignments or scheduling. The follow-up and its outcome go back into the log.

The project is at the proposal stage. The traffic-light indicator is intended to help supervisors decide what to review first. Clinical decisions require professional judgment, and emergencies follow existing reporting and response procedures. Before any real pilot, the team would need to define required fields, reporting time frames, who can see or change records, and how edits are logged.

## First Codex exercise

**Goal:** Record one fictional incident and see its follow-up status change.

1. Open this folder in Codex and paste the prompt below into the chat.

   > Create an `index.html` file for a home care incident log. Keep everything in one page that I can open directly in a browser. Pre-fill the form with a fictional example: Case A, 2026-11-17, Home safety, and “Loose rug by the front door.” Let me edit the fields and click Add incident. Show the report with the status “Needs follow-up” and a button to mark it “Reviewed.” Keep the records in memory for this exercise, so reloading resets the page. Tell me how to open and try the page.

2. Open the generated `index.html` in your browser and click **Add incident**. Check that the report appears once with the case, date, category, note, and **Needs follow-up** status. Click **Mark reviewed** and check that the status changes to **Reviewed**.
3. Ask Codex for one improvement based on what you saw. For example, if it was hard to tell who reviewed the report, ask to add a reviewer field. Repeat the same steps and check that the reviewer appears beside the updated status.

As a group, decide which fields the next worker needs to act on a report, who should see those fields, and what would justify asking a supervisor to review a case sooner. Use fictional cases throughout the exercise.
