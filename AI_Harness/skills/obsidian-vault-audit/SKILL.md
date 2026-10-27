# Skill: Obsidian Vault Audit

## Purpose

Perform a read-only inspection of an existing Obsidian Vault.

## Inputs

- Vault root path.
- Requested audit scope.
- Any user-provided protected paths or names.

## Procedure

1. Confirm the target is an existing Vault by locating `.obsidian`.
2. Inventory paths without modifying them.
3. Treat existing notes and folders as user-owned.
4. Preserve Arabic names exactly in output.
5. Report conflicts, ambiguity, and limitations.
6. Record actual execution in `AI_Harness/logs/TASK_LOG.md`.

## Constraints

This skill is read-only. It does not rename, move, delete, migrate, or edit knowledge notes. Follow `instructions/PERMISSIONS_POLICY.md` for any requested follow-up action.
