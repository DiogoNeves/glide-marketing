# Install Glide

This file is written for an agent harness to execute, but it is readable by a human.

## Human Summary

The installer should:

1. Start from the root of the target Markdown workspace, company repo, or shared docs folder.
2. Inspect existing files without changing anything.
3. Ask which harness is being used: Codex, Claude Code, other, or manual.
4. Ask where existing marketing sources and content live.
5. Draft the source map, content library, company context, and marketing context.
6. Ask what signals the user wants checked daily.
7. Work with the user to confirm Glide has read access to the sources needed.
8. Copy `Glide HQ/` and selected skills only after confirmation.
9. Create or update the root harness instruction file.
10. Inspect available harness connectors and record what is actually connected.
11. Initialize git if the workspace is not already a repository.
12. Offer starter automations after explicit confirmation, using minimal schedule prompts that call installed Glide skills.

Glide defines behavior. The harness decides where computation happens and what data is sent.

## Installer Contract

- Install from the workspace root, not a nested folder.
- Do not change files during inspection.
- Do not overwrite existing files without explicit confirmation.
- Do not install automations without explicit confirmation.
- Reading and fetching information is allowed when access is configured.
- Posting marketing material, sending, publishing, scheduling, purchasing, approving, deleting, changing external systems, or making commitments requires explicit human approval.

## Step 1: Inspect

Inspect only. Check for:

- existing `Glide HQ/`
- `.agents/skills/`
- `.claude/skills/`
- `AGENTS.md`
- `CLAUDE.md`
- `.git/`
- existing company docs, product docs, strategy notes, customer notes, website copy, blog posts, newsletters, social posts, videos, transcripts, sales docs, metrics docs, and decision records
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

## Step 3: Map Sources And Existing Content

Prefer draft-then-ask.

Ask the user where useful marketing source material lives:

- website,
- blog or newsletter,
- social posts,
- videos, podcasts, or transcripts,
- customer calls, support tickets, reviews, testimonials, or sales notes,
- analytics, search, CRM, email, ads, or product data,
- launch plans, positioning docs, decks, or strategy notes,
- existing content drafts or idea backlog.

Then draft:

- `Glide HQ/Source Map.md`
- `Glide HQ/Content Library.md`
- `Glide HQ/Company Context.md`
- `Glide HQ/Marketing Context.md`
- `Glide HQ/Marketing Lead Brief.md`

Then ask:

- Which sources matter most?
- Which sources are off-limits?
- Which existing content should Glide learn from first?
- What marketing outcome should daily updates support?
- What is wrong, missing, or uncertain in the draft context?

Do not turn missing fields into homework. Ask only the questions that materially improve early recommendations or daily operation.

## Step 4: Define Daily Checks And Access

Ask the user what they want Glide Marketing to check daily.

Examples:

- campaign performance,
- new leads or pipeline movement,
- customer replies or support signal,
- content ideas or reuse opportunities,
- newsletter, blog, social, video, or community signal,
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
6. Confirm what should happen when the check finds something: ignore, mention, draft, add to ledger, or ask for approval.

During the first five daily check-ins, ask for more direction each day unless the user opts out. Use the answers to refine pain, goals, process, watchlist, connector access, communication preferences, and ledger behavior.

## Step 5: Optional Skill Packs

Do not install external marketing skill packs by default.

If the user wants specialized marketing workflows, offer to inspect an external skill pack or existing internal process, then use `glide-create-marketing-skill` to create only the small utility skill they need. See `docs/OPTIONAL_SKILL_PACKS.md`.

Good candidates:

- content repurposing,
- customer research synthesis,
- newsletter review,
- SEO/content brief review,
- competitor monitoring,
- launch checklist,
- social post drafting from existing content.

## Step 6: Install

After confirmation:

1. Copy `templates/Glide HQ/` into the workspace.
2. Copy selected `skills/glide-*` folders into the harness skill directory.
3. Create or update the root harness instruction file with the relevant adapter snippet.
4. Record installed skills and proposed automations in `Glide HQ/Automation Registry.md`.
5. Create or update `Glide HQ/Connector Inventory.md` from the connectors actually visible to the harness.
6. Create or update `Glide HQ/Source Map.md` and `Glide HQ/Content Library.md`.
7. Create or update `Glide HQ/Daily Watchlist.md` from the user's desired signals.
8. Confirm `Glide HQ/Follow-Through Ledger.md` has a clear first set of watched commitments or is intentionally empty.
9. If the workspace is not already a git repository, run `git init` after confirmation.
10. Add the Glide root instruction section telling agents to keep useful content and harness updates committed with very short commit messages.
11. Keep scheduled automation prompts minimal; detailed behavior belongs in installed Glide skills and checklists.

## Step 7: Offer Starter Automations

Offer only:

- Daily Marketing Check-In
- Marketing Drift Review
- Nightly Marketing Research Review

Confirm before enabling any automation. If the harness does not support automations, keep the prompts as proposed manual automations in `Glide HQ/Automations/`.

For daily checks, the schedule prompt should only call the installed daily skill, such as:

```text
Run the installed glide-daily-marketing-check-in skill for this workspace.
```

Do not duplicate daily behavior inside the scheduler. When the user asks to change daily checks, update the installed skill, checklist, watchlist, or Glide HQ context in the workspace, then commit those changes to the user's git repository in that folder.

For nightly research reviews, the schedule prompt should only call the installed nightly research skill.

## Step 8: Git Hygiene

If the workspace has no git repository, initialize one after installation confirmation.

Root harness instructions should say:

- Keep meaningful Glide content, context, checklist, skill, automation, and harness updates committed.
- Use very brief commit messages, such as `Update source map`, `Add content source`, `Refresh follow-through`, or `Tighten harness rules`.
- Commit user-requested daily-check behavior changes in the installed workspace git repo.
- Do not commit secrets, credentials, private exports, raw transcripts, or connector data dumps.
- Do not push unless the user or workspace policy says to push.

## Step 9: Connector Inventory

Assume Codex or Claude Code may already have useful connectors, but do not rely on a static registry.

During setup:

1. Inspect the harness-provided tools, MCP servers, apps, plugins, or connector list.
2. Record only what is actually connected in `Glide HQ/Connector Inventory.md`.
3. Ask the user before installing or enabling anything new.
4. Use available connectors for read/fetch workflows when access is granted.
5. For write or external-state changes, draft the action and ask for approval first.
