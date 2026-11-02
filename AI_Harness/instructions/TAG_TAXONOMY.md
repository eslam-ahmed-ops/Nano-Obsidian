# Arabic Tag Taxonomy

This file defines the controlled vocabulary for new Vault notes. The tag values are Arabic because the knowledge base is Arabic. Harness control files remain English.

## Domain tags

- `مجال/برمجة`
- `مجال/ذكاء_اصطناعي`
- `مجال/بيانات`
- `مجال/تعليم`
- `مجال/كتب`
- `مجال/مشاريع`

## Content-type tags

- `نوع/فهرس`
- `نوع/مرجع`
- `نوع/مفهوم`
- `نوع/كورس`
- `نوع/كتاب`
- `نوع/مشروع`
- `نوع/تجربة`

## Status tags

- `حالة/مسودة`
- `حالة/قيد_التعلم`
- `حالة/مراجعة`
- `حالة/مكتمل`
- `حالة/مؤرشف`

## Rules

1. Use YAML tag arrays for new notes.
2. Use no more than three to five tags per note.
3. Do not duplicate an Arabic tag with an English equivalent.
4. Do not use a tag for data that belongs in a property such as author, date, status, or source.
5. Preserve legacy tags during migration until links, searches, and indexes are verified.
6. Add a new tag only when the existing vocabulary cannot express the note's domain, type, or status.
