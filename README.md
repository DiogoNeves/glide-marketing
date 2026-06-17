# Glide Marketing

Glide Marketing is a Markdown operating system for marketing teams, marketing leads, and growth operators.

It gives an AI agent a durable home for marketing context, positioning, customer language, GTM plans, channel work, experiments, decisions, research, and follow-through. The point is simple: stop repeating context, make better marketing decisions, and keep useful work moving without turning marketing into more admin.

Glide Marketing is not an app or SaaS. It is a public set of Markdown templates, skills, checklists, and automation prompts that works with Codex, Claude Code, or another agent harness. Your harness is the execution layer; Glide defines the operating behavior.

## Why It Exists

Marketing work gets noisy quickly: positioning, ICP, campaigns, channels, analytics, customer research, content, launches, sales enablement, and half-finished experiments all compete for attention.

Glide Marketing turns that into an agent-readable operating layer. The agent can read, research, synthesize, challenge, draft, and maintain context over time. It can fetch information when access is configured, but it should ask before posting, sending, changing campaigns, publishing, purchasing, scheduling, approving, or making commitments.

## A Small Example

A marketing lead asks: "What should we do about our weak activation?"

Glide loads company context, marketing context, GTM, analytics, lifecycle, customer research, decisions, contradictions, and follow-through. It gives a direct read, names the missing evidence, suggests the next experiment or customer check, and updates the right Markdown files as the conversation progresses.

## How It Works

- `Glide HQ/` is the agent-owned marketing operating workspace.
- `Company Context.md` captures product, market, business model, strategy, and constraints.
- `Marketing Context.md` captures positioning, ICP, messaging, channels, funnel, metrics, customer language, and active experiments.
- `Marketing Lead Brief.md` captures working preferences, approval boundaries, and calibration.
- Areas cover Strategy, Positioning, Customer Research, GTM, Content, SEO, Paid, Lifecycle, Analytics, Website CRO, Sales Enablement, and Partnerships.
- Skills and checklists encode repeatable marketing workflows.
- Automations are optional prompts for daily, weekly, follow-through, and drift reviews.
- Connectors are discovered from the user's harness during setup; Glide records what is actually available and how it may be used safely.

Glide keeps its internal memory and working structure in `Glide HQ/`. It can read company docs, repos, tools, and external sources when allowed, but it should not modify external systems without explicit approval.

During setup and the first few daily check-ins, Glide tries to understand the current pain, goals, process, and access needed to make the daily loop genuinely useful.

## Included

- `templates/Glide HQ/`: installable marketing operating workspace.
- `skills/`: portable Agent Skills prefixed with `glide-`.
- `automations/`: starter automation prompts.
- `adapters/`: Codex, Claude Code, and generic harness snippets.
- `docs/`: concept, privacy, harness, and release checks.
- `examples/`: short examples for common marketing workflows.

## Install

Open the target Markdown workspace, marketing repo, company repo, or shared docs folder in your agent harness, then ask the harness to follow [INSTALL.md](INSTALL.md).

The installer should inspect before writing, ask which harness to use, draft marketing context from existing materials when possible, then ask focused questions to correct and fill gaps.

## Privacy

Glide Marketing itself does not collect telemetry, run servers, transmit data, or store user data anywhere. It is Markdown structure and instructions.

Privacy depends on the selected harness, model provider, connectors, sync, Git hosting, and automation setup. Review those policies before giving tools access to sensitive company or customer data.

See [docs/PRIVACY.md](docs/PRIVACY.md).

## Inspiration

Glide Marketing is inspired by [Marketing Skills](https://github.com/coreyhaines31/marketingskills), especially the idea that one canonical context document should feed many specialized skills. Glide Marketing keeps that pattern while adding self-evolving operating memory, follow-through, drift review, and approval boundaries.
