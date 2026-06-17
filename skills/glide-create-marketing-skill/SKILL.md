---
name: glide-create-marketing-skill
description: Research a repeatable marketing process and turn it into a concise Glide skill. Use when the user wants a new marketing-specific utility skill for recurring work such as content repurposing, customer research, launch planning, SEO review, newsletter review, competitor monitoring, lifecycle checks, or channel-specific workflows.
---

# Glide Create Marketing Skill

## Load

- `Glide HQ/AGENTS.md`
- `Glide HQ/Source Map.md`
- `Glide HQ/Marketing Context.md`
- `Glide HQ/Skills Index.md`
- Existing `skills/glide-*` examples

## Process

1. Clarify the repeatable marketing job and what good output looks like.
2. Research the process using current sources, expert practice, user examples, and existing company context.
3. Separate durable workflow steps from one-off advice.
4. Design the skill as a small utility with clear trigger metadata.
5. Keep the body concise; move only genuinely reusable detail into references.
6. Add approval boundaries for posting, sending, publishing, campaign changes, spend, or external-system changes.
7. Create or update the skill in the installed skill directory.
8. Validate the skill.
9. Update `Glide HQ/Skills Index.md` and commit the change in the installed workspace git repo when the user asked for the behavior.

## Skill Shape

- Frontmatter name and description are the trigger surface.
- Load only the files needed for the job.
- Prefer steps over philosophy.
- Make outputs concrete.
- Keep schedule prompts minimal; recurring behavior belongs in the skill.

## Output

- Process summary.
- New or updated skill.
- Validation result.
- Suggested daily watchlist, source map, or content library updates if relevant.
