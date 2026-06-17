---
name: glide-daily-marketing-check-in
description: Run a concise daily marketing check-in. Use for morning operating reviews, daily automations, checking company priorities, surfacing one risk/opportunity/question, reviewing follow-through, or scanning configured connectors for important business signal.
---

# Glide Daily Marketing Check-In

## Load

- `Glide HQ/AGENTS.md`
- `Glide HQ/Company Context.md`
- `Glide HQ/Marketing Context.md`
- `Glide HQ/Marketing Lead Brief.md`
- `Glide HQ/Source Map.md`
- `Glide HQ/Content Library.md`
- `Glide HQ/Daily Watchlist.md`
- `Glide HQ/Connector Inventory.md`
- `Glide HQ/Checklists/Daily Marketing Check-In.md`
- `Glide HQ/Follow-Through Ledger.md`
- `Glide HQ/Decision Log.md`
- `Glide HQ/Questions Queue.md`
- `Glide HQ/Contradiction Register.md`
- Configured connectors when safe and useful

## Process

1. Confirm the approval boundary from `AGENTS.md` and `Marketing Lead Brief.md`; do not post marketing material or change external systems without approval.
2. Run `$glide-update-marketing-context` when recent durable signal should shape the check-in.
3. Scan `Daily Watchlist.md`, priorities, follow-through, decisions, questions, and contradictions.
4. Review `Follow-Through Ledger.md` for due, stale, high-stakes, or newly actionable items.
5. Fetch from configured connectors only when the watchlist or current context makes it useful.
6. Choose the smallest useful output.
7. During the first five daily check-ins, ask one useful direction question unless the user opts out. Focus on current pain, goals, process, missing access, signal quality, timing, tone, length, or preferred action level.
8. Draft external actions only for approval.
9. Keep the update brief, and offer one or two optional paths to explore more when there is a useful deeper thread.
10. Update Glide HQ as the conversation progresses, including durable calibration preferences, watchlist changes, access gaps, and ledger updates.

## Automation Contract

- Keep the scheduled automation prompt minimal; it should only call this installed skill for the workspace.
- Do not duplicate the daily process inside the scheduler.
- When the user asks to change daily behavior, update the installed skill, checklist, watchlist, or Glide HQ context in the workspace.
- Commit user-requested daily-check behavior changes to the git repo in the installed workspace with a brief commit message.

## Output

- One concise question, risk, opportunity, contradiction, follow-through nudge, or short bundle.
- One direction question during each of the first five daily check-ins unless the user opts out.
- Optional suggestions for deeper exploration, kept brief.
- Daily watchlist and follow-through ledger updates when useful.

## Quality Bar

- Lead with the useful signal or question.
- Keep the default update under five short bullets.
- Do not mention quiet ledger items.
- Mention access gaps only when they block a useful check or need user action.
- Never present drafts as sent, posted, approved, or scheduled.
