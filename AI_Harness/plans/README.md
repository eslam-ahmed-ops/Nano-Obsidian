# Execution Plans

This directory stores execution plans requested by the user. A plan is a controlled proposal, not permission to execute its steps.

## Naming rule

Use the next unused three-digit number:

`PLAN_001_ENGLISH_SLUG.md`

Examples:

- `PLAN_001_SUMMARIZE_KNOWLEDGE_NOTE.md`
- `PLAN_002_REVIEW_AND_IMPROVE_NOTE.md`

Filenames must use English letters, numbers, underscores, and the `.md` extension. Never reuse a number and never overwrite an existing plan. If a plan needs a substantial revision, create the next plan number and reference the earlier plan.

## Required metadata

Each plan must include:

- Plan number
- English title
- Creation date
- Status: `Draft`, `Approved`, `In Progress`, `Completed`, or `Cancelled`
- Scope and target paths
- Required approvals
- Steps
- Validation method
- Risks and rollback approach

The plan body may follow the language requested by the user, but filenames and control metadata remain in English. If the plan creates a note draft, save that draft under `../review/` and link to it from the plan.

## Creation procedure

1. Scan this directory for existing `PLAN_###_*.md` files.
2. Select the next unused number, starting at `001`.
3. Convert the request into a short English filename slug.
4. Check for a filename conflict before writing.
5. Create the plan with status `Draft`.
6. Present the saved file path to the user.
7. Ask for approval before executing any step that requires approval.
