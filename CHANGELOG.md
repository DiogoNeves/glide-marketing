# Changelog

Notable changes to Glide Marketing.

## 2026-06-25

### Added Weekly Glide Update Checks

- Added `glide-check-for-updates`, `Glide HQ/Glide Updates.md`, a weekly update-check automation prompt, and harness adapter prompts.
- Added update-state and migration guidance so installed workspaces can track the last seen upstream release and preserve local instructions.

### Added Nightly Marketing Research Review

- Added a quiet 4am marketing research and memory maintenance skill, checklist, automation prompt, and rolling 4-day audit.
- Updated automation adapters to include the nightly review and keep scheduled prompts minimal.

## 2026-06-20

### Capped Daily Marketing Output

- Updated daily marketing check-ins to prefer one item, allow up to three only when each is urgent or very important, and ask before continuing when more may matter.
- Added daily ranking and source-arbitration rules for competing signals.
- Added evals as read-only drift-review evidence when present.

## 2026-06-17

### Added Marketing Harness Evals

- Added setup, daily signal, content drafting, and research-to-skill evaluation scenarios.
- Added optional external skill-pack guidance.
- Tightened daily output quality and source/content setup questions.

### Simplified Marketing Setup

- Refocused setup on source access, existing content, daily signals, marketing research, content drafting, and drift review.
- Added `Source Map.md` and `Content Library.md`.
- Added utility skills for drafting from existing content and creating marketing-specific skills from researched processes.
- Reduced starter automations to daily check-in and drift review.

### Hardened Daily And Ledger Rules

- Added stronger daily preflight and approval-boundary checks.
- Expanded the follow-through ledger schema with priority, next action, status, and escalation rules.
- Tightened daily, follow-through, and drift reviews around ledger updates and minimal scheduled prompts.

### Clarified Marketing Posting Approval

- Made explicit that marketing material must not be posted without user approval.

### Tightened Daily Automation Prompts

- Made daily scheduled prompts minimal and skill-driven.
- Added instructions to edit installed skills/checklists for daily behavior changes.
- Clarified that user-requested daily-check changes should be committed in the installed workspace git repo.

### Added First Five Daily Direction Loop

- Made current pain, goals, and operating process part of setup.
- Updated daily check-ins to ask for direction during the first five days.
- Kept daily updates brief while offering small options to explore more.

### Added Daily Watchlist Setup

- Added `Daily Watchlist.md` for what users want checked daily.
- Updated installation to ask for daily checks and work through needed access.
- Updated daily check-ins to maintain watchlist, access gaps, and follow-through ledger updates.

### Initial Marketing Version

- Created Glide Marketing from the Glide marketing base.
- Added marketing-specific context, skills, checklists, automations, and adapters.
- Added first-week daily calibration, connector inventory, follow-through ledger, drift review, and human approval boundaries.
