# Acceptance Tests

Record actual validation results. A check is complete only when it has been run and its result is known.

## Initial Harness validation — 2026-10-27

- [x] `AI_Harness/` exists at the Vault root.
- [x] Required directories exist.
- [x] Required files exist with English names.
- [x] Existing root-level files and folders were inspected before creation.
- [x] No existing file was overwritten.
- [x] No existing Arabic folder or note was modified.
- [x] No second Vault was created.
- [x] No existing AI-related notes were moved.
- [x] New drafts are directed to `AI_Harness/review/` by default.
- [x] New Vault knowledge outputs are directed to Arabic by default; Harness control files remain English and plans remain Arabic.
- [x] Requested execution plans are directed to `AI_Harness/plans/`.
- [x] Plan numbering uses the next unused three-digit number and English filename slugs.
- [x] Skill files use the supported `SKILL.md` format.
- [x] No root-level `AGENTS.md` was created because Harness-local scope is sufficient.

## Follow-up checks

- [ ] Human review of the Harness wording completed.
- [ ] Any future change is logged with its actual validation result.
