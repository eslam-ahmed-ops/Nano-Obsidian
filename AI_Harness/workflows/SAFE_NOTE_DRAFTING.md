# Safe Note Drafting Workflow

Purpose: create an AI-generated draft without silently changing the knowledge base.

1. Clarify the requested topic, audience, and intended destination.
2. Read only the sources needed for the draft and preserve source paths.
3. Create the draft under `AI_Harness/review/` unless the user explicitly authorizes another location.
4. Use English for Harness metadata and preserve any quoted source names exactly.
5. Mark assumptions, unresolved claims, and source gaps.
6. Do not overwrite an existing file; inspect conflicts and report them.
7. Add a review note stating that human review is required.
8. Record the task and output path in `logs/TASK_LOG.md`.
9. Wait for explicit approval before integrating the draft into existing knowledge.
