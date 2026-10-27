# Safe Note Drafting Workflow

Purpose: create an AI-generated draft without silently changing the knowledge base.

1. Clarify the requested topic, audience, and intended destination.
2. Read only the sources needed for the draft and preserve source paths.
3. Create the draft under `AI_Harness/review/` unless the user explicitly authorizes another location.
4. Write new Vault knowledge drafts in Arabic unless the user explicitly requests another language. Keep Harness metadata and control files in English, except execution plans, which are Arabic by default.
5. Preserve any quoted source names exactly.
6. Mark assumptions, unresolved claims, and source gaps.
7. Do not overwrite an existing file; inspect conflicts and report them.
8. Add a review note stating that human review is required.
9. Record the task and output path in `logs/TASK_LOG.md`.
10. Wait for explicit approval before integrating the draft into existing knowledge.
