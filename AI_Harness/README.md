# AI Harness

The AI Harness is a control and workflow layer for this Obsidian Vault. It helps an AI agent inspect the Vault, prepare safe drafts, and support human-led knowledge review without replacing the existing knowledge base.

## Architecture

- `AGENTS.md` is the Harness entry point for an agent working inside this directory.
- `instructions/` contains operating, permission, and Vault-structure guidance.
- `workflows/` defines repeatable audit, drafting, and review procedures.
- `tasks/` records task briefs and task-specific working material.
- `plans/` stores numbered execution plans in sequential order.
- `templates/` stores approved English-named templates for repeatable note structures.
- `review/` is the default location for AI-generated drafts awaiting human review.
- `logs/` records actual execution and verified Harness changes.
- `tests/` records acceptance checks for the Harness itself.
- `skills/` contains compatible `SKILL.md` definitions for supported agent workflows.

## Core boundary

The existing knowledge base remains authoritative. Existing Arabic folders and notes must not be renamed, moved, or modified by default. The Harness may describe them in English while preserving their Arabic names exactly.

New Vault knowledge notes and other knowledge outputs are written in Arabic by default. Harness control files remain in English, while execution plans are written in Arabic by default.

New AI-generated drafts belong under `review/` unless the user explicitly authorizes another location. Human review is required before a draft is integrated into the knowledge base.

## How to use it

1. Read `AGENTS.md` and the relevant files in `instructions/`.
2. Choose a workflow from `workflows/`.
3. Save requested execution plans under `plans/` before execution.
4. Keep task material under `tasks/` and drafts under `review/`.
5. Record actual execution in `logs/TASK_LOG.md` and verified Harness changes in `logs/CHANGE_LOG.md`.
6. Run and record the checks in `tests/ACCEPTANCE_TESTS.md`.

This directory does not authorize Git synchronization, background jobs, dependency installation, or edits to existing knowledge notes.
