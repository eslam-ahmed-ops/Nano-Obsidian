# Plan Management Workflow

Purpose: ensure every requested execution plan is saved, numbered, reviewable, and separate from execution.

## Trigger

Use this workflow whenever the user asks for a plan, implementation plan, strategy, roadmap, action plan, or steps to execute a task.

## Procedure

1. Read the relevant Harness instructions and identify the requested scope.
2. Inspect `AI_Harness/plans/` and find the highest existing `PLAN_###_*.md` number.
3. Choose the next unused three-digit number. Never reuse a number.
4. Create an English filename using `PLAN_###_ENGLISH_SLUG.md`.
5. Check the exact destination for conflicts. Do not overwrite an existing file.
6. Save the plan with status `Draft` and the required metadata.
7. Include objectives, scope, assumptions, ordered steps, approvals, risks, validation, and rollback.
8. Return the saved plan path to the user.
9. Keep the plan separate from execution. A saved plan does not authorize its execution.
10. If the user approves execution, follow the permission policy step by step and update the plan status accurately.

## Revision rule

Do not silently rewrite an existing plan. Create a new numbered plan for a substantial revision and link the new plan to the earlier one. Minor corrections may be made only when the user explicitly asks to edit that plan.

## Storage rule

Plans belong in `AI_Harness/plans/`. AI-generated note drafts belong in `AI_Harness/review/`, even when a plan created those drafts.
