# Install Glide

This file is written for an agent harness to execute, but it is readable by a human.

## Human Summary

The installer should:

1. Start from the root of the target Markdown workspace, company repo, or shared docs folder.
2. Inspect existing files without changing anything.
3. Ask which harness is being used: Codex, Claude Code, other, or manual.
4. Draft company and marketing context from existing materials when possible.
5. Ask what the user wants checked daily.
6. Work with the user to confirm Glide has access to the needed context and connectors.
7. Ask focused questions to correct or fill the context.
8. Copy `Glide HQ/` and selected skills only after confirmation.
9. Create or update the root harness instruction file.
10. Inspect available harness connectors and record what is actually connected.
11. Initialize git if the workspace is not already a repository.
12. Offer starter automations after explicit confirmation.

Glide defines behavior. The harness decides where computation happens and what data is sent.

## Installer Contract

- Install from the workspace root, not a nested folder.
- Do not change files during inspection.
- Do not overwrite existing files without explicit confirmation.
- Do not install automations without explicit confirmation.
- Reading and fetching information is allowed when access is configured.
- Posting, sending, publishing, scheduling, purchasing, approving, deleting, changing external systems, or making commitments requires explicit human approval.

## Step 1: Inspect

Inspect only. Check for:

- existing `Glide HQ/`
- `.agents/skills/`
- `.claude/skills/`
- `AGENTS.md`
- `CLAUDE.md`
- `.git/`
- existing company docs, README files, product docs, strategy notes, customer notes, investor updates, pitch decks, metrics docs, and decision records
- configured connector docs, active connector/tool lists, MCP/app tools, or automation notes

Summarize what exists and what Glide would need to create or update.

If `Glide HQ/` already exists, stop and ask whether to merge carefully, install elsewhere, install only skills, or cancel.

## Step 2: Choose Harness

Recommended mappings:

| Harness | Root instruction file | Skill directory |
| --- | --- | --- |
| Codex | `AGENTS.md` | `.agents/skills/` |
| Claude Code | `CLAUDE.md` | `.claude/skills/` |
| Other/manual | ask the user | ask the user |

Create the root instruction file if missing. If it exists, append or update a clearly marked Glide section and leave unrelated instructions intact.

## Step 3: Draft Company And Marketing Context

Prefer draft-then-ask.

Read available materials and draft:

- `Glide HQ/Company Context.md`
- `Glide HQ/Marketing Context.md`
- `Glide HQ/Marketing Lead Brief.md`

Then ask:

- What is wrong?
- What is missing?
- What is uncertain?
- What should marketing optimize for right now?

Do not turn missing fields into homework. Ask only the questions that materially improve early recommendations.

## Step 4: Define Daily Checks And Access

Ask the user what they want Glide Marketing to check daily.

Examples:

- campaign performance,
- new leads or pipeline movement,
- customer replies or support signal,
- SEO/search changes,
- analytics anomalies,
- content or launch follow-through,
- open decisions,
- stale promises or waiting threads,
- competitor or market changes.

For each requested check:

1. Record it in `Glide HQ/Daily Watchlist.md`.
2. Identify the needed source, file, connector, or manual input.
3. Check whether the harness already has read/fetch access.
4. If access is missing, record the gap and ask how the user wants to provide it.
5. Add any important ongoing commitment to `Follow-Through Ledger.md`.

## Step 5: Install

After confirmation:

1. Copy `templates/Glide HQ/` into the workspace.
2. Copy selected `skills/glide-*` folders into the harness skill directory.
3. Create or update the root harness instruction file with the relevant adapter snippet.
4. Record installed skills and proposed automations in `Glide HQ/Automation Registry.md`.
5. Create or update `Glide HQ/Connector Inventory.md` from the connectors actually visible to the harness.
6. Create or update `Glide HQ/Daily Watchlist.md` from the user's desired daily checks.
7. If the workspace is not already a git repository, run `git init` after confirmation.
8. Add the Glide root instruction section telling agents to keep useful content and harness updates committed with very short commit messages.

## Step 6: Offer Starter Automations

Offer only:

- Daily Marketing Check-In
- Weekly Marketing Review
- Follow-Through Review
- Marketing Drift Review

Confirm before enabling any automation. If the harness does not support automations, keep the prompts as proposed manual automations in `Glide HQ/Automations/`.

## Step 7: Git Hygiene

If the workspace has no git repository, initialize one after installation confirmation.

Root harness instructions should say:

- Keep meaningful Glide content, context, checklist, skill, automation, and harness updates committed.
- Use very brief commit messages, such as `Update company context`, `Add GTM question`, `Refresh follow-through`, or `Tighten harness rules`.
- Do not commit secrets, credentials, private exports, raw transcripts, or connector data dumps.
- Do not push unless the user or workspace policy says to push.

## Step 8: Connector Inventory

Assume Codex or Claude Code may already have useful connectors, but do not rely on a static registry.

During setup:

1. Inspect the harness-provided tools, MCP servers, apps, plugins, or connector list.
2. Record only what is actually connected in `Glide HQ/Connector Inventory.md`.
3. Ask the user before installing or enabling anything new.
4. Use available connectors for read/fetch workflows when access is granted.
5. For write or external-state changes, draft the action and ask for approval first.
