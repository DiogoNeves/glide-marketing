# Automation Registry

Proposed and active Glide automations.

Glide itself does not run automations. The selected harness decides whether automations are supported and how they are configured.

Scheduled prompts should stay minimal and call the installed skill. Update skills, checklists, watchlists, or context files when behavior changes.

| Name | Status | Cadence | Scope | Skill | Output | Last Review |
| --- | --- | --- | --- | --- | --- | --- |
| [[Automations/Daily Marketing Check-In]] | Proposed | Daily or weekdays | Source map, content library, marketing context, daily watchlist, follow-through ledger, configured sources | `glide-daily-marketing-check-in` | Prefer one useful item; max three urgent or very important items | |
| [[Automations/Marketing Drift Review]] | Proposed | Weekly | Operating files, checklists, skills, evals if present, approval boundaries, scheduled prompts | `glide-marketing-drift-review` | Drift report or small non-behavioral corrections | |
| [[Automations/Nightly Marketing Research Review]] | Proposed | Daily at 4am | Recent exchanges, marketing open loops, source/content gaps, open research, daily watchlist signal, evals, stale working-memory candidates, and concise process improvements | `glide-nightly-marketing-research-review` | Internal Glide HQ updates and rolling 4-day audit; approval requests only when needed | |
| [[Automations/Weekly Glide Update Check]] | Proposed | Weekly | Upstream releases, migration notes, local instructions, installed skills, checklists, and automation notes | `glide-check-for-updates` | Quiet no-op when current; update plan or approval request when a new release exists | |

Do not enable automations without user confirmation.
