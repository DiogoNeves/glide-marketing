# Glide Marketing

Glide Marketing is a small Markdown kit for giving an AI agent useful marketing context.

It helps an agent understand your existing sources, track the signals you care about, research marketing questions, and draft content from material you already have.

Glide Marketing is not an app or SaaS. It is a public set of Markdown templates, skills, checklists, and automation prompts that works with Codex, Claude Code, or another agent harness. Your harness is the execution layer; Glide defines the operating behavior.

## Why It Exists

Marketing work gets noisy quickly: sources live everywhere, useful signal is easy to miss, and content work gets worse when the agent does not know what already exists.

Glide Marketing gives the agent a simple base: source map, marketing context, daily watchlist, follow-through ledger, research notes, and utility skills. It can read and draft when access is configured, but it must ask before posting marketing material, sending, changing campaigns, publishing, purchasing, scheduling, approving, or making commitments.

## A Small Example

A founder asks: "Turn my last three posts and customer notes into a launch email draft."

Glide checks the source map, uses the content library, applies the current positioning, drafts from existing material, and points out what still needs approval or better source context.

## How It Works

- `Glide HQ/` is the agent-owned marketing operating workspace.
- `Source Map.md` tells the agent what it can read and how.
- `Content Library.md` records the user's existing content sources.
- `Company Context.md` captures product, market, business model, strategy, and constraints.
- `Marketing Context.md` captures positioning, audience, customer language, channels, and metrics.
- `Marketing Lead Brief.md` captures working preferences, approval boundaries, and calibration.
- `Daily Watchlist.md` tracks the signals the user wants checked.
- `Follow-Through Ledger.md` keeps important marketing loops from disappearing.
- Skills are utilities for setup, daily updates, research, content drafting, and creating new marketing-specific skills.
- Automations are optional; start with daily check-in and drift review.

Glide keeps its internal memory and working structure in `Glide HQ/`. It can read company docs, repos, tools, and external sources when allowed, but it should not modify external systems without explicit approval.

During setup and the first few daily check-ins, Glide tries to understand the current pain, goals, process, and access needed to make the daily loop genuinely useful.

## Included

- `templates/Glide HQ/`: installable marketing operating workspace.
- `skills/`: portable Agent Skills prefixed with `glide-`.
- `automations/`: starter automation prompts, including a quiet 4am research review.
- `adapters/`: Codex, Claude Code, and generic harness snippets.
- `docs/`: concept, privacy, harness, optional skill-pack, and release checks.
- `examples/`: short examples and lightweight eval scenarios.

## Install

Open the target Markdown workspace, marketing repo, company repo, or shared docs folder in your agent harness, then ask the harness to follow [INSTALL.md](INSTALL.md).

The installer should inspect before writing, ask which harness to use, ask where existing marketing sources and content live, draft the first context, and set up a useful daily check.

## Privacy

Glide Marketing itself does not collect telemetry, run servers, transmit data, or store user data anywhere. It is Markdown structure and instructions.

Privacy depends on the selected harness, model provider, connectors, sync, Git hosting, and automation setup. Review those policies before giving tools access to sensitive company or customer data.

See [docs/PRIVACY.md](docs/PRIVACY.md).

## Inspiration

Glide Marketing is inspired by [Marketing Skills](https://github.com/coreyhaines31/marketingskills), especially the idea that one canonical context document should feed many specialized skills. Glide Marketing keeps that pattern while adding self-evolving operating memory, follow-through, drift review, and approval boundaries.
