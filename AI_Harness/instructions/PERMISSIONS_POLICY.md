# Permissions Policy

## Allowed by default

- Read-only inspection of the Vault.
- Creating missing AI Harness directories and files inside `AI_Harness/`.
- Updating Harness logs when recording actual work.
- Creating AI-generated drafts under `AI_Harness/review/`.
- Running local validation that does not install software or alter existing knowledge notes.

## Approval required

Obtain explicit user approval before:

- Modifying, renaming, moving, or deleting any existing knowledge folder or note.
- Integrating a draft into an existing knowledge folder.
- Writing outside `AI_Harness/`.
- Synchronizing Git, committing, pushing, pulling, or changing branches.
- Creating background jobs, scheduled tasks, or watchers.
- Installing dependencies, plugins, or software.
- Bulk edits, migrations, or reorganizations.

## Forbidden

- Overwriting an existing file without explicit authorization and a defined replacement plan.
- Creating a second Vault or migrating existing knowledge.
- Moving existing AI-related notes into the Harness.
- Renaming or altering original Arabic names to make them more convenient.
- Claiming that a draft was human-reviewed or integrated when it was not.
- Fabricating log entries or validation results.

When a conflict is found, preserve the existing file, report the path, and stop that individual write.
