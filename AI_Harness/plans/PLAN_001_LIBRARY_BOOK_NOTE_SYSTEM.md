---
plan_number: 001
title: Library Book Note System
status: Draft
created: 2026-10-28
scope: Existing library notes under the current Obsidian Vault
approval_required: true
---

# خطة نظام ملاحظات الكتب في المكتبة

## الفكرة الأساسية

تكون لكل كتاب ملاحظة رئيسية واحدة، سواء كان مخططًا لقراءته أو قيد القراءة أو مكتملًا. لا نعيد تسمية المجلدات العربية ولا ننقل الملاحظات الحالية. نبدأ بقالب موحد للكتب الجديدة، ثم نرحّل الملاحظات القديمة تدريجيًا بعد الموافقة.

يفصل قالب الكتاب بين أربعة أنواع من المحتوى:

1. **ملخص الغلاف**: نص ظهر الكتاب أو وصف الناشر، مع مصدره بوضوح.
2. **الملخص السريع**: ملخصك الشخصي في 3–7 جمل.
3. **الأفكار المحورية**: شرح أهم الأفكار والحجج والأمثلة مع الفصل أو الصفحة.
4. **الاقتباسات المهمة**: جمل قصيرة مع الصفحة أو الفصل وسبب أهميتها.

## دورة حياة الكتاب

- `Planned`: مخطط لقراءته.
- `Reading`: قيد القراءة.
- `Completed`: تمت قراءته وتلخيصه.
- `Paused`: متوقف مؤقتًا.
- `Abandoned`: أُوقف مع تسجيل السبب.

المسار الطبيعي هو: `Planned → Reading → Completed`.

## النموذج المقترح لكل كتاب

```markdown
---
title: "Book Title"
author: "Author Name"
status: Planned
type: Book
category: "Category"
series: "Series name or none"
rating:
started:
completed:
source:
tags:
  - library
---

# Book Title

## Quick Metadata

- Author:
- Category:
- Status:
- Source:
- Why I chose this book:

## Back-cover Summary

> Publisher or back-cover summary.

Source:

## Quick Summary

Write a short personal summary in 3–7 sentences.

## Central Ideas

### Idea 1 — Title

- Claim:
- Explanation:
- Example:
- Chapter or page:
- My interpretation:

## Important Quotes

> Short quote.

- Page or chapter:
- Why it matters:

## Personal Takeaways

- What changed in my understanding?
- What do I agree or disagree with?
- What should I test in real life?

## Action Items

- [ ] Action derived from the book

## Related Notes

- [[Related note]]

## Review

- Rating:
- What was useful:
- What was weak or unclear:
- Who should read it:
- Would I recommend it?

## Reading Log

- Date:
- Progress:
- Notes:
```

## إضافات مقترحة

- لا تخلط ملخص الغلاف بملخصك؛ ملخص الغلاف تسويقي وقد لا يكون محايدًا.
- افصل الاقتباس عن تحليلك، وأضف رقم الصفحة أو الفصل عند الإمكان.
- أضف نتيجة عملية أو سؤالًا تركه الكتاب لديك.
- أعد مراجعة الملاحظة بعد أسبوع أو شهر لتمييز الأثر المستمر من الانطباع اللحظي.
- استخدم `فهرس المكتبة.md` كصفحة تنقل، واعتمد على قاعدة بيانات قابلة للتصفية حسب الحالة والتصنيف والمؤلف والتقييم.

## خطة التنفيذ

### Phase 1 — Confirm the schema

1. Approve the fields and section names in this plan.
2. Decide whether the body is primarily Arabic, English, or mixed.
3. Confirm the rating scale and whether audience or age fields are needed.

### Phase 2 — Create the template

1. Create an English-named book template in an approved template location.
2. Keep the metadata and sections consistent.
3. Add a copyright-aware rule to keep quotations short and cite pages.

### Phase 3 — Prepare the library index

1. Review `علمًا نافعًا/المكتبة/فهرس المكتبة.md`.
2. Repair navigation links without renaming Arabic folders or notes.
3. Improve the existing library database view to show status, category, rating, and author.

### Phase 4 — Pilot migration

1. Select three books: one planned, one completed, and one incomplete.
2. Apply the template only after approval.
3. Preserve existing content and label uncertain material for review.
4. Refine the template before wider migration.

### Phase 5 — Gradual migration

1. Migrate small batches grouped by category.
2. Never delete or overwrite existing summaries.
3. Label whether each summary came from the publisher or the reader.
4. Validate links and database fields after every batch.

### Phase 6 — Reading workflow

1. Create the note with `status: Planned`.
2. Add metadata and the back-cover summary before reading.
3. Change status to `Reading` and keep short reading-log entries.
4. Capture ideas as they emerge instead of copying large passages.
5. On completion, write the quick summary, central ideas, short quotes, takeaways, and actions.
6. Revisit the note later and add a delayed review.

## Acceptance criteria

- Every new book has one main note.
- The four content layers are visibly separated.
- The index filters by status, category, author, and rating.
- The quick summary can be read in under one minute.
- Central ideas include explanations, not only copied sentences.
- Quotes have page or chapter references when available.
- Existing Arabic names and notes are preserved.
- No existing note is overwritten during migration.
- Each migration batch is reviewed before the next batch.

## Approval boundary

This plan proposes a system only. Creating a template, changing the index, configuring database views, or migrating existing book notes requires approval for that specific step.
