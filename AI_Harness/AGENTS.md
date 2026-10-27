# AI Harness Agent Entry Point

You are operating inside the AI Harness of an existing Obsidian Vault.

## Required reading

Before acting, read:

1. `instructions/OPERATING_RULES.md`
2. `instructions/PERMISSIONS_POLICY.md`
3. `instructions/VAULT_STRUCTURE_GUIDE.md` when inspecting or referencing Vault folders
4. The specific workflow and skill relevant to the task

## Default behavior

- Treat existing knowledge notes as user-owned and preserve them.
- Keep all Harness names, filenames, instructions, logs, and test documents in English.
- Store AI-generated drafts under `review/` by default.
- Store every requested execution plan under `plans/` using the sequential naming rule defined in `workflows/PLAN_MANAGEMENT.md`.
- Prefer read-only inspection and explicit, narrow changes.
- Never infer approval for integrating a draft into the knowledge base.
- Record actual work in `logs/TASK_LOG.md` and verified Harness changes in `logs/CHANGE_LOG.md`.
- Report conflicts, skipped items, and uncertainty clearly.

## Approval boundary

Ask for approval before modifying existing knowledge notes, integrating drafts, synchronizing Git, creating background jobs, or installing dependencies. Do not perform forbidden actions listed in `instructions/PERMISSIONS_POLICY.md`.

When the user asks for a plan, create and save the plan first under `plans/`, then provide the plan and its file link. Do not treat saving a plan as permission to execute it.

`AI_Harness/AGENTS.md` governs work that explicitly uses this Harness. It does not automatically govern the entire Vault; a separate root-level `AGENTS.md` would be needed for that purpose. None was created because it was not needed and no existing root-level file was overwritten.
