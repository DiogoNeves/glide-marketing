# Daily Marketing Check-In

Purpose: run a concise daily pass that improves company context, surfaces one useful signal, and protects follow-through.

## Load

- `Glide HQ/AGENTS.md`
- `Company Context.md`
- `Marketing Context.md`
- `Marketing Lead Brief.md`
- `Daily Watchlist.md`
- `Connector Inventory.md`
- `Follow-Through Ledger.md`
- `Decision Log.md`
- `Questions Queue.md`
- `Contradiction Register.md`
- Configured connectors when safe and useful

## Morning Pass

Check:

- approval boundaries,
- active marketing priorities,
- daily watchlist checks,
- follow-through ledger due/stale/high-stakes items,
- open decisions,
- high-impact questions,
- contradictions,
- calendar, email, CRM, analytics, product, project, or support sources when configured.

## Output

Surface the smallest useful item:

- one question,
- one risk,
- one opportunity,
- one contradiction,
- one follow-through nudge,
- one small approved-safe action suggestion,
- or a short bundle when genuinely useful.

Keep it conversational. Do not make it feel like homework.

## Daily Output Contract

- Lead with the useful signal or question.
- Keep the default update under five short bullets.
- Mention source/access gaps only when they block a useful check or need user action.
- Include approval-needed drafts only as drafts.
- End with one small optional path when deeper work would help.

When there is more to unpack, add a brief invitation with one or two useful directions, such as checking the evidence, turning it into an experiment, reviewing access, or updating the watchlist.

## Watchlist And Ledger

- Use `Daily Watchlist.md` as the default source for what to check.
- If a requested check cannot run because context or connector access is missing, surface the gap only when it blocks a useful update or needs user action.
- Update `Follow-Through Ledger.md` when a daily check creates, clarifies, advances, closes, or stops needing attention.
- Do not mention quiet ledger items unless they are due, stale, high-stakes, newly actionable, or useful for today's decision.
- Add new daily-check preferences to `Daily Watchlist.md` as the user gives guidance.

## Scheduled Prompt

- Keep the daily schedule prompt minimal. It should call the installed `glide-daily-marketing-check-in` skill for this workspace.
- Do not copy this checklist into the scheduler.
- When the user asks to change daily behavior, update the installed skill, this checklist, `Daily Watchlist.md`, or the relevant Glide HQ context.
- Commit those user-requested daily-check changes to the workspace git repo with a brief message.

## First Five Check-Ins

During the first five daily check-ins, ask for more direction so Glide learns the user's pain, goals, process, and daily operating needs.

- Ask one direction question per day unless the user opts out.
- Ask about current pain, goals, process, signal, noise, timing, tone, length, missing context, missing access, or preferred action level.
- Keep the main update short before asking.
- Capture durable preferences in `Marketing Lead Brief.md` or `Communication Preferences.md`.
- Use calibration answers to refine `Daily Watchlist.md` and ledger behavior.

## Guardrails

- Reading and fetching is allowed when access is configured.
- Drafting is allowed.
- Ask before posting marketing material, sending, scheduling, changing tools, approving, purchasing, deleting, publishing, or committing the company.
