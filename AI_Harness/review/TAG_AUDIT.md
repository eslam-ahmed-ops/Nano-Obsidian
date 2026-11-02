# Tag Audit

## Scope

This is a read-only audit record for the unified Vault migration. It does not authorize bulk tag replacement.

## Findings

- Existing notes use a mixture of Arabic YAML tags, English tags, inline hashtags, and unstructured list values.
- Common legacy examples include `برمجة`, `تقنية`, `Agent-Skills`, `ai`, `python`, `library`, and `weekly-log`.
- New destination indexes now use the Arabic hierarchical taxonomy defined in `instructions/TAG_TAXONOMY.md`.
- Legacy tags remain in place during the transition to avoid breaking searches and existing views.

## Migration rule

For each note, map legacy tags to the closest Arabic domain, content-type, or status tag. Preserve the old tag until the replacement is verified in searches, indexes, and Base views. Do not add a second tag merely because a note has moved folders.

## Next audit

Review remaining legacy tags after the moved content and new indexes have been used for one migration cycle. Record every mapping before changing it.
