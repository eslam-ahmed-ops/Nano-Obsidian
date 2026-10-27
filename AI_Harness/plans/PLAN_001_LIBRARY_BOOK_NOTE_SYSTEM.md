---
plan_number: 001
title: Library Book Note System
status: In Progress
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

### المرحلة الأولى — اعتماد النموذج

1. Approve the fields and section names in this plan.
2. Use Arabic for all new book-note headings and content.
3. Confirm the rating scale and whether audience or age fields are needed.

### المرحلة الثانية — إنشاء القالب

1. إنشاء قالب باسم إنجليزي في مكان معتمد للقوالب.
2. الحفاظ على ثبات الحقول والأقسام.
3. إضافة قاعدة تراعي حقوق النشر وتطلب إبقاء الاقتباسات قصيرة مع ذكر الصفحات.

### المرحلة الثالثة — تجهيز فهرس المكتبة

1. مراجعة `علمًا نافعًا/المكتبة/فهرس المكتبة.md`.
2. إصلاح روابط التنقل دون إعادة تسمية المجلدات أو الملاحظات العربية.
3. تحسين عرض قاعدة بيانات المكتبة لإظهار الحالة والتصنيف والتقييم والمؤلف.

### المرحلة الرابعة — الترحيل التجريبي

1. اختيار ثلاثة كتب: كتاب مخطط، وكتاب مكتمل، وكتاب غير مكتمل.
2. تطبيق القالب بعد الموافقة فقط.
3. الحفاظ على المحتوى الموجود ووضع المواد غير المؤكدة تحت قسم للمراجعة.
4. تحسين القالب قبل الترحيل الأوسع.

### المرحلة الخامسة — الترحيل التدريجي

1. ترحيل دفعات صغيرة مجمعة حسب التصنيف.
2. عدم حذف أو استبدال الملخصات الموجودة.
3. تحديد ما إذا كان كل ملخص من الناشر أو من القارئ.
4. التحقق من الروابط وحقول قاعدة البيانات بعد كل دفعة.

### المرحلة السادسة — سير القراءة

1. إنشاء الملاحظة مع `status: Planned`.
2. إضافة البيانات وملخص الغلاف قبل القراءة.
3. تغيير الحالة إلى `Reading` وتسجيل ملاحظات قصيرة أثناء القراءة.
4. تسجيل الأفكار عند ظهورها بدل نسخ مقاطع طويلة.
5. عند الانتهاء، كتابة الملخص السريع والأفكار المحورية والاقتباسات القصيرة والاستفادة والإجراءات.
6. مراجعة الملاحظة لاحقًا وإضافة مراجعة مؤجلة.

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

## Implementation progress

- The template, library index, and database view are implemented.
- Eighteen identified book notes have the standardized metadata and Arabic structure.
- The empty `Untitled.md` record remains unchanged because its book identity is unknown.
- Summaries, central ideas, and quotations remain explicitly pending when no verified source or reader content was available.
- The plan remains `In Progress` until the remaining unidentified record is resolved and the content sections are filled from reliable sources or the reader's notes.
