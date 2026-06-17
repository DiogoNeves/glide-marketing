---
name: glide-marketing-drift-review
description: Review Glide operating files for drift against Harness Design Principles.md. Use for scheduled drift reviews, behavior audits, approval-boundary checks, and simplifying verbose instructions without changing behavior.
---

# Glide Marketing Drift Review

## Load

- `Glide HQ/Harness Design Principles.md`
- `Glide HQ/Checklists/Marketing Drift Review.md`
- Operational files listed in the checklist
- Installed `glide-*` skills

## Process

1. Treat `Harness Design Principles.md` as read-only unless the user explicitly asks to edit it.
2. Review operating files for drift.
3. Fix only clear non-behavioral issues directly.
4. Reduce verbosity when clarity and behavior survive.
5. Ask before behavior-changing edits.
6. Preserve human-approval boundaries for external actions.
7. Preserve minimal scheduled prompts; daily behavior should live in skills, checklists, watchlist, and ledger.
8. Confirm the follow-through ledger still has enough structure to protect commitments without becoming a task manager.

## Output

- Drift found or not found.
- Files changed.
- Verbosity reductions.
- Approval-needed recommendations.
