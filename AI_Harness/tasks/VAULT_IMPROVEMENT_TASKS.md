# Vault Improvement Task List

This list converts the read-only Vault audit recommendations into actionable tasks. These tasks do not authorize edits to existing knowledge notes. Each task requires review of the target files and explicit approval before modifying existing knowledge.

## Status values

- `Pending`: identified but not started.
- `In Progress`: actively being worked on with approved scope.
- `Blocked`: cannot continue without a decision, source, or approval.
- `Completed`: implemented and verified.

## Priority 1 — Integrity and safety

- [ ] **IMPROVEMENT-001 — Repair and disambiguate internal links**  
  Status: `Pending`  
  Targets: index notes under `برمجة/`, `علمًا نافعًا/`, and `عقل ثاني/`  
  Actions: audit wikilinks, replace incorrect paths, make duplicate targets explicit, and verify image, PDF, Base, and Canvas references.  
  Approval: required before editing existing notes.

- [ ] **IMPROVEMENT-002 — Protect and structure sensitive financial notes**  
  Status: `Pending`  
  Targets: `المال والرزق/المديونيات.md`, `المال والرزق/حل.md`  
  Actions: add privacy guidance, separate current financial data from repayment strategy, add update dates and currency fields, and verify calculations.  
  Approval: required before editing existing notes.

- [ ] **IMPROVEMENT-003 — Review security-sensitive AI instructions**  
  Status: `Pending`  
  Targets: AI tool setup and privacy notes under `برمجة/وكلاء الذكاء الاصطناعي/`  
  Actions: add sources and verification dates, remove or clearly label default credentials, redact secrets if present, and separate historical notes from current instructions.  
  Approval: required before editing existing notes.

## Priority 2 — Structure and metadata

- [ ] **IMPROVEMENT-004 — Standardize library metadata**  
  Status: `In Progress`  
  Targets: `علمًا نافعًا/المكتبة/سجل المكتبة/`  
  Actions: standardize YAML fields for status, type, rating, author, age, and tags; normalize status values; complete missing fields; and preserve the existing Arabic filenames.

- [ ] **IMPROVEMENT-005 — Standardize course metadata and progress tracking**  
  Status: `Pending`  
  Targets: `علمًا نافعًا/كورسات/`  
  Actions: define consistent course fields, fix incomplete properties, remove blank checklist entries, and separate course status from the list of possible statuses.

- [ ] **IMPROVEMENT-006 — Replace empty notes with intentional states**  
  Status: `In Progress`  
  Targets: all empty Markdown notes identified by the audit  
  Actions: fill, convert to a documented template, archive, or retain intentionally after review; do not delete automatically.

- [x] **IMPROVEMENT-007 — Improve indexes and navigation pages**  
  Status: `Completed`  
  Targets: root index notes such as `برمجة.md`, `عقل ثاني.md`, `علمًا نافعًا.md`, and `المال والرزق.md`  
  Actions: add missing sections, repair stale links, document folder purpose, and add clear next-step navigation.

## Priority 3 — Content quality

- [ ] **IMPROVEMENT-008 — Split the large Python reference note**  
  Status: `Pending`  
  Target: `برمجة/المكتبة البرمجية/Python 1/Python.md`  
  Actions: split the monolithic note into modular lessons and projects, create a navigation index, preserve examples, and review code examples without executing untrusted content automatically.

- [ ] **IMPROVEMENT-009 — Review Python examples for correctness**  
  Status: `Pending`  
  Target: the split Python lesson notes  
  Actions: identify inconsistent variable names, spelling errors in code values, incomplete asynchronous examples, and missing explanations; validate examples in a controlled environment only after approval.

- [ ] **IMPROVEMENT-010 — Separate daily tasks from knowledge indexes**  
  Status: `Pending`  
  Target: `اغتنم وقتك.md`  
  Actions: keep the page as a dashboard, move actionable work into a structured task system, and add status, priority, area, and due-date fields.

- [ ] **IMPROVEMENT-011 — Add evidence and review dates to changing technical notes**  
  Status: `Pending`  
  Targets: hardware, local-model, pricing, and tool recommendation notes  
  Actions: add source, last-verified date, confidence, assumptions, and an expiry or review reminder for volatile claims.

- [ ] **IMPROVEMENT-012 — Improve opinion and essay notes**  
  Status: `Pending`  
  Targets: notes under `عقل ثاني/وجهات نظر/`  
  Actions: distinguish personal opinion from evidence, add counterarguments and sources, clarify definitions, and reduce broad or judgmental claims while preserving the author’s viewpoint.

- [ ] **IMPROVEMENT-013 — Make the educational-agent plan measurable**  
  Status: `Pending`  
  Target: the educational AI architecture note under `برمجة/وكلاء الذكاء الاصطناعي/`  
  Actions: replace unsupported absolute targets with a test set, metric definitions, error categories, acceptance thresholds, and versioned evaluation results.

## Priority 4 — Attachments and maintenance

- [ ] **IMPROVEMENT-014 — Review unclassified attachments**  
  Status: `Pending`  
  Targets: images, the PDF, Base files, and Canvas files found during the audit  
  Actions: verify that each attachment is intentionally referenced, add descriptive context where useful, and document orphaned or obsolete attachments before any cleanup.

- [ ] **IMPROVEMENT-015 — Establish a recurring review cycle**  
  Status: `Pending`  
  Scope: improved notes after implementation  
  Actions: review financial and technical notes regularly, check broken links, validate course progress, and record changes in the Harness logs.

## Recommended execution order

1. `IMPROVEMENT-001` — link integrity.
2. `IMPROVEMENT-002` and `IMPROVEMENT-003` — privacy and security.
3. `IMPROVEMENT-004` through `IMPROVEMENT-007` — metadata and navigation.
4. `IMPROVEMENT-008` through `IMPROVEMENT-013` — content improvement.
5. `IMPROVEMENT-014` and `IMPROVEMENT-015` — attachments and maintenance.
